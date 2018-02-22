<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    Test
    <router-link to="/">回到首页</router-link>
  </div>
</template>

<script>
export default {
  name: 'Test',
  data () {
    return {
      msg: 'Welcome to Your Test App'
    }
  }
}
</script>
