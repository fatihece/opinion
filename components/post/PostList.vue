<template>
  <div
    class="container-fluid mt-5 d-flex flex-wrap justify-content-center align-items-center"
  >
    <Post v-for="index in 5" v-bind:key="index" :isAdmin= "isAdmin"/>
  </div>
</template>
<script>
import Post from "@/components/post/Post";
export default {
 components:{
    Post
 },
 props:{
  isAdmin:{
    required:false,
    default:false,
    type:Boolean
  }
 }
};
</script>
