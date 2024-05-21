<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 4
      h1 Sistema gestor de base de datos

    .row.mb-4
      .col-lg-8
        .fondo-color-sistema-m.borde-8.px-4.py-3
          p.mb-0 En el mercado existen muchos sistemas gestores de bases de datos, a continuación se usará MySQL para realizar las prácticas, pero ello no significa ni que sea el mejor, o el más completo del mercado, sino más bien el más usado para aplicaciones web, de pequeña, mediana y, en algunos casos, de gran complejidad. Es un buen punto de partida y todos los conceptos en MySQL vistos son reutilizables en PosgresSQL, Oracle, u otro motor de bases de datos relacional.
      .col-lg-4
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/121.png",style="max-width: 401px;")
    
    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 A continuación, se presenta el paso a paso de la descarga e instalación del entorno desarrollo WEB XAMPP:
    
    figure.mb-5(data-aos="zoom-in-up")
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/4CWzy5fWOXQ?si=zsGm22VgG0iLpYcY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen)
      figcaption Video. Descarga e instalación de entorno desarrollo WEB XAMPP


    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 Continuemos con la descarga e instalación de herramienta CASE MyQL #[em Workbench]:
    
    figure.mb-5(data-aos="zoom-in-up")
      .video 
        iframe(width="560" height="315" src="https://www.youtube.com/embed/C4bOTdaxoCM?si=Yg87QAmxA_gUXDtM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen)
      figcaption Video. Descarga en instalación de herramienta CASE MyQL Workbench

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 Ahora, estudiemos el diseño de una base de datos con MyQL #[em Workbench] relación de muchos a muchos:
    
    figure.mb-5(data-aos="zoom-in-up")
      img(src="@/assets/curso/temas/img-video-temporal.png")
      figcaption Video. Diseño de una base de datos con MyQL Workbench relación de muchos a muchos

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 Continuemos con el diseño de una base de datos con MyQL #[em Workbench] relación de uno a muchos:
    
    figure.mb-5(data-aos="zoom-in-up")
      img(src="@/assets/curso/temas/img-video-temporal.png")
      figcaption Video. Diseño de una base de datos con MyQL Workbench relación de uno a muchos

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 Y finalicemos con el diseño de una base de datos con MyQL #[em Workbench] relación de uno a uno:
    
    figure.mb-5(data-aos="zoom-in-up")
      img(src="@/assets/curso/temas/img-video-temporal.png")
      figcaption Video. Diseño de una base de datos con MyQL Workbench relación de uno a uno


</template>

<script>
export default {
  name: 'Tema3',
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
