<template>
  <FileUpload mode="basic" name="demo[]" url="./upload.php" 
              accept="video/*" @upload="onUpload"
              :chooseLabel="label" />
</template>

<script>
import FileUpload from 'primevue/fileupload'
export default {
  name: 'VideoSelectorControlPane',
  components: {FileUpload},
  props: {
      onUpload: Function,
      label: String
  }
}
</script>