<template>
    <b-container>
        <div class="contenido">
            <img src="@/assets/images/coche.svg" alt="" class="car1">
        </div>
    </b-container>
</template>
<script>
export default {
    name: 'Nuevo',
    date: () => {
        return {

        }
    },methods: {

    }
}
</script>
<style lang="scss" scope>
    .contenido {
        background: gray;
        padding-top: 100px;
        display: block;
        position: absolute;
        border-radius: 100%;
        border: 0px solid gray;
        box-shadow: bisque;
        display: block;
        overflow: hidden;
        width: 300px;
        height:  300px;
        margin-left: 0 auto;
        .car1 {
            width: 100px;
            //animación: 
            transition-timing-function: cubic-bezier(0,1.17,0,1.01);
            animation-name: front-move;
            animation-duration: 5s;
            animation-iteration-count: infinite;
            bottom: 0;
            left: 50px;
            position: absolute;
        }
        @keyframes front-move{
            from{
                width: 100px;
                opacity: 0;
            }
            80%{
                opacity: 1;
            }
            to{
                /*transform: translateX(-50px);*/
                opacity: 0;
                width: 200px;
            }
        }
    }
</style>