<template>
  <div>
    <h1>Setup</h1>
    <div style="margin-bottom: 1em">
      <CheckCircleStatusIcon :isComplete="true"/>
      <i class="pi pi-arrow-right" style="margin: 0 10px" />
      <CheckCircleStatusIcon :isComplete="false" />
      <i class="pi pi-arrow-right" style="margin: 0 10px" />
      <CheckCircleStatusIcon :isComplete="false" />
    </div>
    <OnboardingPane
      style="min-width: 350px; margin-top: 20px; padding-bottom: 50px"
    />
  </div>
</template>

<script>
import OnboardingPane from "./OnboardingPane";
import CheckCircleStatusIcon from "../CheckCircleStatusIcon.vue";
export default {
  name: "OnboardingFlow",
  components: { OnboardingPane, CheckCircleStatusIcon },
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