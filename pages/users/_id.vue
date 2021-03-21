<template>
  <h1>This is the page for the sub route id: {{ getId }}</h1>
</template>

<script>
export default {
  name: 'UserId',
  layout: 'users',
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
