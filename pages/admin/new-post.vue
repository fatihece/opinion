<template>
  <PostForm @submit="savePos($event)" />
</template>
<script>
import PostForm from "@/components/admin/PostForm";
export default {
  components: {
    PostForm,
  },
  methods: {
    savePost(post) {
      console.log(post);
    },
  },
};
</script>
