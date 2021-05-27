<template>
  <div>
      <MenuMobile class="d-block d-lg-none"/>
      <MenuPc class="d-none d-lg-block"/>
      <div class="about flex-column row mx-0 mb-5 align-items-center justify-content-center">
        <h1 class="activar text-center mb-5">Activa tu asesor Bamba gratis</h1>
        <form data-aos="fade-up" data-aos-anchor-placement="top-bottom" class="row m-0 flex-column justify-content-center align-items-center" v-on:submit.prevent="sendUser">
          <div class="cont-formulario">
              <div class="form-row row m-0">
                <div class="margen-entre-inputs col-md-4 px-2">
                  <input :class="{error : formulario.nombre == ''}" v-model="formulario.nombre" type="text" class="form-control" id="validationDefault01" placeholder="Nombre*" required>
                  <span class="label-fecha mt-2" style="color:red" v-if="formulario.nombre == ''">El campo es requerido</span>
                </div>
                <div class="margen-entre-inputs col-md-4 px-2">
                  <input :class="{error : formulario.primer_apellido == ''}" v-model="formulario.primer_apellido" type="text" class="form-control" id="validationDefault02" placeholder="Apellido paterno*" required>
                  <span class="label-fecha mt-2" style="color:red" v-if="formulario.primer_apellido == ''">El campo es requerido</span>
                </div>
                <div class="margen-entre-inputs col-md-4 px-2">
                  <input :class="{error : formulario.segundo_apellido == ''}" v-model="formulario.segundo_apellido" type="text" class="form-control" id="validationDefaultUsername" placeholder="Apellido materno*" aria-describedby="inputGroupPrepend2" required>
                  <span class="label-fecha mt-2" style="color:red" v-if="formulario.segundo_apellido == ''">El campo es requerido</span>
                </div>
              </div>

              <div class="form-row row m-0">
                <div class="margen-entre-inputs col-md-4 px-2">
                    <select  :class="{error : formulario.genero == ''}" v-model="formulario.genero" class="custom-select w-100">
                      <option selected>Género</option>
                      <option class="marke"  value="Mujer">Mujer</option>
                      <option class="marke"  value="Hombre">Hombre</option>
                    </select>
                    
                </div>
                <div class="margen-entre-inputs col-md-4 px-2">
                  <input :class="{error : formulario.celular == ''}" v-model="formulario.celular" type="text" class="form-control" id="validationDefault04" placeholder="Celular*" required>
                  <span class="label-fecha mt-2" style="color:red" v-if="formulario.celular == ''">Proporciona tu celular</span>
                </div>
                <div class="margen-entre-inputs col-md-4 px-2">
                  <input :class="{error : formulario.email == ''}" v-model="formulario.email" type="email" class="form-control" id="validationDefault05" placeholder="Email*" required>
                  <span class="label-fecha mt-2" style="color:red" v-if="formulario.email == ''">Proporciona tu email</span>
                </div>
              </div>
              <div class="form-group form-fecha col-md-4 margen-entre-inputs p-0 row m-0 justify-content-between">
                <div class="col-4 ">
                  <select v-model="dia" class="custom-select w-100">
                    <option class="marke" selected>Día</option>
                    <option class="marke" v-for="(items, index) in fecha.dia" :key="index" :value="items">{{items}}</option>
                  </select>
                </div>
                
                <div class="col-4  ">
                  <select v-model="mes" class="custom-select w-100">
                    <option class="marke" selected>Mes</option>
                    <option class="marke" v-for="(items, index) in fecha.meses" :key="index" :value="items">{{items}}</option>
                  </select>
                </div>
                <div class="col-4  ">
                    <select v-model="year" class="custom-select w-100">
                      <option class="marke" selected>Año</option>
                      <option class="marke" v-for="(items, index) in fecha.año" :key="index" :value="items">{{items}}</option>
                    </select>
                </div>
                <label class="label-fecha mt-3">Fecha de nacimiento*</label>
              </div>
          </div>
          <button class="btn enlace-activar col-md-2 py-2 col-4 mt-4" type="submit">Activar</button>
      </form>
      </div>
      
      <Footer/>
  </div>
</template>
<script>
import axios from "axios"
import MenuMobile from '@/components/nav/MenuMobile.vue'
import MenuPc from '@/components/nav/Menupc.vue'
import Footer from '@/components/templates/Footer.vue'
import { fecha } from '@/utils/fechas'
export default {
  name:'AsesorbambaFormulario',
  components: {
    MenuMobile,
    MenuPc,
    Footer,
  },
  data(){
    return {
        formulario:{
        'nombre':'Juan',
        'primer_apellido':'Zuck',
        'segundo_apellido':'Bild',
        'genero':'Género',
        'celular':'12345678',
        'email':'example@bamba.com',
        'fecha': ''
    },
      fecha:fecha,
      dia:'Día',
      mes:'Mes',
      year:'Año',
    
    }
  },

  methods:{
    sendUser(){
      this.formulario.fecha = this.dia +' de '+this.mes+' del '+this.year
      const BASE_URL = "https://60a8622120a6410017305acd.mockapi.io/api/v1/user";
      if(this.formulario.nombre !== '' && this.formulario.nombre !== 'Juan' &&  this.formulario.primer_apellido !== '' && this.formulario.primer_apellido !== 'Zuck' && this.formulario.segundo_apellido !== '' && this.formulario.segundo_apellido !== 'Bild' && this.formulario.genero !== '' && this.formulario.genero !== 'Género' && this.formulario.celular !== '' && this.formulario.celular !== '12345678' && this.formulario.email != '' && this.formulario.email != 'example@bamba.com' && this.formulario.fecha != ''){
          axios.post(BASE_URL, {
          user: this.formulario
        })
        .then((res) => {
          this.formulario.nombre = '' 
          this.formulario.primer_apellido = '' 
          this.formulario.segundo_apellido = '' 
          this.formulario.genero = '' 
          this.formulario.celular = ''
          this.formulario.email = ''
          this.$router.push('/congratulation')

        })
          .catch(err => reject(err))
        return
      } else {
          console.log('hay campos vacios')
      }
      
     
    }
  }
}
</script>
<style>
.about{
  height: 85vh;
  width:100%;
}
.cont-formulario{
  max-width: 65rem;
  margin: 0 auto;
  background: #DCF0FB;
  border-radius: 8px;
  padding: 3.5rem;
}
.activar{
  color:#162E88;
  font-family: 'Montserrat-SemiBold';
  font-size:38px
}
input{
  background-color: #DCF0FB!important;
  border: #a0d6f1 solid 1px!important;
  color:#162E88!important;
  font-family: 'Montserrat-Semibold';
}
input::placeholder{
  color:#162E88!important;
  font-family: 'Montserrat-Semibold';
}
.error{
  border: red solid 1px!important;
}
.custom-select{
    display: block;
    padding: .50rem .75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color:#162E88!important;
    font-family: 'Montserrat-Semibold';
    
    background-color: #DCF0FB!important;
    border: #a0d6f1 solid 1px!important;
    border-radius: .25rem;
    transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;
}
.custom-select:focus-visible{
    outline:none;    
}
.custom-select:focus{
    box-shadow: 0 0 0 0.25rem rgb(13 110 253 / 25%);
}
.form-fecha{
  padding: 0.8rem;

}
  .enlace-activar{
    color: #FFFFFF!important;
    font-family: 'Montserrat-SemiBold';
    background: #113291!important;
    border-radius: 8px;
    font-weight: 600;
    font-size:17px
  }
  .label-fecha{
    font-family: 'Montserrat-Light';
    font-size:12px;
    color:#162E88;
  }
  .margen-entre-inputs{
    margin-bottom: 2rem;
  }
  .marke{
        background: #FFFFFF;
        padding: .50rem .75rem;
        font-family: 'Montserrat-Light';
    }
  @media only screen and (max-width: 769px) and (max-width: 428px){
    .activar{
      color:#162E88;
      font-family: 'Montserrat-SemiBold';
      font-size:24px
    }
  }
  @media only screen and (max-width: 427px){
    .margen-entre-inputs{
      margin-bottom: 1rem;
    }
     .activar{
      color:#162E88;
      font-family: 'Montserrat-Bold';
      font-size:22px;
      margin-top:4rem;
      padding: 0 2rem;
    }
     .cont-formulario{
        max-width: 100%;
        margin: 0 auto;
        background: #DCF0FB;
        border-radius: 8px;
        padding: 2rem;
    }
    .about{
      height: 100%;
      width:100%;
    }
    .cont-formulario{
      padding: 2rem;
    }
   }
</style>
