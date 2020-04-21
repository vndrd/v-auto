<template>    
    <div class="banner" id="banner">
        <b-navbar toggleable="lg" type="dark" :class="{change_color: scrollPosition > 100}" style="position:fixed;width:100%">
            <b-navbar-brand href="#">ZXC</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav>
                    <b-nav-item href="#" v-scroll-to="'#banner'">Inicio</b-nav-item>
                    <b-nav-item href="#" v-scroll-to="{ el: '#servicios', offset: -50 }">Servicios</b-nav-item>
                    <b-nav-item href="#" >Contacto</b-nav-item>
                </b-navbar-nav>
                <!-- Right aligned nav items -->
                <b-navbar-nav class="ml-auto izq">
                    <li>
                        <img src="@/assets/images/WhatsApp_Logo_3.png" alt="" width="40px" class="img-fluid">
                        <span>+591</span> 77777777 
                    </li>
                    <li>
                        <img src="@/assets/images/gps-icon.png" alt="" width="30px" class="img-fluid">
                        <span>El Alto</span> | Zona QWE calle 2</li>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>        
        <div class="text">
            <h1>Taller de Autotrónica</h1>
            <h2>ZXC</h2>
            <p>Servicios de mecánica automotríz</p>
            <b-button v-scroll-to="{ el: '#servicios', offset: -100 }">Servicios</b-button>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Navbar',
    data: () => {
        return {
            scrollPosition: null
        }
    },
    mounted: function(){
        window.addEventListener('scroll', this.updateScroll);
    },
    methods: {
        updateScroll() {
            this.scrollPosition = window.scrollY
        }
    },
    watch: {
        asd: function() {
            console.log(this.updateScroll)
        }
    }
}
</script>
<style lang="scss" scoped>
.router-link-exact-active{
    border-bottom: 1px solid yellow;
}
.banner {
    background-image: 
            linear-gradient(to top, rgba(1,1,1,.8),rgba(1,1,1,.8)),
        url('~@/assets/images/large.png');
    background-size: 115vw;
    background-repeat: no-repeat;
    height: 100vh;
    .text{
        text-align: center;
        margin: 0 auto;
        padding-top: 150px;
        color:#ddd;
        font-size: 1vw;
        h1{
            font-size: 5vw;
            margin-top: 20vh;
        }
        p{
            color: #aaa;
            font-size: 1.5vw;
        }
        button {
            margin-top: 5vh;
            padding: 10px 50px;
            background: #ad8d00;
        }
    }
    /*navbar */
}
.izq {
    li{
        color:#dfd;
        vertical-align: middle;
        padding-left: 30px;
        span {
            color:#aaa;
        }
    }
    li:nth-child(2){
        padding-top: 5px ;
    }
    img {
        
    }
}
.change_color {
    transition: .5s ease-in-out;
    background-color:#eee;
    a, li {
        color: black !important
    }
    a:hover {
        color: #666 !important
    }
}
.navbar-dark .navbar-nav .nav-link {
    color: rgba(255, 255, 255, 0.5);
    text-align: center;
}
$orig: #6A8EA9;
$prim: #f9f871;
$prim2: #a8ee8d;
$prim3: #62dcad;
$prim4: #39c5c1;
$prim5: #4eaac0;
$prim6: #6a8ea9;


</style>