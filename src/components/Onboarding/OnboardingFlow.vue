<template>
  <div>
    <h1>Setup</h1>
    <div style="margin-bottom: 1em">
      <CheckCircleStatusIcon :isComplete="stepsCompleted >= 1" />
      <i class="pi pi-arrow-right" style="margin: 0 10px" />
      <CheckCircleStatusIcon :isComplete="stepsCompleted >= 2"/>
      <i class="pi pi-arrow-right" style="margin: 0 10px" />
      <CheckCircleStatusIcon :isComplete="stepsCompleted === 3"/>
    </div>
    <OnboardingPane
      style="min-width: 350px; margin-top: 20px; padding-bottom: 50px"
      :onStepComplete=goToNextStep
      :onStepGoBack=goToPreviousStep
    />
  </div>
</template>

<script>
import OnboardingPane from "./OnboardingPane";
import CheckCircleStatusIcon from "../CheckCircleStatusIcon.vue";
import { ref } from "vue";
export default {
  name: "OnboardingFlow",
  components: { OnboardingPane, CheckCircleStatusIcon },
  setup() {
    let stepsCompleted = ref(0);
    function goToNextStep() {
      stepsCompleted.value++;
    }
    function goToPreviousStep() {
      stepsCompleted.value--;
    }
    return {
      stepsCompleted,
      goToNextStep,
      goToPreviousStep
    }
  },

};
</script>

<style scoped>
p {
  line-height: 1.5;
  margin: 0;
}
i {
  font-size: 2rem;
}
</style>