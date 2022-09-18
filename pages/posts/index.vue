<template>
    <div>
      <PostList  :posts="fetchedPosts"/>
    </div>
  </template>
  
  <script>
  import PostList from "@/components/post/PostList";

  export default {
    components: {
      PostList,

    },
    asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        fetchedPosts: [
          {
            id: 1,
            title: "Ece && Gülce",
            subTitle: "Ece ile Gülce'nin maceraları",
            text: "Builds on top of standard HTML, CSS and JavaScript with intuitive API and world-class documentation.",
          },
          {
            id: 1,
            title: "Naz && Nil",
            subTitle: "Naz ile Nil'in maceraları",
            text: "A rich, incrementally adoptable ecosystem that scales between a library and a full-featured framework.",
          },
        ],
      });
    }, 2000);
  },
  };
  </script>
   