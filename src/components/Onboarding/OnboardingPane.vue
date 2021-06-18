<template>
  <form id="signup-form" @submit.prevent="processForm">
    <Card style="min-height: 300px">
      <template #title> Choose Videos To Syncronize</template>
      <template #content>
        <div>
          <div style="margin-top: 30px">
            <input type="file" id="video1" name="video1" accept="video/*" @change="setVideoFilePath"><br><br>
            
          </div>
          <div style="margin-top: 20px; margin-bottom: 30px">
            <input type="file" id="video2" name="video2" accept="video/*" @change="setVideoFilePath"><br><br>
          </div>
        </div>
      </template>
      <template #footer>
        <Button
          icon="pi pi-chevron-right"
          label="Next: Begin Syncing"
          iconPos="right"
          class="p-button-outlined p-button-secondary"
          style="margin-bottom: 30px"
          @click=onStepComplete
          type="submit"
        />
      </template>
    </Card>
  </form>
</template>

<script>
import Button from "primevue/button";
import Card from "primevue/card";
export default {
  name: "OnboardingPane",
  components: { Button, Card },
  props: {
    onStepComplete: Function,
  },
  data() {
    return {
      video1: false,
      video2: false
    }
  },
  methods: {
    setVideoFilePath(evt, index) {
      console.log(evt.target.value)
      console.log(index)
      console.log(this.video1)
      console.log(this.video1)
    }
  }

};
</script>

<style scoped>
p {
  line-height: 1.5;
  margin: 0;
}
</style>