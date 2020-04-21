<template>
  <section class="servicios">
      <div class="servicios-banner">  
            <h1 class="text-center text-dark border-bottom-3">Servicioss</h1>    
      </div>
      <b-container>
          <b-row>
              <b-col md="4">QWE</b-col>
              <b-col md="4">ASD</b-col>
              <b-col md="4">ZXC</b-col>
          </b-row>
          Icons made by <a href="https://www.flaticon.com/authors/google" title="Google">Google</a> from <a href="https://www.flaticon.com/" title="Flaticon"> www.flaticon.com</a>
      </b-container>
  </section>
</template>

<script>
export default {
  name: 'Servicios',
  props: {
    msg: String
  }
}
//http://talleresgonzalo.com/
//https://prezi.com/ifg8e0v3dxos/diseno-de-una-pagina-web-de-un-taller-mecanico/
//http://www.autocarrascosa.es/home/
</script>

<style scoped lang="scss">
.servicios{
    min-height: 90vh;
    background-color: white;
}
.servicios-banner {
    background:white;
    height: 30vh; 
    /*background-size: 50vw;*/
    background-size: 120vw;
    background-position: right;
    background-image:linear-gradient(to bottom, rgba(255,255,255,1),rgba(255,255,255,.2)),
    
    url('~@/assets/images/rec1416.png');
    /* parallax */
    background-attachment: fixed;
    background-repeat: no-repeat;
    background-size: cover;
    /*vertical align h1*/
    position: relative;
}
.servicios-banner h1{
    font-weight: bold;
    font-size: 300%;
    /*vertical align */
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 50%;
    height: 30%;
    margin: auto;
}
</style>
