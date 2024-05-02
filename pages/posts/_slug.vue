<template>
  <div class="container">
    <div class="zalogo">
        <h1>О товаре</h1>
    </div>
    <div class="row">
      <div class="col-lg-8">
        <nav aria-label="breadcrumb" class="mt-4">
          <ol class="breadcrumb">
            <li class="breadcrumb-item"><nuxt-link to="/">Главная</nuxt-link></li>
            <li class="breadcrumb-item active" aria-current="page">{{ post.title }}</li>
          </ol>
        </nav>
        <img class="img-fluid rounded " :src="post.photo" alt="">
        <hr>
        <p v-html="post.description">
        </p>
        <hr>
        <h4 class="card-price">{{ post.price }} р.</h4>
        <div class="d-flex justify-content-end">
        </div>
        <hr>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  async asyncData({params}) {
    const post = await axios.get(`http://127.0.0.1:8000/api/posts/${params.slug}`);
    return {
      post: post.data,
    }
  },
}
</script>