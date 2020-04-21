<template>
  <section class="servicios" id="servicios">
    <b-container class="pt-5">
        <h1 class="text-center">¿Qué necesitas?</h1>
        <b-row>
            <b-col lg="3">
                <b-card bg-variant="secondary" text-variant="dark" class="text-center"
                >   
                    <h4>Chapa y Pintura</h4>
                    <a href="#"> Ver mas</a>
                </b-card>
            </b-col>
            <b-col lg="3">
                <b-card bg-variant="secondary" text-variant="dark" class="text-center"
                >
                    <h4>Chapa y Pintura</h4>
                    <a href="#"> Ver mas</a>
                </b-card>
            </b-col>
            <b-col lg="3">
                
            </b-col>
        </b-row>
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
.container {
    h1{
        color:#555;
    }
}
.text-servicios {
    color: #6A8EA9;
}
.servicios:nth-child(1){
    min-height: 1000px !important;
    background: #fff;
}
.bg-secondary {
    background-color: #fff !important;
}
.card {
    border: 1px solid #fff !important;
    min-height: 250px;
    img{
        filter: contrast(.2);
        background: linear-gradient(to bottom, white, black);
        cursor: pointer;
    }
    img:hover {
        opacity: 0.5;
        transition: 1s ease; 
        filter: brightness(1);
    }

}
</style>
