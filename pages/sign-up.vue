<template>
    <div class="sign">
        <!--logo-->
        <div class="logo">
            <nuxt-link to="/">
                <img src="../assets/img/logo.png"/>
            </nuxt-link>
        </div>
        <!--注册的表单-->
        <div class="main">
            <div class="title">
                <h4>
                    <nuxt-link to="/sign-in">登录</nuxt-link>
                    <b>·</b>
                    <nuxt-link  class="active" to="/sign-up">注册</nuxt-link>
                </h4>
            </div>
            <div class="js-sign-up">
                <form action="" method="post">
                    <div class="input-prepend">
                        <input class="top-radius" type="text" placeholder="你的昵称">
                        <i class="fa fa-user"></i>
                    </div>
                    <div class="input-prepend">
                        <input type="text" placeholder="手机号">
                        <i class="fa fa-phone"></i>
                    </div>
                    <div class="input-prepend ssm">
                        <input type="text" placeholder="请输入验证码">
                        <i class="fa fa-shield"></i>
                        <a class="send-ssm btn btn-success" href="">发送验证码</a>
                    </div>
                    <div class="input-prepend">
                        <input class="bottom-radius" type="text" placeholder="设置密码">
                        <i class="fa fa-lock"></i>
                    </div>
                    <input class="btn btn-success sign-up-btn" type="button" value="注册">
                    <p class="sign-up-msg">
                        点击 “注册” 即表示您同意并愿意遵守简书 <br>
                        <a href="#"> 用户协议 </a>
                        和
                        <a href="#">隐私政策</a> 。
                    </p>
                </form>
                <div class="more-sign">
                    <p>社交账号登录</p>
                    <ul>
                        <li class="weixin">
                            <a href="">
                                <i class="fa fa-weixin"></i>
                            </a>
                        </li>
                        <li class="qq">
                            <a href="">
                                <i class="fa fa-qq"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import '~/assets/css/sign.css'
    export default {
        name: "sign-up",
        head (){
            return {
                title:'注册-简书',
                meta:[
                    {hide:'',name:'description',content:'登录页面'}
                ]
            }
        }
    }
</script>

<style scoped>

</style>