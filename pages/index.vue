<template>
  <section id="posts">
    <post-preview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id" />
  </section>
</template>

<script>
import PostPreview from "@/components/Blog/PostPreview";

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: "A New Beginning",
          previewText: "The post that started everything",
          thumbnailUrl: "https://www.bluebillywig.com/sites/default/files/styles/full_width_with_sidebar/public/thumbnailsvideo.png",
          id: "a-new-beginning"
        },
        {
          title: "A Second Beginning",
          previewText: "The second post that started everything",
          thumbnailUrl: "https://www.bluebillywig.com/sites/default/files/styles/full_width_with_sidebar/public/thumbnailsvideo.png",
          id: "a-second-beginning"
        },
      ]
    };
  }
};
</script>

<style scoped>
  #posts {
    padding-top: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }

  @media (min-width: 35rem) {
    #posts {
      flex-direction: row;
    }
  }
</style>
