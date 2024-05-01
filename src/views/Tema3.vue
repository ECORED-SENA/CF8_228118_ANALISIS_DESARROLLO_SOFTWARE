<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 3
      h1 Normalización

    .row.mb-5
      .col-lg-4
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/79.png",style="max-width: 401px;")
      .col-lg-8
        .fondo-color-sistema-m.p-4.borde-8.mb-4
          p.mb-0 La normalización es el procedimiento mediante el cual se aplican las reglas de mapeo o conversión de un modelo entidad-relación a un modelo relacional, es decir, a tablas y relaciones. Los principios rectores de este proceso son: no redundancia de datos (que no se repitan los datos) y que la dependencia de datos sea coherente (una separación lógica de datos en tablas).
        p.mb-0 Los datos redundantes desperdician espacio en disco y crean problemas de mantenimiento. Por ejemplo, en la figura 15 del tema anterior, se ve que los datos comunes de los clientes y los bancos están en la tabla persona, mientras que los datos que pertenecen exclusivamente a los empleados están en otra tabla que se relaciona con la de personas.
    
    p.mb-5 #[b Ahora, ¿qué es una dependencia incoherente?]

    .row.justify-content-center.mb-5
      .col-lg-10
        .fondo-personalizado-1.p-3.borde-12
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/80.png",style="max-width: 72px;")
            .col
              p.mb-0.text-white Aunque resulta intuitivo para un usuario buscar en la tabla de persona el correo de un cliente en particular, es posible que no tenga sentido buscar en esa columna el salario del empleado que se relaciona con esos datos de la tabla persona, porque el salario del empleado está relacionado con la tabla empleado o depende de él. Las dependencias incoherentes pueden dificultar el acceso a los datos, porque la ruta para encontrar los datos puede faltar o estar dañada.

    p.mb-5 A continuación, lo invitamos a ver el siguiente video sobre normalización.

    figure.mb-5(data-aos="zoom-in-up")
      img(src="@/assets/curso/temas/img-video-temporal.png")
      figcaption Video. Normalización
    
    p.mb-5 La siguiente tabla nos presenta las tres formas normales y sus principios.
    
    .row.justify-content-center.mb-5
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Tabla 4.] Formas normales
        .tabla-a.tabla-personalizada-1.mb-4.tam-1
          table
            thead
              tr
                th.text-start Forma normal
                th Principios
            tbody
              tr
                td #[b Primera forma normal]
                td
                  p.mb-0 Eliminar grupos de repetición en tablas individuales.
                  p.mb-0 Crear una tabla independiente para cada conjunto de datos relacionados.
                  p.mb-0 Identificar cada conjunto de datos relacionados con una clave primaria.
              tr
                td #[b Segunda forma normal]
                td
                  p.mb-0 Crear tablas independientes para conjuntos de valores que se aplican a varios registros.
                  p.mb-0 Relacionar estas tablas con una clave foránea.
              tr
                td #[b Tercera forma normal]
                td
                  p.mb-0 Eliminar los campos que no dependen de la clave.
    
    .row.justify-content-center.mb-4
      .col-lg-10
        .fondo-color-sistema-n.p-3.borde-10
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/36.svg",style="max-width: 86px;")
            .col
              p.mb-0 Hay una cuarta forma normal, también llamada forma normal de #[b #[em Boyce Codd ](BCNF)], y una quinta forma normal, pero rara vez se consideran en un diseño práctico, solo agregan complejidad al sistema y no aportan un valor funcional que aporte a la solución del problema, por esta razón no será tratada.
    
    Separador

    #t_3_1.titulo-segundo.color-acento-contenido
      h2 3.1 Dependencias funcionales
    
    .row.mb-5
      .col-lg-8
        p.mb-4 Una dependencia funcional es un tipo de restricción que termina construyendo una generalización del concepto de clave, como se estudió en el modelo E-R y en el modelo relacional. Pero no es tan fácil localizar las dependencias, debido a que necesitan de un análisis de los atributos (columnas) o, con más precisión, de las interrelaciones entre atributos y, frecuentemente, la intuición no es suficiente a la hora de encontrar y clasificar todas las dependencias. Aunque existe una teoría matemática para realizar este análisis, un ejemplo sencillo puede enseñar cómo analizar estas dependencias de manera intuitiva, tal como se presentará a continuación.

        .fondo-color-sistema-k.p-4.borde-20
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/81.png",style="max-width: 86px;")
            .col
              p.mb-4.fw-bold Ejemplo
              p.mb-0 Un cliente pide que se desarrolle un #[em software] para llevar el inventario de una ferretería, los productos, los proveedores y el precio al que cada proveedor vende cada producto, para lo cual suministra la siguiente información, y se deben identificar las dependencias funcionales para poder realizar un modelo relacional.
      .col-lg-4.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/82.png",style="max-width: 401px;")

    .row.justify-content-center.mb-5
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 16.] Proveedores, productos y precios
        figure
          img.mx-auto(src="@/assets/curso/temas/83.png",style="max-width: 1030px;",alt="Imagen que presenta la información sobre proveedores, productos y precios.")

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 El principio de no repetición de datos, indica que se deben identificar todos los datos que se repiten y se puede ver en la siguiente figura, tenido en cuenta los colores de sombreado como se muestra. Es de notar que el nit_proveedor es igual en todos los registros que tienen el mismo valor de correo, nombres y teléfono.

    .row.justify-content-center.mb-5
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 17.] Dependencia de nit_proveedor con datos del proveedor
        figure
          img.mx-auto(src="@/assets/curso/temas/84.png",style="max-width: 1030px;",alt="Imagen que presenta la dependencia de nit_proveedor con datos del proveedor.")

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 Ahora, en la siguiente figura,  la columna código_producto es la misma para la columna producto, pero difiere del precio que cada proveedor ofrece del mismo.

    .row.justify-content-center.mb-5
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 18.] Dependencia de código_producto_ con datos del producto
        figure
          img.mx-auto(src="@/assets/curso/temas/85.png",style="max-width: 1030px;",alt="La imagen presenta la dependencia de nit_proveedor con datos del proveedor.")

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 La dependencia #[b código_producto] no se cumple para el precio del producto, por lo tanto, dice que para cada proveedor y producto, debe existir un precio distinto, como se presenta en la siguiente figura.

    .row.justify-content-center.mb-5
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 19.] Dependencia de nit_proveedor, código_producto_ con precio del producto
        figure
          img.mx-auto(src="@/assets/curso/temas/86.png",style="max-width: 1030px;",alt="La imagen presenta la dependencia de nit_proveedor con datos del proveedor.")

    .row.mb-5
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 En la siguiente tabla, se observan las dependencias detectadas.
    
    .row.justify-content-center 
      .col-lg-6
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Tabla 5.] Dependencias funcionales

        .tabla-a.tabla-personalizada-1.mb-4.tam-1
          table
            thead
              tr
                th.text-start Atributo
                th Es dependencia funcional de:
            tbody
              tr
                td #[b nit_proveedor]
                td
                  p.mb-0 Correo
                  p.mb-0 Nombres
                  p.mb-0 Teléfono
              tr
                td #[b codigo_producto]
                td
                  p.mb-0 Producto
              tr
                td #[b nit_proveedor, codigo_producto]
                td
                  p.mb-0 Precio
              tr
                td(colspan="2") #[b Referencia Tabla - Norma APA]
    
    .cont-titulo-decorativo.p-2.mt-5.mb-5
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Definición formal dependencia funcional
    
    .row.mb-5 
      .col-lg-7
        p.mb-4 Se dice que un atributo X de una relación, “depende funcionalmente” de otro atributo o conjunto de atributos Y de la relación, si a todo valor (o valores del conjunto) Y le corresponde siempre el mismo valor de X.
        p.mb-0 Las dependencias funcionales de la tabla anterior se pueden representar en modelo entidad relación, teniendo en cuenta que un proveedor puede suministrar muchos productos y, a su vez, un producto puede ser proveedor por más de un proveedor, y que por cada producto que es proveído por un proveedor, existe un precio.
      .col-lg-5.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/87.png",style="max-width: 505px;")

    .titulo-sexto.color-acento-contenido
      p.mb-0 #[b Figura 20.] Diagrama entidad relación dependencia funcional
    
    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-5.borde-lg-10(style="overflow: hidden;")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/88.svg",style="max-width: 1029px;",alt="La imagen presenta el diagrama entidad relación dependencia funcional.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/89.svg",style="max-width: 1029px;",alt="La imagen presenta el diagrama entidad relación dependencia funcional.")
    
    p.mb-5 Como se puede notar, en la figura anterior, la relación provee, cuando es mapeado a un diagrama relacional, se genera una tabla intermedia provee, que debe tener un atributo adicional “precio”.

    .row.justify-content-center.mb-4
      .col-lg-12
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 21.] Diagrama relacional dependencia funcional
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/90.png",style="max-width: 1138px;",alt="Imagen que presenta el diagrama relacional dependencia funcional.")

        .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
          .burbuja2.right(style="top: 19%;")
          .burbuja2(style="bottom: -100px;left: 40px;")
          .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
            figure
              img.mx-auto(src="@/assets/curso/temas/91.png",style="max-width: 394px;",alt="Imagen que presenta el diagrama relacional dependencia funcional.")
    
    Separador

    #t_3_2.titulo-segundo.color-acento-contenido
      h2 3.2 Diseño relacional
    
    p.mb-5 Hasta este momento, se han examinado problemas concretos de las formas normales muy básicas y de la normalización. Ahora, se estudiará el modo en que se encaja la normalización en un proceso general de diseño de bases de datos y se puede hacer de una de las siguientes formas:

    .row.mb-5
      .col-lg-7
        AcordionA.acordion-personalizado-1(tipo="a" clase-tarjeta="acordion-personalizado-1__tarjeta")
          div.ms-md-5(titulo="Opción 1")
            .row.align-items-center
              .col-lg-9
                p.mb-0.ps-md-2 Convirtiendo un diagrama entidad relación a un diagrama relacional y de esa forma, obtener las tablas.
              .col-lg-3.order-first.order-lg-last
                figure.mb-4.mb-lg-0
                  img.mx-auto(src="@/assets/curso/temas/92.png",style="max-width: 106px;")
          div.ms-md-5(titulo="Opción 2")
            .row.align-items-center
              .col-lg-9
                p.mb-0.ps-md-2 Puede tener una tabla con todos los datos que se procesan en una aplicación, e identificado las dependencias funcionales, de manera que nos permite identificar las tablas y las llaves o claves primarias de cada una.
              .col-lg-3.order-first.order-lg-last
                figure.mb-4.mb-lg-0
                  img.mx-auto(src="@/assets/curso/temas/92.png",style="max-width: 106px;")
          div.ms-md-5(titulo="Opción 3")
            .row.align-items-center
              .col-lg-9
                p.mb-0.ps-md-2 Se puede hacer un diseño #[em ad hoc] (para que cumpla el requerimiento) y se debe comprobar luego que satisface la forma normal deseada.
              .col-lg-3.order-first.order-lg-last
                figure.mb-4.mb-lg-0
                  img.mx-auto(src="@/assets/curso/temas/92.png",style="max-width: 106px;")
      .col-lg-5
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/93.png",style="max-width: 505px;")

    p.mb-4 En el mundo práctico y en la medida que se tiene más experticia, las opciones 2 y 3 son las más empleadas.
    p.mb-4 A continuación, se muestra un ejemplo completo sobre cómo abordar un problema de almacenamiento de datos y transformarlo en un modelo relacional, recogiendo los conceptos vistos hasta ahora, pasando de un diagrama entidad relación a un modelo relacional, que es en todo caso el objetivo general de un diseño de base de datos.

    .fondo-personalizado-7.mb-5
      .fondo-personalizado-7__contenido
        .row.mb-4.pt-4
          .col-lg-7
            p.mb-4.fw-bold Problema:
            p.mb-4 Se necesita gestionar una biblioteca escolar y nuestro cliente quiere tener ciertas herramientas a su disposición para controlar publicaciones tales como libros, revistas, folletos y también llevar un registro de los estudiantes y préstamos. Adicionalmente, se necesita un control de los ejemplares de cada libro o publicación, su ubicación y su estado, registrar la retirada de libros por préstamo y restitución de ejemplares, para esto necesita información sobre editoriales datos como dirección, teléfono y nombre de la editorial.

            .fondo-color-sistema-n.p-3.borde-10
              .row.align-items-center 
                .col-md-auto
                  figure.mb-4.mb-md-0
                    img.mx-auto(src="@/assets/curso/temas/94.png",style="max-width: 86px;")
                .col
                  p.mb-0 De cada publicación se pueden tener varios ejemplares, por ejemplo: del libro Nacho lee, la biblioteca tiene 5 ejemplares, también de cada publicación se debe conocer, su autor o autores, el tema que trata la publicación (geografía, física, matemática, etc.) y la editorial. Cada libro tiene un título, idioma, formato (digital web, impreso, digital CD), código ISBN y fecha de publicación.
          .col-lg-5
            figure.mb-4.mb-lg-0
              img.mx-auto(src="@/assets/curso/temas/95.png",style="max-width: 470px;")
        
        p.mb-4 Cada ejemplar tiene un código de barras, cuando un ejemplar ya está muy descargado se debe poder dar de baja; es decir, que ya se puede botar y no usarlo más.

        .row.pb-4
          .col-auto.d-none.d-lg-block
            img(src="@/assets/curso/temas/96.svg",style="max-width: 85px;")
          .col
            p.mb-4 Tanto el estudiante, como el autor de un libro tienen los siguientes datos: nombres, apellidos, correo. Adicional, un estudiante tiene los datos de documento de identidad, teléfono, dirección, grado escolar.
            p.mb-0 De cada préstamo interesa saber qué ejemplar se prestó, fecha en la que se prestó, la fecha en que se devolvió y alguna nota o comentario.

    .row.justify-content-center 
      .col-lg-6.col-md-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 22.] Análisis de relacionar autor
        figure
          img.mx-auto(src="@/assets/curso/temas/98.svg",style="max-width: 607px;", alt="La imagen presenta el análisis de relacionar autor.")





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
