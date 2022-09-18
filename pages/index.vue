<template>
  <div>
    <PostList :posts="fetchedPosts" />
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
  // data() {
  //   return {
  //     fetchedPosts: [
  //       {
  //         id: 1,
  //         title: "Ece && Gülce",
  //         subTitle: "Ece ile Gülce'nin maceraları",
  //         text: "Builds on top of standard HTML, CSS and JavaScript with intuitive API and world-class documentation.",
  //       },
  //       {
  //         id: 1,
  //         title: "Naz && Nil",
  //         subTitle: "Naz ile Nil'in maceraları",
  //         text: "A rich, incrementally adoptable ecosystem that scales between a library and a full-featured framework.",
  //       },
  //     ],
  //   };
  // },
  asyncData(context, callback) {
    console.log("Async çalıştı.")
    console.log("context",context)
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
