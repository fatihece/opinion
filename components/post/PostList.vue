<template>
  <div
    class="container-fluid mt-5 d-flex flex-wrap justify-content-center align-items-center"
  >
    <Post v-for="index in 5" v-bind:key="index" />
  </div>
</template>
<script>
import Post from "@/components/post/Post";
export default {
 components:{
    Post
 }
};
</script>
