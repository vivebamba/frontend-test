<template>
  <div class="home ">
    <MenuMobile class="d-block d-sm-block d-lg-none"/>
    <MenuPc class="d-none d-sm-none d-lg-block"/>
    <div class="my-5 container">
      <div class="w-100 justify-content-center row mx-auto">
        <img src="@/assets/img/logo-prueba.png" alt="" class="img-logoHome">
      </div>
        
        <div  class="p-4 primer-cont mt-3">
            <h3 class="titulos mb-3">¿Por qué estoy aquí?</h3>
            <p class="textos">Solvo y Bamba unen sus fuerzas para ofrecerte servicios financieros y protección, ayudándote a resolver imprevistos médicos 10 veces más rápido y 10 veces más económico.</p>
        </div>
        <div  class="p-3 my-4 segundo-cont">
            <h3 class="titulos mb-3">Beneficios de la alianza</h3>
            <p class="textos">Buscamos brindarte los mejores beneficios para ti y  las personas que te rodean, mediante asesoría médica y laboral que ayuda a proteger tu salud y fiananzas</p>
        </div>
    </div>

    <AsesorMobile class="container d-block d-lg-none"/>
    <AsesorPc class="container d-none d-lg-flex"/>
    <div class="row m-0 justify-content-center mb-4">
      <router-link to="/asesorbamba" class="btn enlace-activar py-2 my-4 col-md-3 col-9">Activar tu asesor Bamba gratis</router-link>
    </div>
    

    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import MenuMobile from '@/components/nav/MenuMobile.vue'
import MenuPc from '@/components/nav/Menupc.vue'
import AsesorMobile from '@/components/asesorbamba/AsesorMobile.vue'
import AsesorPc from '@/components/asesorbamba/AsesorPc.vue'
import Footer from '@/components/templates/Footer.vue'
export default {
  name: 'Home',
  components: {
    MenuMobile,
    MenuPc,
    AsesorMobile,
    AsesorPc,
    Footer
  }
}
</script>
<style>
  .img-logoHome{
    max-width: 50%!important;
    height: auto;
  }
  .titulos{
    font-family: 'Montserrat-Bold';
    color:#162E88;
    font-size:20px;
    font-weight: 700
  }
  .textos{
    color:#162E88;
    font-family: 'Montserrat-SemiBold';
  }
  .primer-cont{
    background: #DCEFFB;
    border-radius: 4px;
  }
  .segundo-cont{
    border-radius: 4px;
  }
  .enlace-activar{
    color: #FFFFFF!important;
    font-family: 'Montserrat-SemiBold';
    background: #113291!important;
    border-radius: 10px!important;
    font-weight: 600;
    font-size:15px;
    transition: ease 0.3s all!important;
    transform: scale(0.9);
  }
  .enlace-activar:hover{
    transition: ease 0.3s all;
    transform: scale(1)
  }
  @media only screen and (max-width: 426px){
    .img-logoHome{
      max-width: 70%!important;
      height: auto;
    }
     .titulos{
        font-family: 'Montserrat-Bold';
        color:#162E88;
        font-size:17px;
        font-weight: 700
    }
    .textos{
      color:#162E88;
      font-family: 'Montserrat-SemiBold';
      font-size:15px;
    }
  }
</style>