<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5.pb-0.pb-md-0
  
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción

    .fondo-personalizado-2.pos-1
      .fondo-personalizado-2__contenido
        p.mb-4(data-aos="fade") Una base de datos se puede percibir como un “almacén” de información que se define y se crea una sola vez para guardar grandes cantidades de datos de forma organizada (o estructurada), con el fin de poder encontrarla y utilizarla fácilmente.

        .row.align-items-center.pb-5
          .col-lg-8(data-aos="fade-left")
            p.mb-4 Teniendo en cuenta la anterior información, en el presente componente formativo, se presentará el concepto y características de las bases de datos actuales, tomando en cuenta que cada base de datos es diseñada para cumplir con los requisitos de información de una organización o una empresa.

            .fondo-personalizado-1.p-3.borde-12
              .row.align-items-center 
                .col-md-auto
                  figure.mb-4.mb-md-0
                    img.mx-auto(src="@/assets/curso/temas/1.svg",style="max-width: 85px;")
                .col
                  p.mb-0.text-white Estos diseños están concebidos para emplear Sistemas de Gestión de Bases de Datos (en adelante SGDB), que es un sistema o servicio informático que permite a las personas definir, crear, dar soporte y mantenimiento a las bases de datos, controlando el acceso de forma segura.
          .col-lg-4.order-first.order-lg-last(data-aos="fade-right")
            figure.mb-4.mb-lg-0
              img.mx-auto(src="@/assets/curso/temas/2.png",style="max-width: 400px;")

    
</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
}
</script>

<style lang="sass"></style>
