<template>
  <form id="signup-form" @submit.prevent="processForm">
    <Card style="min-height: 300px">
      <template #title> Choose Videos To Syncronize</template>
      <template #content>
        <div>
          <div style="margin-top: 30px">
            <FileUpload
              mode="basic"
              name="video1[]"
              url="./upload.php"
              accept="video/*"
              @upload="onUpload"
              chooseLabel="Choose Video #1"
            />
          </div>
          <div style="margin-top: 20px; margin-bottom: 30px">
            <FileUpload
              mode="basic"
              name="video2[]"
              url="./upload.php"
              accept="video/*"
              @upload="onUpload"
              chooseLabel="Choose Video #2"
            />
          </div>
        </div>
      </template>
      <template #footer>
        <Button
          icon="pi pi-chevron-right"
          label="Next: Begin Syncing"
          iconPos="right"
          class="p-button-outlined p-button-secondary"
          disabled="disabled"
          style="margin-bottom: 30px"
        />
      </template>
    </Card>
  </form>
</template>

<script>
import Button from "primevue/button";
import Card from "primevue/card";
import FileUpload from "primevue/fileupload";
export default {
  name: "OnboardingPane",
  components: { Button, Card, FileUpload },
};
</script>

<style scoped>
p {
  line-height: 1.5;
  margin: 0;
}
</style>