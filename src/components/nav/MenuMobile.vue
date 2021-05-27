<template>
  <div class="hello">
    <div class="cont-barra row mx-0 justify-content-between w-100 align-items-center pt-3">
        <router-link to="/" class="col-3">
          <img src="@/assets/img/bamba-logo.png" alt="" class=" img-log">
        </router-link>
        <button class="btn col-3" @click="show = true">
          <svg 
          xmlns="http://www.w3.org/2000/svg" 
          xmlns:xlink="http://www.w3.org/1999/xlink" 
          aria-hidden="true" 
          focusable="false" 
          width="3em" 
          height="2.5em" 
          style="-ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" 
          preserveAspectRatio="xMidYMid meet" 
          viewBox="0 0 24 24">
            <g fill="none" 
            stroke="#C4C4C4" 
            stroke-width="2" 
            stroke-linecap="round" 
            stroke-linejoin="round">
              <path d="M3 12h18"/>
              <path d="M3 6h18"/>
              <path d="M3 18h18"/>
            </g>
          </svg>
        </button>
        <div class="cont-menu-mobile" :class="{'show-menu' : show}">
            <button @click="show = false" class="btn hidden-menu">
               <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="1em" height="1em" style="-ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 16 16"><g fill="#626262"><path d="M1.293 1.293a1 1 0 0 1 1.414 0L8 6.586l5.293-5.293a1 1 0 1 1 1.414 1.414L9.414 8l5.293 5.293a1 1 0 0 1-1.414 1.414L8 9.414l-5.293 5.293a1 1 0 0 1-1.414-1.414L6.586 8L1.293 2.707a1 1 0 0 1 0-1.414z"/></g></svg>
            </button>
            <div>
                <router-link to="/" class="w-100 justify-content-center row mx-auto mt-5">
                  <img src="@/assets/img/logo-mobile.png" alt="" class="img-logoHome">
                </router-link>
                <ul class="nav navmobile mt-5  col-12 row justify-content-between mx-auto ">
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Blog </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Bamba para todos </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Nuestros planes </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Arma tu plan </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Sobre nosotros </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Servicios gratuitos </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Preguntas frecuentes </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Contacto </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Tienda  </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link to="/" class="enlaces-nav"> Perfil </router-link></li>
                  <li class="col-12 py-2 text-center"><router-link class="enlaces-nav" to="/"> Cerrar sesión </router-link></li>
              </ul>
            </div>
        </div>
    </div>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      show:false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .cont-menu-mobile{
    height: 100vh;
    width:100%;
    background: #fff;
    position: fixed;
    z-index: 99999999;
    top:0;
    transition: 0.3s ease all;
    transform: translateY(100%);
    overflow: auto;
  }
  .show-menu{
    transition: 0.5s ease all;
    transform: translateY(0%);
    animation: circle 0.5s 
  }
  @keyframes circle {
    0%{
      border-top-left-radius: 10rem;
      border-top-right-radius: 10rem;
    }
    50%{
      border-top-left-radius: 5rem;
      border-top-right-radius: 5rem;
    }
    75%{
      border-top-left-radius: 0rem;
      border-top-right-radius: 0rem;
    }
    100%{
      border-top-left-radius: 0rem;
      border-top-right-radius: 0rem;
    }
  }
  .hidden-menu{
    position:absolute;
    right:1rem;
    top:1rem;
  }
  .cont-barra{
      background: #113291;
      position:fixed;
      top:0;
      height:5rem;
      z-index:9999
  }
  .img-log{
    width: 130px;
    height: 19px;
  }
   .navmobile li a{
        font-family: 'Montserrat-SemiBold';
        color:#113291!important;
    }
</style>
