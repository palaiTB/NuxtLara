<template>
  <div class="container">
    <h2>Making an API request</h2>
    <hr>
    <div class="row">
      <Card v-for="(post,index) in posts" :key="index" :posts="post" class="col-lg-4 mb-3" /> <!-- remember this v-for statement -->
    </div>
  </div>
</template>

<script>
  import axios from 'axios'
  import Card from '@/components/Card'
  export default{
      components:{
          Card
      },
      data(){
          return{
              posts: []
          }
      },
      asyncData(){
          return axios.get('https://jsonplaceholder.typicode.com/todos')
              .then(res => {
                  return {posts: res.data}
              })
      }
  }
</script>

<!--<script>-->
<!--  import axios from "axios";-->

<!--  export default {-->
<!--      data(){-->
<!--          return{-->
<!--              posts: []-->
<!--          }-->
<!--      },-->
<!--      mounted(){-->
<!--        axios.get('https://jsonplaceholder.typicode.com/todos')-->
<!--            .then(response => {-->
<!--              console.log(response)-->
<!--              this.posts = response.data-->
<!--            })-->
<!--            .catch(error => {-->
<!--                console.log(error)-->
<!--            })-->
<!--      }-->
<!--  }-->
<!--</script>-->
