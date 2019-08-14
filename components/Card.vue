<template>
  <div>
    <div class="card" style="width: 18rem;">
      <div class="card-body">
        <h5 class="card-title"><nuxt-link :to="{name: 'posts-id', params: {id: posts.id}}">{{posts.id}}</nuxt-link></h5>
        <h6 class="card-subtitle mb-2 text-muted">{{posts.title}}</h6>
      </div>
    </div>
  </div>
</template>

<script>
  export default{
    props: {
        posts: Object
    }
  }
</script>
