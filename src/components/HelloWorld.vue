<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <router-link to="/test">/test</router-link>
    <ul>

    </ul>
  </div>
</template>

<script>
import axios from 'axios'
var qs = require('qs');
export default {
  name: 'HelloWorld',
  beforeCreate: function () {

    let that = this
    axios.post('https://y.freekeer.com/marketing/insensitive/npo/getAreas')
      .then(function (response) {
        console.log(response)
        that.msg=response
      })
      .catch(function (response) {
        location.href='/m/'
        console.log(response);
      })
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
