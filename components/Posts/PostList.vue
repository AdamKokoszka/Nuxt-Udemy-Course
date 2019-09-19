<template>
  <div class="post-list">
    <PostPreview v-for="post in posts" :key="post.id" id="1" :is-admin="isAdmin" :title="post.title" :previewText="post.previewText" :thumbnail="post.thumbnail" />
  </div>
</template>

<script>
  import PostPreview from '~/components/Posts/PostPreview.vue'
  export default {
    props: {
      isAdmin: {
        type: Boolean,
        default: false
      },
      posts: {
        type: Array,
        required: true
      }
    },
    components: {
      PostPreview
    }
  }
</script>

<style scoped>
  .post-list {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

</style>
