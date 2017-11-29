<template>
    <div class="login tc pr">
        <div class="login-background pa"></div>
        <h3 class="title">Login</h3>
        <div class="tc ofh">
            <span class="input--hoshi">
                <input class="input__field input__field--hoshi" type="text" name="email" id="email">
                <label class="input__label input__label--hoshi input__label--hoshi-color-3" for="uid">
                <span class="input__label-content input__label-content--hoshi">邮箱</span>
                </label>
            </span>
            <span class="input--hoshi">
                <input class="input__field input__field--hoshi" type="password" name="password" id="password">
                <label class="input__label input__label--hoshi input__label--hoshi-color-3" for="uid">
                <span class="input__label-content input__label-content--hoshi">密码</span>
                </label>
            </span>
        </div>
        <div class="tc">
            <button class="btnn t-1 cp">登录</button>
            <button class="btnn t-1 cp">注册</button>
        </div>
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
