<template>
<header class="site-header">
    <nav class="navbar">
        <div class="container">
            <img src="img/logo1.png" width="167" height="111" >
            <div class="navbar-navs">
            <li> <nuxt-link class="nav-link" to="/">Главная</nuxt-link> </li>
            <li> <nuxt-link class="nav-link" to="/contact">Отзывы</nuxt-link> </li>
            </div>
            <div class="navbar-nav">
            <nuxt-link  to="/signout">Выход</nuxt-link>
            <nuxt-link to="/signin">Вход</nuxt-link>
            <nuxt-link to="/signup">Регистрация</nuxt-link>
            </div>
        </div>
    </nav>
</header>
</template>

<script>
export default {
  name: "Navbar",
}
</script>

<style scoped>

</style>