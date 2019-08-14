<template>
  <div class="container">
    <h1>hello User</h1>
    <input type="text" v-model="id">
    <button @click="loaduser">Load User</button>
  </div>
</template>

<script>
  export default {
      data(){
          return {
              id: ''
          }
      },

      methods: {
          loaduser(){
            this.$router.push(`/users/${this.id}`) //Very important line!!
          }
      }
  }
</script>
