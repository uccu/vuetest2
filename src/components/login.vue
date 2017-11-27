<template>
  <div class="tc login container">
    <h1>{{msg}}</h1>

    <form class="form" method="post" action="#/dd">
      <label></label>
      <input name="email">
      <input name="password" type="password">
      

    </form>
    <button v-on:click="te()">11</button>
  </div>
</template>

<script>
export default {
  name: 'login',
  data () {
    return {
      msg: 'Login'
    }
  },
  methods: {
    te () {
      this.msg = 'ww'
      console.log(this.msg)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
