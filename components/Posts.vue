<!--
 * @Description: 
 * @Author: jinxiaojian
 * @Email: jinxiaojian@youxin.com
 * @Date: 2019-09-02 00:35:55
 * @LastEditTime: 2019-09-02 01:01:12
 * @LastEditors: 靳肖健
 -->
<!-- ./components/Posts.vue -->
<template>
  <section class="main-content">
    <div class="container">
      <h1 class="title has-text-centered">Recent Posts.</h1>
      <div class="columns is-multiline">
        <div class="column is-half" v-for="(post,index) in posts" :key="index">
          <div class="card">
            <header class="card-header">
              <p class="card-header-title">{{ post.title }}</p>
            </header>
            <div class="card-content">
              <div class="content">
                {{ post.summary }}
                <br />
                <small>
                  by
                  <strong>{{ post.author}}</strong>
                  \\ {{ post.published }}
                </small>
              </div>
            </div>
            <footer class="card-footer">
              <nuxt-link :to="`/post/${post.id}`" class="card-footer-item">Read More</nuxt-link>
            </footer>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import posts from "~/posts.json";
export default {
  name: "posts",
  data() {
    return { posts };
  },
};
</script>