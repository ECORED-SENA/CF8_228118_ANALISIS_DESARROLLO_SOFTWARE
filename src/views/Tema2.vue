<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 2
      h1 Modelo entidad relación
    
    .row.mb-5
      .col-lg-7
        p.mb-0 Las bases de datos relacionales, inicialmente no son fáciles de modelar, por lo que se requiere de cierto nivel de abstracción, es decir, se va ocultando la complejidad del diseño de la base de datos, primero analizando el requerimiento desde un punto de vista conceptual, entendido como las necesidades de la empresa o del sistema de información, luego se va analizando desde el punto de vista de la lógica de los datos y, finalmente, se analiza físicamente cómo se almacenarán los datos. A continuación,  se presentan algunos conceptos:
      .col-lg-5.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/25.png",style="max-width: 503px;")

    
    .row.mb-5 
      .col-lg-5
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/26.png",style="max-width: 505px;")
      .col-lg-7
        AcordionA.acordion-personalizado-1(tipo="a" clase-tarjeta="acordion-personalizado-1__tarjeta")
          div.ms-md-5(titulo="Entidad")
            .row.align-items-center
              .col-lg-9.mb-4.mb-lg-0
                p.mb-0.ps-md-2 El modelo de datos entidad-relación (E-R), está basado en una percepción del mundo real que consta de una colección de objetos básicos llamados entidades, y de las relaciones entre estos objetos. Una entidad es una «cosa» u «objeto» en el mundo real que es distinguible de otros objetos. Por ejemplo, cada persona es una entidad, y las #[b cuentas] bancarias pueden ser consideradas entidades y se representa con un rectángulo.
              .col-lg-3
                figure
                  img.mx-auto(src="@/assets/curso/temas/27.svg",style="max-width: 100px;")
          div.ms-md-5(titulo="Atributos")
            .row.align-items-center
              .col-lg-9.mb-4.mb-lg-0
                p.mb-0.ps-md-2 Las entidades están descritas por un conjunto de atributos, por ejemplo, una persona puede tener estos atributos: nombres, apellidos, edad, documento de identidad (identificación); o la cuenta bancaria puede tener los siguientes atributos: número de cuenta, saldo, fecha de creación; se representan con una elipse.
              .col-lg-3
                figure
                  img.mx-auto(src="@/assets/curso/temas/28.svg",style="max-width: 100px;")
          div.ms-md-5(titulo="Relaciones")
            .row.align-items-center
              .col-lg-9.mb-4.mb-lg-0
                p.mb-0.ps-md-2 Una relación es una asociación entre varias entidades. Por ejemplo, una relación #[b titular] asocia un cliente con cada cuenta que tiene (de la que es titular). Se representa con un rombo.
              .col-lg-3
                figure
                  img.mx-auto(src="@/assets/curso/temas/29.svg",style="max-width: 100px;")

    p.mb-5 Se presentará más claro en un diagrama, pero antes se deben considerar los siguientes elementos:

    .fondo-personalizado-4.mb-5
      .fondo-personalizado-4__contenido
        .row 
          .col-lg-7.mb-4.mb-lg-0
            ul.lista-ul.lista-personalizada-2
              li
                span
                  .lista-num-per-1 1
                span Rectángulos, que representan conjuntos de entidades.
              li
                span
                  .lista-num-per-1 2
                span Elipses, que representan atributos.
              li
                span
                  .lista-num-per-1 3
                span Rombos, que representan relaciones entre conjuntos de entidades.
              li
                span
                  .lista-num-per-1 4
                span Líneas, que unen los atributos con los conjuntos de entidades y los conjuntos de entidades con las relaciones.
          .col-lg-5
            figure
              img.mx-auto(src="@/assets/curso/temas/30.png",style="max-width: 505px;")
    
    .titulo-sexto.color-acento-contenido
      p.mb-0 #[b Figura 2.] Entidad relación persona cuenta bancaria
    
    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-4(style="overflow: hidden;")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/32.svg",style="max-width: 1029px;",alt="Imagen que representa la entidad relación persona cuenta bancaria.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/33.svg",style="max-width: 1029px;",alt="Imagen que representa la entidad relación persona cuenta bancaria.")

    .row.mb-5
      .col-lg-7.mb-4.mb-lg-0
        p.mb-4 Para una base de datos de un sistema bancario consistente en clientes (es decir personas) y sus cuentas bancarias, en la figura anterior se muestra el diagrama Entidad Relación. En ells se indica que hay dos entidades que son persona y cuenta, con los atributos descritos anteriormente para cada una. El diagrama también representa la relación titular entre persona y cuenta.
        .row.mb-5
          .col-auto.d-none.d-sm-block
            img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
          .col
            p.mb-0 Se debe tener en cuenta que el modelo relacional convierte las entidades en tablas, por lo tanto, se puede poner como ejemplo que las entidades personas se conviertan en tablas como muestra la siguiente figura.
      .col-lg-5
        figure
          img.mx-auto(src="@/assets/curso/temas/34.png",style="max-width: 505px;")

    .row.justify-content-center.mb-5
      .col-lg-8
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 3.] Tablas de una entidad relación
        figure
          img.mx-auto(src="@/assets/curso/temas/35.png",style="max-width: 820px;",alt="Imagen que presenta las tablas de una entidad relación.")
    
    .row.justify-content-center.mb-5
      .col-lg-10
        .fondo-color-sistema-n.p-3.ps-4.borde-10
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/36.svg",style="max-width: 86px;")
            .col
              p.mb-0 Las tablas de la figura anterior muestran cada uno de los conjuntos de registros, la “tabla persona” muestra 6 registros y la “tabla cuenta” muestra 9 de ellas; cada uno de estos registros representa un objeto, es decir, de la tabla persona hay 6 (objetos) o personas. A la agrupación de los datos de cada registro se le llama TUPLA y, en términos sencillos, una TUPLA de una base de datos, es el conjunto de todos los atributos (columnas) de una fila.

    Separador

    

</template>

<script>
export default {
  name: 'Tema2',
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
