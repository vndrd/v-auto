<template>
    <b-navbar toggleable="md" type="light" class="nav" fixed="top">
        <b-navbar-brand href="#">
            <img alt="Vue logo" src="@/assets/images/log.svg" width="100px">
            Autotrónica XYZ
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav>
                <b-nav-item to="/" class="items">Home</b-nav-item>
                <b-nav-item to="/about" class="items">About</b-nav-item>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>    
</template>
<script>
export default {
    name: 'Navbar',
}
</script>
<style lang="scss" scoped>
$orig: #6A8EA9;
$prim: #f9f871;
$prim2: #a8ee8d;
$prim3: #62dcad;
$prim4: #39c5c1;
$prim5: #4eaac0;
$prim6: #6a8ea9;
.nav{
    background-image: linear-gradient(to left,  white, #6A8EA9);
}
.navbar-light .navbar-brand {
    color: rgba(255, 255, 255, 0.9);
}
.navbar-light .navbar-nav .nav-link {
    color: #fff;
    font-weight: bold;
}
.navbar-light .navbar-nav .nav-link:hover, .navbar-light .navbar-nav .nav-link:focus {
   border-bottom: aquamarine 1px solid;
    color: #fff;
}

.items{
    margin-left: 100px;
    color: white !important;
}
</style>