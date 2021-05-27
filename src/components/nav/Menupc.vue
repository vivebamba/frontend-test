<template>
    <div class="cont-barra w-100 py-3">
        <nav class="w-100 row mx-3 justify-content-between w-100 align-items-center ">
            <router-link to="/" class="col-1 p-0">
                <img src="@/assets/img/bamba-logo.png" alt="" class=" img-log">
            </router-link>
            <ul class="nav col-11 row justify-content-between ">
                <li class="col-2 text-center"><router-link to="/" class="enlaces-nav"> Bamba para<br/> todos </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Nuestros planes </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Arma tu plan </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Sobre nosotros </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Servicios gratuitos </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Blog </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Preguntas frecuentes </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Contacto </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Tienda  </router-link></li>
                <li class="col-1 text-center"><router-link to="/" class="enlaces-nav"> Perfil </router-link></li>
                <li class="col-1 text-center">
                    <button @click="drop" @blur="show = false" class="btn col-12 btn-sm "  type="button" data-toggle="dropdown" id="dropdownMenuLink" aria-haspopup="true" aria-expanded="false">
                        <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="1.1em" height="1.em" style="-ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 616 614"><path d="M602.442 200l-253 317c-24 29-61 29-84 0l-253-317c-24-30-12-53 25-53h540c38 0 49 23 25 53z" fill="#fff"/></svg>
                    </button>
                    <div class="dropdown-menu p-0" :class="{'d-flex' : show}" aria-labelledby="dropdownMenuLink">
                        <ul  class="nav item-drop w-100" style="background: #113291;">
                            <li class="col-12 py-2 px-3"><router-link class="enlaces-drop" to="/"> Cerrar sesión </router-link></li>
                        </ul>
                    </div>
                </li>
              
            </ul>
  
        </nav>
    </div>
</template>
<script>
export default {
    name:'Menupc',
    data(){
        return {
            show: false
        }
    },
    methods:{
        drop(){
            this.show = !this.show
        }
    }
}
</script>
<style>
    .cont-barra{
        background: #113291;
        position:fixed;
        top:0;
        z-index:9999
    }
    .img-log{
        width: 100%!important;
        height: auto;
        cursor:pointer;
    }
    .nav{
        font-family: 'Montserrat-SemiBold';
        color:#fff;
        transition: ease 0.2s all;
    }
    .nav li a:hover{
        color:#f67779!important;
        transition: ease 0.2s all;
    }
    .enlaces-nav{
        color: #ffffff!important;
        text-decoration: none!important;
        font-size: 14px;
        font-family: 'Montserrat-SemiBold';
    }
    .enlaces-drop{
        color: #ffffff;
        text-decoration: none!important;
    }
    .dropdown-menu{
        border:none!important;
        z-index:999999999;
        max-height: 30rem;
        overflow: auto;
        right: 3rem;
        margin-top: 0;
        margin-right: -4rem;
    }
    @media only screen and (max-width: 427px){
        .img-log{
            width: 113px!important;
            height: 23px;
            cursor:pointer;
        }
    }
  
</style>