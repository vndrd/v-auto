<template>
    <div>
        <b-button class="fixedIcon" pill variant="light"
        @click="fab = !fab; menu = !menu">
        <img src="@/assets/images/whatsapp.svg" alt="" width="100px" class="img-fluid rounded-circle">
        </b-button>
        <transition name="messageCard">
            <b-card
            header="Contáctanos"
            class="fixedCard"
            v-if="menu"
            > 
            <b-card-text class="b-card-texto">Hola, ¿cómo podemos ayudarte?</b-card-text>
            <b-input v-model="text"></b-input>
            <b-button href="#" @click="sendMessage" class="rounded-circle btn-send" >
                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="isolation:isolate" viewBox="0 0 20 18" width="30px" height="auto"><defs><clipPath id="_clipPath_fgX00hLzP9PnAfCkGQoSPsYB7aEGkj1G"><rect width="20" height="18"></rect></clipPath></defs><g clip-path="url(#_clipPath_fgX00hLzP9PnAfCkGQoSPsYB7aEGkj1G)"><path d=" M 0 0 L 0 7.813 L 16 9 L 0 10.188 L 0 18 L 20 9 L 0 0 Z "  fill = "#128C7E"></path></g></svg>
            </b-button>
            </b-card>
        </transition>
    </div>
</template>
<script>
export default {
    name: 'FloatedIcon',
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
<style lang="scss" scoped>
.messageCard-enter{
  opacity: 0;
  transform: translateX(100px);
}
.messageCard-enter-to{
  opacity: 1;
  transform: translateX(0px);
}
.messageCard-enter-active, .messageCard-leave-active{
    transition: .5s;
}
.messageCard-leave{
  transform: translateX(0px);
  opacity: 1;
}
.messageCard-leave-to{
  opacity: 0;
  transform: translateX(100px);
}
.card-header {
    padding: 0.75rem 1.25rem;
    margin-bottom: 0;
    background-color: #075E54 !important;
    color: white;
    border-bottom: 1px solid rgba(0, 0, 0, 0.125);
    padding: 0xp 30px !important;
}
.card-body {
    flex: 1 1 auto;
    min-height: 1px;
    padding: 1.25rem;
    background-color: #ECE5DD;
    text-align: right;
}
.card-body input{
    background-color: #ECE5DD;
    border-radius: 100px;
    float:left;
    width: 80%;
}
.form-control:focus {
    background-color: #ECE5DD !important;
    box-shadow: 0 0 0 0.05rem #128C7E !important;
    border-color: #128C7E !important ;
}
.card-body p{
  background-color: #DCF8C6;
  border-radius: 50px;
  padding: 10px;
  display:inline-flex;
  margin: 30px 0;
}
.card-body a{
    float:left;
}

*{
  font-family: 'Roboto', sans-serif;
}
.fixedCard {
  position: fixed !important;
  bottom: 0;
  right:0;
  width:400px;
  margin: 90px 20px; 
  -webkit-box-shadow: 0px 0px 20px -3px rgba(0,0,0,0.75) !important;
  -moz-box-shadow: 0px 0px 20px -3px rgba(0,0,0,0.75) !important;
  box-shadow: 0px 0px 20px -3px rgba(0,0,0,0.75) !important;
}
.fixedIcon{
  position: fixed;
  bottom: 0;
  right:0;
  width:60px;
  padding: 0px !important;
  margin: 20px; 
  overflow: hidden;
}
.rounded-pill , .btn-light:not(:disabled):not(.disabled):active, .btn-light:not(:disabled):not(.disabled).active, .show > .btn-light.dropdown-toggle, .btn-light:focus, .btn-light.focus{
  border-radius: 50rem !important;
  -webkit-box-shadow: 0px 0px 20px -3px rgba(0,0,0,0.75) !important;
  -moz-box-shadow: 0px 0px 20px -3px rgba(0,0,0,0.75) !important;
  box-shadow: 0px 0px 20px -3px rgba(0,0,0,0.75) !important;
}
.fixedIcon img{
  width: 100%;
  height: auto;
}
.btn-light {
    color: #212529;
    background-color: rgba(0,0,0,0) !important;
    border-color: rgba(0,0,0,0) !important;
}
.btn-send {
  border: 0px solid red !important;
  margin-left: 10px;
  width: 40px;
  height: 40px;
  background-color: #ECE5DD !important;
  align-content: center;
  svg{
    margin: 0 auto;
  }
}
.btn-send:hover {
  background-color: #dCd5cD !important;
}
</style>