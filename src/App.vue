<template>
  <div id="app">
    <Navbar :gotoServices="gotoServices"/>
    <router-view/>
  </div>
</template>
<script>
import Navbar from '@/components/Navbar3.vue'
export default {
  components: {Navbar},
  
  methods: {
    gotoServices: function(e){
            e.preventDefault()
            var container = this.$el.querySelector("#servicios");
            console.log("ssscontainer")
            console.log(container)
            setTimeout(() => {
              container.scrollIntoView();
              
            }, 1000);
            
        }
  }
}
</script>
<style scope lang="scss">
  .custom-b-nav-item {
    text-decoration: none;
    color:#ffffff;
  }
  nav{
    &.router-link-exact-active {    
      color: #42b983;
    }
  }
</style>
