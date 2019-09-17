<template>
  <div class="post-list">
    <PostPreview id="1" :is-admin="isAdmin" title="First Title" previewText="Hello!" thumbnail="https://www.macobserver.com/wp-content/uploads/2017/10/code-2434271_1280-1200x630.jpg" />
    <PostPreview id="2" :is-admin="isAdmin" title="Second Title" previewText="H1!" thumbnail="https://www.macobserver.com/wp-content/uploads/2017/10/code-2434271_1280-1200x630.jpg" />
    <PostPreview id="3" :is-admin="isAdmin" title="Third Title" previewText="Hi" thumbnail="https://www.macobserver.com/wp-content/uploads/2017/10/code-2434271_1280-1200x630.jpg" />
  </div>
</template>

<script>
  import PostPreview from '~/components/Posts/PostPreview.vue'
  export default {
    props: {
      isAdmin: {
        type: Boolean,
        default: false
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
