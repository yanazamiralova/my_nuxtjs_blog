<template>
<div>
    <div class="zalogo" width = 100%>
        <h1>Главная</h1>
    </div>
    <div class = "goog">
    <div v-for="post in posts" :key="post.slug" class="blog">
        <img class = "media"  height="150" :src="post.photo">
        <p class="title"> {{ post.title }}</p>
        <p class="price"><b>{{ post.price }}p.</b></p>
        <nuxt-link :to="`/posts/${post.slug}`" class="model">О товаре</nuxt-link>
    </div>
    </div>
</div>
</template>


<script>
import axios from "axios";
export default {
  async asyncData(ctx) {
    const { data } = await axios.get(`http://127.0.0.1:8000/api/posts/`);
    return {
      posts: data.results,
    }
  }
}
</script>