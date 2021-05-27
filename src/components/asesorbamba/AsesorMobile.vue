<template>
    <div >
        <carousel :autoplay="false" :items="1"  :nav="false" class=" w-100 align-items-center d-flex justify-content-around mx-auto p-0">
            
                <div class="cont-asesor px-0 pt-4 flex-column row mx-3 align-items-center">
                    <div>
                        <p class="titulos-carrusel">Asersor Bamba gratis para que tengas atención y acompañamiento personalizado 24/7 para apoyo en resolución de imprevistos de forma rápida y eficaz.</p>
                        <ul class="list-carrusel">
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Búsqueda de precios en farmacias y laboratorios</span>    
                            </li>
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Agendar citas con médicos especialistas por video consulta o presencial</span>    
                            </li>
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Buscar los mejores hospitales, clínicas para atender cualquier padecimiento.</span>    
                            </li>
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Entre otros</span>    
                            </li>
                        </ul>
                    </div>
                    
                    <img src="@/assets/img/monito-1.png" alt="" class="img-asesor">
                </div>
                <div class="cont-asesor px-0 pt-4 flex-column row mx-3 align-items-center">
                    <div>
                        <p class="titulos-carrusel ">Soluciones de protección (de primer nivel) a la medida</p>
                        <ul class="list-carrusel ">
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Planes pre-diseñados o modulares en donde puedes combinar seguros de accidentes y consultas con especialistas</span>    
                            </li>
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Cobertura flexible (anual/mensual)</span>    
                            </li>
                            <li>
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="0.4em" height="0.4em" style="margin-right:0.5rem; -ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><g fill="none"><circle cx="12" cy="12" r="10" fill="#162E88"/></g></svg>
                                <span>Precios justos y accesibles para todos</span>    
                            </li>
                        </ul>
                    </div>
                
                    <img src="@/assets/img/monito-2.png" alt="" class="img-asesor">
                </div>
                    <template slot="prev"><span class="prev arrow "><svg class="senal" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="1em" height="1em" style="-ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><path fill="#ffffff" d="M13.83 19a1 1 0 0 1-.78-.37l-4.83-6a1 1 0 0 1 0-1.27l5-6a1 1 0 0 1 1.54 1.28L10.29 12l4.32 5.36a1 1 0 0 1-.78 1.64z"/></svg></span></template>
                    <template slot="next"><span class="next arrow "><svg class="senal" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" focusable="false" width="1em" height="1em" style="-ms-transform: rotate(360deg); -webkit-transform: rotate(360deg); transform: rotate(360deg);" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24"><path fill="#ffffff" d="M10 19a1 1 0 0 1-.64-.23a1 1 0 0 1-.13-1.41L13.71 12L9.39 6.63a1 1 0 0 1 .15-1.41a1 1 0 0 1 1.46.15l4.83 6a1 1 0 0 1 0 1.27l-5 6A1 1 0 0 1 10 19z"/></svg></span></template>
             
        </carousel>
    </div>
</template>
<script>
import carousel from 'vue-owl-carousel'
export default {
    components: { carousel },
    name:'AsesorMobile'
}

</script>
<style>
    .cont-asesor{
        background: #FEE4E5;
        border-radius: 12px;
    }
    .titulos-carrusel{
        font-family: 'Montserrat-SemiBold';
        color:#162E88;
        font-size:15px;
        font-weight: 700;
        line-height: 2;
        padding: 0 3rem;
        
    }
    .list-carrusel{
        font-family: 'Montserrat-Light';
        color:#162E88;
        font-size:15px;
        padding: 0 3rem;
    }
    .list-carrusel li{
        padding:0.5rem 0;
        list-style: none;
    }
    .arrow{
        position: absolute;
        z-index:2;
        background: rgba(17, 50, 145, 0.8);
        border-radius: 100%;
        
    }
    .prev{
        margin-right:-1rem;
    }
    .next{
        margin-left:-2rem;
    }
    .senal{
        height: 2rem;
        width: 2rem;
    }

    .img-asesorD{
        max-width: 80%!important;
        min-width: 80%!important;
    }

    .second{
        margin-top: 5rem!important;
    }
    .owl-carousel{
        padding: 0!important
    }
    .activar{
        color:#162E88;
        font-family: 'Montserrat-Bold';
        font-size:38px
    }
    @media only screen and (max-width: 768px) and (min-width: 427px){
        .img-asesor{
            max-width: 18rem!important;
            min-width: 18rem!important;
        }
    }
    @media only screen and (max-width: 426px){
        
        .titulos-carrusel{
            font-family: 'Montserrat-SemiBold';
            color:#162E88;
            font-size:15px;
            font-weight: 700;
            line-height: 2;
            padding: 0 1rem ;
        }
        .list-carrusel{
            font-family: 'Montserrat-Light';
            color:#162E88;
            font-size:15px;
            padding: 0rem 1rem;
        }
        .list-carrusel li{
            padding:0.5rem 0;
            list-style: none;
        }
    }
</style>