<!--
 * @Description: 
 * @Author: jinxiaojian
 * @Email: jinxiaojian@youxin.com
 * @Date: 2019-09-01 23:48:15
 * @LastEditTime: 2019-09-02 01:07:17
 * @LastEditors: 靳肖健
 -->
<!-- ./pages/index.vue -->
<template>
  <div>
    <section class="hero is-medium is-primary is-bold">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">Welcome to the JavaScript SSR Blog.</h1>
          <h2 class="subtitle">Hope you find something you like.</h2>
          <br />
          <posts />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Posts from "../components/Posts.vue";

export default {
  head: {
    title: "Home",
  },
  components: {
    Posts,
  },
};
</script>
<style scoped>
.container {
  height: 100vh;
}
</style>