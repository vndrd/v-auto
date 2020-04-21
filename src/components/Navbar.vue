<template>
<nav class="navbar navbar-dark bg-dark fixed">
    <a class="navbar-brand" href="#">Navbar w/ text</a>
    <li class="nav-item active">
        <router-link to="/">Home</router-link>
    </li>
    <li class="nav-item">
        <router-link to="/about">about</router-link>
    </li>
</nav>
</template>
<script>
export default {
    name: 'Navbar',
}
</script>
<style lang="scss" scoped>
    .nav{
        background: #6A8EA9;
    }
    .items{
        margin-left: 100px;
        color: white !important;
    }
</style>