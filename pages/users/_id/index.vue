<template>
 <div>
  <h1>A single user</h1>
  <h3>ID: {{ $route.params.id }}</h3>
<!--  http://localhost:3000/users/9-->
 </div>
</template>
<script>
export default {
  validate(data) {
    console.log(data);
//    return data.params.id == 1
    return /^\d+$/.test(data.params.id)
  },
  layout: 'users'
}
</script>