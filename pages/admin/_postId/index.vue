<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
  import AdminPostForm from '@/components/Admin/AdminPostForm'
  export default {
    components: {
      AdminPostForm
    },
    data() {
      return {
        loadedPost: {
          author: 'Adam',
          title: 'My new Post',
          content: 'My first content on this page!',
          thumbnailLink: 'https://www.macobserver.com/wp-content/uploads/2017/10/code-2434271_1280-1200x630.jpg'

        }
      }
    }
  }

</script>
<style scoped>
  .update-form {
    width: 90%;
    margin: 20px auto;
  }

  @media (min-width: 768px) {
    .update-form {
      width: 500px;
    }
  }

</style>
