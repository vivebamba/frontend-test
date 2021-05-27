<template>
    <div >
        <MenuMobile class="d-block d-lg-none"/>
        <MenuPc class="d-none d-lg-block"/>
        <div class="cont-conf row m-auto justify-content-around align-items-center my-5">
            <img data-aos="zoom-in" data-aos-duration="2000" src="@/assets/img/monito_activado.png" alt="" class="img-logoHomeActivado col-md-3  col-lg-3 d-none d-lg-block">
                <div class="col-12 col-md-9 col-lg-4 flex-column align-items-center">
                    <div>
                        <h1 class="activarD text-center mb-5">Tu asesor Bamba ha sido activado</h1>
                        <h2 class="activarD sub text-center mb-5">Aprovecha tu cúpon Bamba</h2>
                    </div>
                    <div class="row m-0 justify-content-center mb-4">
                        <p class="codigo col-lg-5 col-7 text-center">SOLVO20</p>
                    </div>
                    <div class="d-flex d-lg-none justify-content-center">
                        <img src="@/assets/img/monito_activado.png" alt="" class="img-logoHomeActivado col-md-3 col-6 ">
                        <img src="@/assets/img/monita_activada.png" alt="" class="img-logoHomeActivadoV col-md-3 col-6 ">
                    </div>
                    
                    <div class="row m-0 justify-content-center mb-4">
                        <router-link to="/asesorbamba" class="btn enlace-activar p-activar row m-auto justify-content-center align-items-center py-2 my-2  col-lg-6 col-8 mx-2">Conoce nuestros planes</router-link>
                        <router-link to="/asesorbamba" class="btn enlace-activar p-activar row m-auto justify-content-center align-items-center py-2 my-2 col-lg-4 col-8 mx-2">Arma tu plan</router-link>
                    </div>
                </div>
            <img data-aos="zoom-in" data-aos-duration="2000" src="@/assets/img/monita_activada.png" alt="" class="img-logoHomeActivadoV col-md-3 col-lg-3 d-none d-lg-block">
        </div>
        
        <Footer/>
    </div>
</template>
<script>
import MenuMobile from '@/components/nav/MenuMobile.vue'
import MenuPc from '@/components/nav/Menupc.vue'
import Footer from '@/components/templates/Footer.vue'
export default {
    name:'Congratulation',
     components: {
        MenuMobile,
        MenuPc,
        Footer
    }
}
</script>
<style>
    .img-logoHomeActivado{
        max-width:23%;
    }
    .img-logoHomeActivadoV{
        max-width:20%;
    }
    .activarD{
        color:#162E88;
        font-family: 'Montserrat-Bold';
        font-size:26px
    }
    .codigo{
        background: #DCF0FB;
        color:#162E88;
        font-family: 'Montserrat-Bold';
        font-size:16px;
        padding: 0.7rem 2rem;
        border-radius:10px;

    }
    .cont-conf{
        height: 80vh;
    }
    @media only screen and (max-width: 900px){
        .cont-conf{
            height: 100%;
            width:100%
        }
    }
    @media only screen and (max-width: 426px){
         .img-logoHomeActivado{
            max-width:46%;
        }
        .img-logoHomeActivadoV{
            max-width:43%;
        }
         .activarD{
            font-size:26px;
            padding: 0 2rem;
        }
        .sub{
            font-family: 'Montserrat-SemiBold';
            font-size:20px;
            padding: 0;
        }
        .p-activar{
            font-size:15px
        }
    }
</style>