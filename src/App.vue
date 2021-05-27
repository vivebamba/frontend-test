<template>
  <div id="app">
    <div id="nav">
     
    </div>
    
      <router-view/>
  </div>
</template>

<style>

@font-face {
    font-family: 'Montserrat-Bold';
    src: url('./assets/Fuentes/Montserrat/Montserrat-Bold.ttf') 
}
@font-face {
    font-family: 'Montserrat-SemiBold';
    src: url('./assets/Fuentes/Montserrat/Montserrat-SemiBold.ttf') 
}
@font-face {
    font-family: 'Montserrat-Light';
    src: url('./assets/Fuentes/Montserrat/Montserrat-Light.ttf') 
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: start;
  color: #2c3e50;
}
@media only screen and (max-width: 426px){
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50; 
}
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #aac9f1;
}
button, input, select{
  transform: scale(1);
  transition: 0.3s ease all;
}
button:focus, input:focus, select:focus{
  box-shadow: none!important;
  transform: scale(1.03);
  transition: 0.3s ease all;
}
.row>*{
  max-width: auto;
}


</style>
