# Prueba de Desarrollo Front End

## Introducción

**El tiempo que tienen para desarrollar la prueba es de 2 días**

Esta es la prueba técnica que hemos preparado en Bamba®, es hora de mostrar tus conocimientos y sorprendernos.

Los aspectos que se evaluarán en la tarea son los siguientes.

- Calidad en el código.
- Creatividad.
- Dominio de las tecnologías que decidan utilizar.
- Atención al detalle.

# Instrucciones

El siguiente ejercicio debe desarrollarse haciendo uso de alguno de los siguientes Herramientas:

- React
- VueJs

## Ejercicio

1. Haz fork del repositorio

1. Maquetación: Deberás traducir el diseño ubicado en `assets/mockups/` a una SPA. En la carpeta `assets/img/` encontraras todas las imagenes necesarias para la aplicación la aplicación.

1. La aplicación deberá ser desarrollada teniendo en cuenta la filosofía `Mobile First`

1. El formulario deberá tener las siguientes validaciones:

   - Nombre - requerido
   - Apellido Paterno - requerido
   - Apellido Materno - requerido
   - Genero - requerido
   - Celular - requerido, 10 dígitos,solo números
   - Email - requerido, correo válido
   - Fecha de nacimiento - requerio, no debe ser mayor a 60 años

1. **SEO Friendly:** Bamba busca siempre tener una buena posición en ránkings de búsqueda. Crear etiquetas necesarias para un buen **SEO** (hint: use las keywords: crédito,bienestar,seguridad).
   **Opcional:** agregar etiquetas para redes sociales (hint: [http://ogp.me](http://ogp.me)).

1. **Advanced CSS:** Puede usar frameworks a elección para escribir CSS (hint: bootstrap)teniendo en cuenta la compatibilidad con distintos browsers (hint opcional: Usar [BrowserStack](http://www.browserstack.com/) para chequear el renderizado en distintos navegadores).

1. Al finalizar la aplicación subela a un repositorio en tu cuenta de Github y envía un `Pull Request`a este repositorio

1. En el archivo README deberás agregar:
   - Pasos para correr la aplicación en local
   - Listado con las versiones de Node y Npm necesarias.
   - Aspectos que consideres importante para la ejecucíon de la aplicación

## Se darán puntos extras si utilizas

- Utilizas sass
- La usabilidad en móvil es muy buena
- Pruebas automatizadas

## Consideraciones Técnicas

1. El enpoint al que tendrás que enviar la información del formulario es el siguiente:

```
https://60a8622120a6410017305acd.mockapi.io/api/v1/user
```

2. Las propiedades que recibe el endpoint son las siguientes

```
{
    'name': 'Nicola',
    'lastname': 'Tesla',
    'secondLastname': 'Mandic',
    'gender': M,
    'cellphone': '5554762134',
    'birthdate': '1986-09-21'
}
```

## Contacto

Si en el transcurso del desarrollo de la prueba tienen alguna duda pueden escribirme un correo electrónico a `adrian@4uno.org` y me comunico con ustedes para apoyarles.
