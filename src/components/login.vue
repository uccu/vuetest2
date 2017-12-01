<template>
    <div class="login tc pr">
        <div class="login-background pa"></div>
        <h3 class="title">Login</h3>
        <div class="tc ofh" v-on:click.native="t()">
            <span class="input--hoshi" v-for="input in inputs">
                <input class="input__field input__field--hoshi" :type="input.type" :name="input.name" :id="input.name" v-on:focus="focus(input.name,$event)" v-on:blur="blur(input.name)">
                <label class="input__label input__label--hoshi input__label--hoshi-color-3" :for="input.name">
                <span class="input__label-content input__label-content--hoshi">{{ input.title }}</span>
                </label>
            </span>
        </div>
        <div class="tc">
            <button class="btnn t-1 cp" v-on:click="index()">登录</button>
            <button class="btnn t-1 cp">注册</button>
        </div>
    </div>
</template>

<script>
import $ from 'jquery'
export default {
  name: 'login',
  data () {
    return {
      msg: 'Login',
      inputs: [
        { name: 'email', title: '邮箱', type: 'text' },
        { name: 'password', title: '密码', type: 'password' }
      ]
    }
  },
  methods: {
    'focus': function (z, $event) {
      $('#' + z).parent().addClass('input--filled')
    },
    'blur': function (z) {
      if ($('#' + z).val().trim() === '')$('#' + z).parent().removeClass('input--filled')
    },
    index: function () {
      window.location = '#/index'
    },
    t: function () {
      console.log(1)
    }
  }
}
</script>
<style scoped>
    @import '../assets/css/input.css';
    .login{
        width:300px;height:500px;overflow:hidden
    }
    .login-background{
        background-image : url(/src/assets/pic/login-background.jpg);
        width: 100%;
        height: 100%;
        z-index: -10;
        background-size: cover;
        background-position: center center;
    }
    h3.title{
        margin-top:30px;
        color:#fff;
        font-family: fantasy;
    }
    .btnn{
        background-color:transparent;
        border:solid 1px transparent;
        color:#ccc;
        font-size:0.8em;
        opacity:0.7;
        padding:7px 15px;
        border-radius:4px;
        outline:0
    }
    .btnn:hover{
        opacity:0.97;
        border:solid 1px #ccc;
        color:#fff;
    }


</style>
