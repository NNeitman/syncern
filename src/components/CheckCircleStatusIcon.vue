<template>
    <i v-if="isComplete" class="pi pi-check-circle" v-bind="$attrs"></i>
    <i v-else class="pi pi-circle-off"  v-bind="$attrs"></i>
</template>

<script>
export default {
  name: "CheckCircleStatusIcon",
  props: {
    isComplete: Boolean
  }
};
</script>

<style scoped>
.decoration {
  font-size: .5rem;
}

i {
  font-size: 2rem;
}
</style>