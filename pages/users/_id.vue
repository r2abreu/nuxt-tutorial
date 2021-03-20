<template>
  <h1>This is the page for the sub route id: {{ getId }}</h1>
</template>

<script>
export default {
  name: 'UserId',
  validate(context) {
    return !isNaN(context.params.id);
  },
  computed: {
    getId() {
      return this.$route.params.id;
    },
  },
};
</script>
