<template>
  <div class="post-page">
    <PostList :posts="loadedPosts"/>
  </div>
</template>

<script>
  import PostList from '~/components/Posts/PostList.vue'

  export default {
    components: {
      PostList
    },
    asyncData(context) {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            loadedPosts: [
              {
                id: '1',
                title: 'My title',
                previewText: 'This is my first post',
                thumbnail: 'https://image.shutterstock.com/image-photo/colorful-flower-on-dark-tropical-260nw-721703848.jpg'
              },
              {
                id: '2',
                title: 'My second title',
                previewText: 'This is my second post',
                thumbnail: 'https://image.shutterstock.com/image-photo/bright-spring-view-cameo-island-260nw-1048185397.jpg'
              }
            ]
          });
        }, 1500);
      })
        .then(data => {
          return data
        })
        .catch(e => {
        context.error(new Error())
      });
    }
  };

</script>
<style scoped>
  .posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .post-list {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

</style>
