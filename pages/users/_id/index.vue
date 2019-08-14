<template>
  <div class="container">
    <h2>This is User's {{$route.params.id}}</h2>
  </div>
</template>

<script>
  export default {
    validate({params}){
      return /^\d+$/.test(params.id)
    }
  }
</script>
