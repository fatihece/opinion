<template>
  <div>
    <PostList />
    <About />
  </div>
</template>

<script>
import PostList from "@/components/post/PostList";
import About from "@/components/home/About";
export default {
  components: {
    PostList,
    About,
  },
};
</script>
 