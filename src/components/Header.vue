<template>
  <div class="header">
    <div class="header-top">
      <div class="h-top-left">
        <span>你好，{{nickname}}</span>&nbsp;&nbsp;&nbsp;&nbsp;
        <span>消息 <strong>0</strong></span>
      </div>
      <div class="h-top-right">
        <ul>
          <li>
            <router-link to="/order">我的订单</router-link>
          </li>
          <li>
            <router-link to="/goods">购物车</router-link>
          </li>
          <li>
            <router-link to="/goods">我的收藏</router-link>
          </li>
          <li>
            <router-link to="/goods">商家入口</router-link>
          </li>
        </ul>
      </div>
    </div>
    <div class="header-bottom">
      <div class="h-bottom-logo"></div>
      <div class="h-bottom-search">
        <input v-model="searchParam" type="text" placeholder="请输入 商品/店铺" />
        <button type="button" @click="search(searchParam)">搜&nbsp;&nbsp;索</button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Header',
    data() {
      return {
        nickname: '游客',
        searchParam: ''
      }
    },
    methods:{
      search(param){
        console.log('要搜索的内容为：',param)
      }
    }
  }
</script>

<style scoped>
  .header {
    width: 100%;
    height: 120px;
    background-color: antiquewhite;
  }

  .header-top {
    width: 100%;
    height: 40px;
  }

  .header-bottom {
    width: 100%;
    height: 80px;
  }

  .h-top-left {
    float: left;
    margin-left: 100px;
    margin-top: 10px;
  }

  .h-top-right {
    float: right;
    margin-top: 10px;
    margin-right: 100px;
  }

  .h-top-right ul {
    padding: 0;
    margin: 0;
    list-style: none;
    text-decoration: none;
    /* 去掉下划线 */
  }

  .h-top-right ul li {
    display: inline;
    padding: 0 5px;
  }

  .h-top-right ul a {
    text-decoration: none;
    /* 去掉下划线 */
  }

  .h-bottom-logo {
    float: left;
    margin-left: 100px;
    margin-top: 10px;
    width: 155px;
    height: 62px;
    background-image: url(../assets/images/logo.png);
    background-repeat: no-repeat;
    background-size: 100%;
  }

  .h-bottom-search {
    float: right;
    margin-top: 20px;
    margin-right: 100px;
  }

  .h-bottom-search input {
    -webkit-appearance: none;
    background-color: #FFF;
    background-image: none;
    border: 1px solid #DCDFE6;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    color: #606266;
    display: inline-block;
    font-size: inherit;
    height: 40px;
    line-height: 40px;
    outline: 0;
    padding: 0 15px;
    -webkit-transition: border-color .2s cubic-bezier(.645, .045, .355, 1);
    transition: border-color .2s cubic-bezier(.645, .045, .355, 1);
  }

  .h-bottom-search button {
    display: inline-block;
    line-height: 1;
    white-space: nowrap;
    cursor: pointer;
    border: 1px solid #409EFF;
    -webkit-appearance: none;
    text-align: center;
    -webkit-box-sizing: border-box;
    box-sizing: border-box;
    outline: 0;
    margin: 0;
    -webkit-transition: .1s;
    transition: .1s;
    font-weight: 500;
    padding: 12px 15px;
    font-size: 14px;
    color: #FFF;
    background-color: #409EFF;
  }
</style>
