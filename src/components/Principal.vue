<template>
  <div class="bienvenidos">
    <div class="container-fluid">      
      <b-row>
        <b-col md="6">
          <b-container pl="5">
            <div class="texto-bienvenido text-left">
              <p class="h5">Taller de AutoTrónica</p>
              <h1 class="display-4 mb-5">Servicios en mecánica automotríz </h1>
              <a href="#" class="btn btn-primary btn-lg">Servicios</a>
            </div>
          </b-container>
        </b-col>
      </b-row>


      
    </div>
  </div>
</template>

<script>
export default {
  name: 'Principal',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
.bienvenidos {
    background:white;
    height: 100vh; 
    background-size: calc(50% + 100px);
    background-position: calc(100% + 10px) 80px;
    background-repeat: no-repeat;
    background-image:
      linear-gradient(to right, rgba(245, 246, 252, 0.0), rgba(117, 119, 93, 0.73)),
      url('~@/assets/images/newone1541.png');
}
/*to bottom, rgba(245, 246, 252, 0.52), rgba(117, 19, 93, 0.73)), */
/*MEDIAS*/
@media (max-width: 768px) {

  .bienvenidos {
    background:rgba(245, 246, 252, 0.52);
    height: 100vh; 
    background-size: 768px;
    background-repeat: no-repeat;
    background-image:
      linear-gradient(to bottom, rgba(245, 246, 252, 0.52), rgba(117, 19, 93, 0.73)),
      url('~@/assets/images/newone1541.png');
  }
}
.encabezado {
  background: rgba(0, 0, 0, 0.6);
  color: #111; 
}

#menuPrincipal {
  clear: both; }

.navbar-brand {
  text-transform: uppercase;
  font-size: 1.3rem; }

.navbar-dark .navbar-toggler-icon {
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='30' height='30' viewBox='0 0 30 30'%3e%3cpath stroke='rgba(255, 255, 255, 1)' stroke-linecap='round' stroke-miterlimit='10' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3e%3c/svg%3e"); }

.navbar-toggler-icon {
  font-size: 1.8rem; }

.navbar-dark .navbar-nav .nav-link {
  color: white;
  text-align: center;
  margin: .2rem 0;
  -webkit-transition: all .3s ease;
          transition: all .3s ease; }

.navbar-dark .navbar-nav .active > .nav-link, .navbar-dark .navbar-nav .nav-link.active, .navbar-dark .navbar-nav .nav-link.show, .navbar-dark .navbar-nav .show > .nav-link {
  background: #f05f40; }

.navbar-dark .navbar-nav .nav-link:focus, .navbar-dark .navbar-nav .nav-link:hover {
  background: #f05f40; }

/*Bloque: Bienvenida*/
.texto-bienvenido {
  position:relative;
  padding-top: 200px;
  font-weight: bold;
  padding-left: 25%;
  h1{
    color: #6a8ea9;
    width: 500px;
  }
  p{
    color: #ccc;
  }
}

.btn-primary {
  background-color: #f9f871;
  border-color: #7eaac0;
  text-transform: uppercase; }

.btn-primary:hover {
  color: #fff;
  background-color: #a8ee8d;
  border-color: #c8ee8d;
  -webkit-transition: all .5s ease;
          transition: all .5s ease; 
}

</style>
