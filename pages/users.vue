<template>
  <div>
    <h1>This is the main users page</h1>
    <input v-model="id" type="text" />
    <button @click="onClick">Go to the user page</button>
    <nuxt-child />
  </div>
</template>

<script>
export default {
  name: 'UserIndex',
  layout: 'users',

  data() {
    return {
      id: '',
    };
  },
  methods: {
    onClick() {
      this.$router.push(`/users/${this.id}`);
    },
  },
};
</script>
