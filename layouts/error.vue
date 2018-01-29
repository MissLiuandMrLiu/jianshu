<template>
  <!--<section class="container">
    <h1 class="title">
      {{ error.statusCode }}
    </h1>
    <h2 class="info">
      {{ error.message }}
    </h2>
    <nuxt-link class="button" to="/" v-if="error.statusCode === 404">
      Homepage
    </nuxt-link>
  </section>-->
    <div class="four" v-if="error.statusCode === 404">
      <a href="">
        <img class="header" src="../assets/img/简书.png"/>
      </a>
      <div class="error">
        <div class="error-block">
          <img src="../assets/img/404.jpg" alt="404">
          <h3>您找的页面不存在</h3>
          <p>可能是因为您的链接地址有误、该文章已经被作者删除或转为私密状态。</p>
          <nuxt-link to="/">返回「简书」首页</nuxt-link>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  props: ['error']
}
</script>

<style scoped>
/*.title
{
  margin-top: 15px;
  font-size: 5em;
}
.info
{
  font-weight: 300;
  color: #9aabb1;
  margin: 0;
}
.button
{
  margin-top: 50px;
}*/
.four {
  position: relative;
}
.header{
  width: 300px;
  position: absolute;
  top: 40px;
  left: 40px;
}
.error {
  width: 100%;
  max-width: 1440px;
  margin: 0 auto;
  text-align: center;
}
  .error .error-block {
    padding-top: 80px;
    padding-bottom: 20px;
  }
.error .error-block h3 {
  margin: 40px 0 20px 0;
  font-weight: bold;
}
  .error .error-block p {
    margin: 10px 0 30px 0;
    font-size: 14px;
  }
  .error .error-block a {
    padding: 13px 0;
    width: 160px;
    font-size: 15px;
    border-radius: 40px;
    color: #ffffff!important;
    background-color: #42C02E;
    border-color: #42C02E;
    display: inline-block;
    text-align: center;
    vertical-align: middle;
    touch-action: manipulation;
    cursor: pointer;
    background-image: none;
    border: 1px solid transparent;
    white-space: nowrap;
    user-select: none;
  }
  @media (max-width: 768px) {
    .header {
      display: none ;
    }
  }
</style>
