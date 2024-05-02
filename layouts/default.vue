<template>
  <div>
    <Navbar />
    <div class="container">
      <Nuxt />
    </div>
    <Footer />
  </div>
</template>


<script>
import Navbar from "~/components/Navbar";
import Footer from "@/components/Footer";


export default {
  components: {
    Navbar,
    Footer,
  }
};
</script>

<style>

</style>