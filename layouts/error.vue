<template>
  <div>
    <h1>This is a customized error page</h1>
    <p v-if="error.statusCode === 404">This website could not be loaded</p>
    <p v-else>This website threw an error: {{ error.statusCode }}</p>
  </div>
</template>

<script>
export default {
  props: {
    error: {
      type: Number,
      default: null,
    },
  },
};
</script>
