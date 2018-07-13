<template>
    <div class="head-nav">
        <nav class="navbar navbar-default">
  <div class="container-fluid">
    <!-- Brand and toggle get grouped for better mobile display -->
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <a class="navbar-brand" href="#">Jun Blog</a>
    </div>

    <!-- Collect the nav links, forms, and other content for toggling -->
    <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
      <ul class="nav navbar-nav navbar-right">
        <li><router-link :to="'/'">Home</router-link></li>
        <li><router-link :to="'/photoes'">Photoes</router-link></li>
        <li><router-link :to="'/archive'">Archive</router-link></li>
        <li><router-link :to="'/me'">About Me</router-link></li>
      </ul>
    </div><!-- /.navbar-collapse -->
  </div><!-- /.container-fluid -->
</nav>
    </div>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: "home"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
<style lang="less" scoped>
@main-color: #e0bd62;
.head-nav{
    padding-bottom: 20px;
}
.navbar-default {
    background-color: transparent;
    border: 0;
  .navbar-brand {
    color: @main-color;
    font-size: 30px;
    padding-bottom: 0;
    padding-top: 25px;
  }
  .navbar-nav>li{
      width: 100px;
      text-align: center;
      a{
          padding: 25px 0 5px 0;
      }
  }
  .navbar-nav .router-link-exact-active{
    background-color: #fff;
    color: @main-color;
  }
  .navbar-nav .router-link-exact-active{
      border-bottom: solid 2px @main-color;
  }
}
</style>

