<template>
  <div class="home">
    <Principal v-if="false"/>
    <Servicios />
    <Nuevo if="false"/>
    <FloatedIcon />
    <!--Div where the WhatsApp will be rendered-->
  </div>
</template>

<script>

// @ is an alias to /src
import Principal from '@/components/Principal.vue'
import Servicios from '@/components/Servicios2.vue'
import Nuevo from '@/components/Nuevo.vue'
import FloatedIcon from '@/components/FloatedIcon.vue'
//import isMobile from 'ismobilejs';

export default {
  name: 'Home',
  components: {
    Principal, Servicios, Nuevo, FloatedIcon
  },
  data: () => {
    return {
      fab: false,
      fav: true,
      menu: false,
      message: false,
      hints: true,
      phone: '59167348032',
      text: "",
      apilink: ""
    }
  },
  watch: {
		
	},
  created: function(){
    this.apilink = 'http://';
    this.apilink += this.isMobilevue() ? 'api' : 'web';
    this.apilink += '.whatsapp.com/send?phone=' + this.phone + '&text=' + encodeURI("Hola! ");
    console.log("el apilink: ",this.apilink)
  },
  methods: {
    sendMessage: function(){
      this.apilink = 'http://';
      this.apilink += this.isMobilevue() ? 'api' : 'web';
      this.apilink += '.whatsapp.com/send?phone=' + this.phone + '&text=' + encodeURI("Hola! "+this.text);
      //this.apilink += this.isMobilevue() ? 'api' : 'web';
      window.open(this.apilink);
    },
    isMobilevue: function() {
      //https://www.npmjs.com/package/ismobilejs
        return false;
    }
  }
}
</script>
<style lang="scss">

</style>