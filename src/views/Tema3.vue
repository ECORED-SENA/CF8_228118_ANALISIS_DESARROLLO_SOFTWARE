<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 3
      h1 Normalización

    .row.mb-5
      .col-lg-4(data-aos="fade-right")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/79.png",style="max-width: 401px;")
      .col-lg-8(data-aos="fade-left")
        .fondo-color-sistema-m.p-4.borde-8.mb-4
          p.mb-0 La normalización es el procedimiento mediante el cual se aplican las reglas de mapeo o conversión de un modelo entidad-relación a un modelo relacional, es decir, a tablas y relaciones. Los principios rectores de este proceso son: no redundancia de datos (que no se repitan los datos) y que la dependencia de datos sea coherente (una separación lógica de datos en tablas).
        p.mb-0 Los datos redundantes desperdician espacio en disco y crean problemas de mantenimiento. Por ejemplo, en la figura 15 del tema anterior, se ve que los datos comunes de los clientes y los bancos están en la tabla persona, mientras que los datos que pertenecen exclusivamente a los empleados están en otra tabla que se relaciona con la de personas.
    
    p.mb-5(data-aos="fade") #[b Ahora, ¿qué es una dependencia incoherente?]

    .row.justify-content-center.mb-5
      .col-lg-10(data-aos="fade-right")
        .fondo-personalizado-1.p-3.borde-12
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/80.png",style="max-width: 72px;")
            .col
              p.mb-0.text-white Aunque resulta intuitivo para un usuario buscar en la tabla de persona el correo de un cliente en particular, es posible que no tenga sentido buscar en esa columna el salario del empleado que se relaciona con esos datos de la tabla persona, porque el salario del empleado está relacionado con la tabla empleado o depende de él. Las dependencias incoherentes pueden dificultar el acceso a los datos, porque la ruta para encontrar los datos puede faltar o estar dañada.

    p.mb-5(data-aos="zoom-in-up") A continuación, lo invitamos a ver el siguiente video sobre normalización.

    figure.mb-5(data-aos="zoom-in-up")
      .video
        iframe(width="560" height="315" src="https://www.youtube.com/embed/GF0n6Spz6zE?si=QMPKcJ4NC46KreDj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen)
      figcaption Video. Normalización

    
    p.mb-5(data-aos="fade") La siguiente tabla nos presenta las tres formas normales y sus principios.
    
    .row.justify-content-center.mb-5(data-aos="flip-up")
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
    
    .row.justify-content-center.mb-4(data-aos="fade")
      .col-lg-10
        .fondo-color-sistema-n.p-3.borde-10
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/36.svg",style="max-width: 86px;")
            .col
              p.mb-0 Hay una cuarta forma normal, también llamada forma normal de #[b #[em Boyce Codd ](BCNF)], y una quinta forma normal, pero rara vez se consideran en un diseño práctico, solo agregan complejidad al sistema y no aportan un valor funcional que aporte a la solución del problema, por esta razón no será tratada.
    
    Separador

    #t_3_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 3.1 Dependencias funcionales
    
    .row.mb-5
      .col-lg-8(data-aos="fade-right")
        p.mb-4 Una dependencia funcional es un tipo de restricción que termina construyendo una generalización del concepto de clave, como se estudió en el modelo E-R y en el modelo relacional. Pero no es tan fácil localizar las dependencias, debido a que necesitan de un análisis de los atributos (columnas) o, con más precisión, de las interrelaciones entre atributos y, frecuentemente, la intuición no es suficiente a la hora de encontrar y clasificar todas las dependencias. Aunque existe una teoría matemática para realizar este análisis, un ejemplo sencillo puede enseñar cómo analizar estas dependencias de manera intuitiva, tal como se presentará a continuación.

        .fondo-color-sistema-k.p-4.borde-20
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/81.png",style="max-width: 86px;")
            .col
              p.mb-4.fw-bold Ejemplo
              p.mb-0 Un cliente pide que se desarrolle un #[em software] para llevar el inventario de una ferretería, los productos, los proveedores y el precio al que cada proveedor vende cada producto, para lo cual suministra la siguiente información, y se deben identificar las dependencias funcionales para poder realizar un modelo relacional.
      .col-lg-4.order-first.order-lg-last(data-aos="fade-left")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/82.png",style="max-width: 401px;")

    .row.justify-content-center.mb-5(data-aos="zoom-in-up")
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 16.] Proveedores, productos y precios
        figure
          img.mx-auto(src="@/assets/curso/temas/83.png",style="max-width: 1030px;",alt="Imagen que presenta la información sobre proveedores, productos y precios.")

    .row.mb-5(data-aos="fade-right")
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 El principio de no repetición de datos, indica que se deben identificar todos los datos que se repiten y se puede ver en la siguiente figura, tenido en cuenta los colores de sombreado como se muestra. Es de notar que el nit_proveedor es igual en todos los registros que tienen el mismo valor de correo, nombres y teléfono.

    .row.justify-content-center.mb-5
      .col-lg-10(data-aos="flip-up")
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 17.] Dependencia de nit_proveedor con datos del proveedor
        figure
          img.mx-auto(src="@/assets/curso/temas/84.png",style="max-width: 1030px;",alt="Imagen que presenta la dependencia de nit_proveedor con datos del proveedor.")

    .row.mb-5(data-aos="zoom-in-up")
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 Ahora, en la siguiente figura,  la columna código_producto es la misma para la columna producto, pero difiere del precio que cada proveedor ofrece del mismo.

    .row.justify-content-center.mb-5(data-aos="fade")
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 18.] Dependencia de código_producto_ con datos del producto
        figure
          img.mx-auto(src="@/assets/curso/temas/85.png",style="max-width: 1030px;",alt="La imagen presenta la dependencia de nit_proveedor con datos del proveedor.")

    .row.mb-5(data-aos="flip-up")
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 La dependencia #[b código_producto] no se cumple para el precio del producto, por lo tanto, dice que para cada proveedor y producto, debe existir un precio distinto, como se presenta en la siguiente figura.

    .row.justify-content-center.mb-5(data-aos="fade")
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 19.] Dependencia de nit_proveedor, código_producto_ con precio del producto
        figure
          img.mx-auto(src="@/assets/curso/temas/86.png",style="max-width: 1030px;",alt="La imagen presenta la dependencia de nit_proveedor con datos del proveedor.")

    .row.mb-5(data-aos="fade")
      .col-auto.d-none.d-md-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 En la siguiente tabla, se observan las dependencias detectadas.
    
    .row.justify-content-center 
      .col-lg-6
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Tabla 5.] Dependencias funcionales

        .tabla-a.tabla-personalizada-1.mb-4.tam-1(data-aos="flip-up")
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
    
    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="flip-up")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Definición formal dependencia funcional
    
    .row.mb-5 
      .col-lg-7(data-aos="fade-right")
        p.mb-4 Se dice que un atributo X de una relación, “depende funcionalmente” de otro atributo o conjunto de atributos Y de la relación, si a todo valor (o valores del conjunto) Y le corresponde siempre el mismo valor de X.
        p.mb-0 Las dependencias funcionales de la tabla anterior se pueden representar en modelo entidad relación, teniendo en cuenta que un proveedor puede suministrar muchos productos y, a su vez, un producto puede ser proveedor por más de un proveedor, y que por cada producto que es proveído por un proveedor, existe un precio.
      .col-lg-5.order-first.order-lg-last(data-aos="fade-left")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/87.png",style="max-width: 505px;")

    .titulo-sexto.color-acento-contenido(data-aos="fade-left")
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
    
    p.mb-5(data-aos="fade-left") Como se puede notar, en la figura anterior, la relación provee, cuando es mapeado a un diagrama relacional, se genera una tabla intermedia provee, que debe tener un atributo adicional “precio”.

    .row.justify-content-center.mb-4(data-aos="flip-up")
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

    #t_3_2.titulo-segundo.color-acento-contenido(data-aos="zoom-in-up")
      h2 3.2 Diseño relacional
    
    p.mb-5(data-aos="fade") Hasta este momento, se han examinado problemas concretos de las formas normales muy básicas y de la normalización. Ahora, se estudiará el modo en que se encaja la normalización en un proceso general de diseño de bases de datos y se puede hacer de una de las siguientes formas:

    .row.mb-5(data-aos="flip-up")
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

    p.mb-4(data-aos="fade-left") En el mundo práctico y en la medida que se tiene más experticia, las opciones 2 y 3 son las más empleadas.
    p.mb-4(data-aos="fade-right") A continuación, se muestra un ejemplo completo sobre cómo abordar un problema de almacenamiento de datos y transformarlo en un modelo relacional, recogiendo los conceptos vistos hasta ahora, pasando de un diagrama entidad relación a un modelo relacional, que es en todo caso el objetivo general de un diseño de base de datos.

    .fondo-personalizado-7.mb-5(data-aos="flip-up")
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

    .row.mb-5
      .col-lg-7.mb-4.mb-lg-0(data-aos="fade-left")
        p.mb-4 En este diagrama se presenta una posible solución:
        p.mb-4 La relación entre persona y estudiante corresponde al caso estudiado en las relaciones de uno a uno (entre persona y empleado del banco), de la figura Diagrama relacional 1:1.
        p.mb-4 El tema se vuelve complejo, porque se debe analizar si aplica lo mismo para autor.
        p.mb-4 Al mapear estas entidades a diagrama relacional, resultan 3 tablas (estudiante, persona y autor), pero autor solo tendría una única columna y al no tener atributos adicionales relacionados con el autor, es prácticamente lo mismo que tener la tabla persona, por lo tanto, no es conveniente dejarlo de esta forma y más bien relacionar la publicación directamente con la entidad persona.
        p.mb-0 Se debe estudiar detenidamente el diagrama entidad relación por varios minutos, asegúrese que comprende el porqué de cada elemento y su multiplicidad.
      .col-lg-5(data-aos="fade-right")
        figure
          img.mx-auto(src="@/assets/curso/temas/99.png",style="max-width: 505px;")

    .row.justify-content-center.mb-5(data-aos="fade-left")
      .col-lg-8
        .fondo-color-sistema-k.borde-20.p-4.py-3
          .row.align-items-center
            .col-md-auto 
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/100.svg",style="max-width: 99px;")
            .col 
              p.mb-4.fw-bold Para recordar:
              p.mb-0 Una relación de muchos a muchos (N:N) se convierte en una tabla cuya llave primaria es computar por las llaves foráneas de las otras dos tablas. Una relación de uno a muchos (1:N) se convierte en una columna (llave foránea) de la tabla que tiene los muchos, y finalmente una relación de uno a uno (1:1) se convierte una columna en cualquier (llave foránea) de las dos tablas.
    
    .p-4.mt-5.fondo-personalizado-1.borde-11.mb-5(data-aos="flip-up")
      .row
        .col-auto(style="margin: auto;")
          figure.mb-lg-0.mb-2
            img(src="@/assets/curso/temas/101.png" style="max-width:72px")
        .col-lg.mb-4.mb-md-0.col-md-6
          h4.color-acento-contenido-p Modelo entidad biblioteca
          p.mb-0.text-white Lo invitamos a descargar el PDF Modelo entidad relación biblioteca, para conocer cómo queda el diagrama con el ejercicio trabajado.
        .col-md-auto.text-center(style="place-self:center;")
          a.boton.color-acento-botones(:href="obtenerLink('downloads/Modelo_entidad_relacion_biblioteca.pdf')" target="_blank")
            span(style="color:initial;") Descargar
            i.fas.fa-file-download(style="color:initial;")

    p.mb-5(data-aos="fade") A continuación, se presenta el modelo racional.

    .fondo-personalizado-7.pos-1.mb-4
      .fondo-personalizado-7__contenido
        .row.justify-content-center.mb-5
          .col-lg-10
            .titulo-sexto.color-acento-contenido
              p.mb-0 #[b Figura 23.] Modelo relacional
            figure.d-none.d-lg-block
              img.mx-auto(src="@/assets/curso/temas/102.png",style="max-width: 1030px;",alt="La imagen presenta el modelo racional.")

            .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
              .burbuja2.right(style="top: 19%;")
              .burbuja2(style="bottom: -100px;left: 40px;")
              .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
                figure
                  img.mx-auto(src="@/assets/curso/temas/103.png",style="max-width: 485px;",alt="La imagen presenta el modelo racional.")
        
        .row.align-items-center.pb-2
          .col-lg-7.mb-4.mb-lg-0
            p.mb-0 Hasta ahora se ha visto cómo distribuir el almacenamiento de los datos en tablas, de manera que no se permita la duplicidad de datos y procurando una estructura lógica, que presente la información del mundo real. Pero aún falta analizar el problema desde el punto de vista que permita garantizar que los datos que se van a insertar, son correctos, para lo cual es importante conocer las restricciones de integridad que puede tener una base de datos.
          .col-lg-5
            figure
              img.mx-auto(src="@/assets/curso/temas/104.png",style="max-width: 455px;")

    Separador

    #t_3_3.titulo-segundo.color-acento-contenido
      h2 3.3 Reglas de integridad

    .row.mb-5
      .col-lg-8(data-aos="fade-left")
        p.mb-4 Cuando se define un atributo, sin saber, se está escogiendo para él un dominio, es decir, un conjunto de valores que puede tener. Por ejemplo: en MySQL, cuando se elige un atributo de tipo entero (INT), los posibles valores que puede tener esa columna van desde -2147483648 hasta 2147483647, es decir, valores positivos o negativos, de manera que si se quieren solo valores positivos, se deben definir como entero sin signo (UNSIGNED INT), por lo tanto, los valores van desde 0 hasta 4294967295.
        .fondo-color-primario.px-3.py-4.borde-16
          .row.align-items-center 
            .col-md-auto 
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/105.png",style="max-width: 72px;")
            .col 
              p.mb-0.text-white La calidad de los datos garantiza que los datos almacenados en la base de datos cumplan con los estándares y requisitos de la organización. En otras palabras, asegura el mantenimiento de la integridad de los datos en una base de datos. Al hacerlo, aplica un conjunto de reglas a un conjunto de datos completo o específico y se almacena en la base de datos de destino, por lo consiguiente, para garantizar la integridad se debe tener en cuenta:
      .col-lg-4.order-first.order-lg-last(data-aos="fade")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/106.png",style="max-width: 400px;")

    .row.mb-5 
      .col-lg-7(data-aos="flip-up")
        AcordionA.acordion-personalizado-1(tipo="a" clase-tarjeta="acordion-personalizado-1__tarjeta")
          div.ms-md-5(titulo="Criterio de NULIDAD")
            .row.align-items-center
              .col-lg-9
                p.mb-0.ps-md-2 Cuando en una fila un atributo (columna) es desconocido, se dice que es nulo. Un nulo no representa el valor cero (0) ni una cadena vacía (“”), porque estos son valores que tienen un significado o valor. El nulo significa ausencia de información, bien porque al insertar la fila se desconocía el valor del atributo, o tal vez porque para dicha fila el atributo no tiene valor. Debido a que los nulos no son valores, deben tratarse de forma particular, lo que causa problemas de implementación. Actualmente casi todos los SGDB soportan valores nulos.
              .col-lg-3.order-first.order-lg-last
                figure.mb-4.mb-lg-0
                  img.mx-auto(src="@/assets/curso/temas/107.svg",style="max-width: 72px;")
          div.ms-md-5(titulo="Integridad de entidad")
            .row.align-items-center
              .col-lg-9
                p.mb-0.ps-md-2 Ninguno de los atributos o columnas que componen una llave primaria debe ser NULO. Es decir, una clave primaria es irreducible para identificar de modo único una fila, el que sea irreducible significa que ningún subconjunto de la clave primaria sirve para identificar inequívocamente la dial: a la fila o tupla. Si se permitiera valor nulo en una columna que hace parte de la llave primaria, esta estaría contradiciendo la irreductibilidad de una llave primaria; esto no aplica para claves alternativas, solo para la clave primaria.
              .col-lg-3.order-first.order-lg-last
                figure.mb-4.mb-lg-0
                  img.mx-auto(src="@/assets/curso/temas/107.svg",style="max-width: 72px;")
          div.ms-md-5(titulo="Integridad referencia")
            .row.align-items-center
              .col-lg-9
                p.mb-0.ps-md-2 Para esto se debe analizar el modelo de la figura Modelo relacional y en particular, la relación entre las tablas persona y estudiante. Como se sabe, la tabla estudiante tiene una llave primaria que, a la vez, es una referencia de la tabla persona. 
              .col-lg-3.order-first.order-lg-last
                figure.mb-4.mb-lg-0
                  img.mx-auto(src="@/assets/curso/temas/107.svg",style="max-width: 72px;")
      .col-lg-5.order-first.order-lg-last(data-aos="fade-right")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/108.png",style="max-width: 505px;")

    .fondo-personalizado-4.mb-5(data-aos="zoom-in-up")
      .fondo-personalizado-4__contenido
        .row.align-items-center.pb-4
          .col-lg-8
            p.mb-0 En la siguiente figura, por cada estudiante (tabla estudiante) existe uno y solo un elemento en la tabla persona, de tal forma que un estudiante es la conjunción de ambas tablas por medio de la llave foránea (que a la vez es llave primaria) id_estudiante, pero ¿qué tal que no existiera? Eso significa que la base de datos es inconsistente o que tiene datos basura en la tabla estudiante. Afortunadamente los SGDB permiten definir reglas que impidan que esto ocurra en las tablas, es decir, que no permita registrar un estudiante con id_estudiante con un valor que no existe en la columna id_persona de la tabla persona.
          .col-lg-4.order-first.order-lg-last
            figure.mb-4.mb-lg-0
              img.mx-auto(src="@/assets/curso/temas/109.png",style="max-width: 505px;")

    .titulo-sexto.color-acento-contenido(data-aos="flip-up")
      p.mb-0 #[b Figura 24.] Error de integridad referencial
    figure.d-none.d-lg-block.mb-5
      img.mx-auto(src="@/assets/curso/temas/110.png",style="max-width: 1240px;",alt="La imagen presenta el error de integridad referencial.")

    .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
      .burbuja2.right(style="top: 19%;")
      .burbuja2(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4(data-aos="fade")
        figure
          img.mx-auto(src="@/assets/curso/temas/111.png",style="max-width: 483px;",alt="La imagen presenta el error de integridad referencial.")

    .row.justify-content-center.mb-5(data-aos="fade-left")
      .col-lg-8
        .fondo-color-sistema-k.borde-20.p-4.py-3
          .row.align-items-center
            .col-md-auto 
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/112.svg",style="max-width: 99px;")
            .col 
              p.mb-4.fw-bold Pregunta de análisis de datos
              p.mb-0 Ahora, hay que preguntarse lo siguiente: ¿qué pasaría si se borra el registro de la tabla persona que tiene id_persona con valor tres (3), sufrirá algún problema los datos de la tabla estudiante?, o ¿qué pasaría si se cambia el valor de tres (3) en la columna id_persona, por otro valor como por ejemplo nueve (9)?, antes de continuar, hay que tomarse unos minutos para pensarlo.

    .fondo-personalizado-4(data-aos="fade-right")
      .fondo-personalizado-4__contenido
        .row.align-items-center.pt-2
          .col-lg-7.mb-4.mb-lg-0
            p.mb-4.fw-bold Respuesta
            p.mb-4 La respuesta a las cuestiones planteadas es que en cualquiera de las operaciones de borrado o actualización del dato se incurrirá en una violación de la integridad referencial de la tabla estudiante, porque no habrá manera de conocer los datos complementarios del estudiante que se encuentran en la tabla persona.
            p.mb-0 Para evitar estos problemas de inconsistencia, los sistemas gestores de bases de datos permiten definir unas reglas cuando se borra o actualiza un dato que es referencia foránea de otra tabla.
          .col-lg-5
            figure
              img.mx-auto(src="@/assets/curso/temas/113.png",style="max-width: 505px;")

    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="fade-left")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Regla de borrado

    p.mb-3(data-aos="fade-left") Define el comportamiento a la pregunta: ¿qué ocurre si se intenta borrar la fila referenciada por la clave foránea de otra tabla? Para lo cual, el SGBD implementa una de las siguientes opciones:

    .fondo-personalizado-10.mb-5
      .fondo-personalizado-10__contenido.py-5(style="padding-bottom:7rem !important;")
        .row(data-aos="flip-up")
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/114.png",style="max-width: 89px;")
              h4.mb-4.text-center Restringir
              p.mb-0.text-center No se permite borrar la fila referenciada.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/114.png",style="max-width: 89px;")
              h4.mb-4.text-center Cascada
              p.mb-0.text-center Se borra la fila referenciada y también se borran las filas que la referencian, mediante la clave foránea en la otra tabla.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/114.png",style="max-width: 89px;")
              h4.mb-4.text-center Poner null
              p.mb-0.text-center Se borra la fila referenciada y las filas que la referenciaban ponen en nulo la clave foránea (solo si acepta nulos).
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/114.png",style="max-width: 89px;")
              h4.mb-4.text-center Valor por defecto
              p.mb-0.text-center Se borra la fila referenciada y las filas que la referenciaban ponen en la clave foránea el valor por defecto que defina la regla.

    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="fade")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Regla de edición

    p.mb-5(data-aos="zoom-in-up") Define el comportamiento a la pregunta: ¿qué sucede si se intenta modificar el valor de la clave primaria de la fila referenciada por la clave foránea por otra tabla? Para lo cual, el SGBD implementa una de las siguientes opciones:

    .row.mb-4(data-aos="flip-up")
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/115.png",style="max-width: 89px;")
              h4.mb-4.text-center Restringir
              p.mb-0.text-center No se permite editar la fila referenciada.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/115.png",style="max-width: 89px;")
              h4.mb-4.text-center Cascada
              p.mb-0.text-center Se actualiza la fila referenciada y también se actualiza las filas que la referencian mediante la clave foránea en la otra tabla.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/115.png",style="max-width: 89px;")
              h4.mb-4.text-center Poner null
              p.mb-0.text-center Se actualiza la fila referenciada y las filas que la referenciaban ponen a nulo la clave foránea (solo si acepta nulos).
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/115.png",style="max-width: 89px;")
              h4.mb-4.text-center Valor por defecto
              p.mb-0.text-center Se edita la fila referenciada y las filas que la referenciaban ponen en la clave foránea el valor por defecto que defina la regla.


    p.mb-4(data-aos="flip-up") De esta forma, una vez definida la estructura del modelo de datos, se debe determinar el comportamiento de estas operaciones, lo cual generalmente responde a requerimiento del sistema de información.

    Separador

    #t_3_4.titulo-segundo.color-acento-contenido(data-aos="fade-right")
      h2 3.4 Lenguajes de los sistemas administradores de bases de datos
    
    .fondo-personalizado-4(data-aos="zoom-in-up")
      .fondo-personalizado-4__contenido
        .row.align-items-center.py-4
          .col-lg-9
            p.mb-0 Los sistemas gestores de bases de datos, emplean un lenguaje que se denomina SQL que corresponde al nombre en inglés (#[em Structured Query Language]). Generalmente, cuando un SGBD relacional implementa el lenguaje SQL, todas las acciones, y operaciones se llevan a cabo en el sistema, mediante sentencias de este lenguaje. Dentro de SQL hay varios tipos de sentencias que se agrupan en cuatro conjuntos.
          .col-lg-3.order-first.order-lg-last
            figure.mb-4.mb-lg-0
              img.mx-auto(src="@/assets/curso/temas/117.png",style="max-width: 295px;")
    
    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="fade")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Sentencias de definición de datos (DDL)
    
    .row.align-items-center.mb-5(data-aos="fade-right")
      .col-lg-7
        .bloque-texto-b.bloque-texto-personalizado-2
          .bloque-texto-b__texto
            p.mb-0 Son las sentencias que permiten crear tablas, alterar su definición y eliminarlas. En una base de datos relacional existen otros tipos de objetos además de las tablas, como las vistas, los índices y los disparadores. Las sentencias para crear, alterar y eliminar vistas e índices también pertenecen a este conjunto de sentencia y se les denomina DDL del inglés #[em Data Definition Language].
      .col-lg-5.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/118.png",style="max-width: 505px;")

    .row.mb-5(data-aos="fade")
      .col-auto.d-none.d-lg-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 #[b Ejemplo DDL]
        p.mb-0 Para crear la tabla persona de la figura Modelo relacional, quedaría de la siguiente forma:
    
    .fondo-personalizado-burbuja(data-aos="fade-left")
      .burbuja.left(style="bottom: 0;")
      .fondo-personalizado-burbuja__contenido.pb-5
        .row.justify-content-center.pb-5
          .col-lg-4.col-md-8
            .bloque-codigo-personalizado
              .cabecera-bloque-codigo.p-4.py-3
                .bloque-codigo-circulos 
                  .bloque-codigo-circulo.c1
                  .bloque-codigo-circulo.c2
                  .bloque-codigo-circulo.c3
              .cuerpo-bloque-codigo.p-4
                code
                  | CREATE TABLE persona (
                  br
                  | id_persona INT NOT NULL,
                  br
                  | nombres VARCHAR(250) NOT NULL,
                  br
                  | apellidos VARCHAR(250) NOT NULL,
                  br
                  | correo VARCHAR(250) NOT NULL,
                  br
                  | PRIMARY KEY (id_persona)
                  br
                  |);

    .fondo-personalizado-burbuja(data-aos="fade-right")
      .burbuja.right(style="bottom: 0;")
      .fondo-personalizado-burbuja__contenido
        .row.justify-content-center.mb-5
          .col-lg-10
            .fondo-color-sistema-n.p-3.borde-10
              .row.align-items-center 
                .col-md-auto
                  figure.mb-4.mb-md-0
                    img.mx-auto(src="@/assets/curso/temas/36.svg",style="max-width: 86px;")
                .col
                  p.mb-0 Nota: cada atributo se define en una línea separada por una coma, se agregan restricciones de no nulidad (NOT NULL) al final la sentencia termina con punto y coma. Ahora, así se borraría esa misma tabla:
        
        .row.justify-content-center.mb-4
          .col-lg-3.col-md-5.col-sm-7
            .fondo-color-sistema-n.p-4.borde-10
              p.mb-0.text-center DROP TABLE persona;

        .cont-titulo-decorativo.p-2.mt-5.mb-5
          .row
            .col-auto.pe-0
              figure
                img(src="@/assets/curso/temas/img-titulo-dec.png")
            .col.align-self-end
              h3.mt-3.mb-0.me-2 Sentencias de manejo de datos (DML)

    p.mb-5(data-aos="fade") Estas sentencias que permiten insertar datos en las tablas, consultarlos, editarlos y borrarlos, se denomina DML del inglés #[em Data Manipulation Language].

    .row.mb-5(data-aos="flip-up")
      .col-auto.d-none.d-lg-block
        img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
      .col
        p.mb-0 #[b Ejemplo DML]
        p.mb-0 A continuación, se muestra cómo se inserta una fila a la tabla persona, luego cómo se actualiza la fila insertada y posteriormente cómo se borra:

    .fondo-personalizado-burbuja(data-aos="zoom-in-up")
      .burbuja.left(style="bottom: 0;")
      .fondo-personalizado-burbuja__contenido.pb-5
        .row.justify-content-center.mb-4
          .col-lg-4.col-md-8
            .bloque-codigo-personalizado
              .cabecera-bloque-codigo.p-4.py-3
                .bloque-codigo-circulos 
                  .bloque-codigo-circulo.c1
                  .bloque-codigo-circulo.c2
                  .bloque-codigo-circulo.c3
              .cuerpo-bloque-codigo.p-4
                code
                  | INSERT INTO persona (id_persona, nombres, apellidos, correo) VALUES (1, 'Ana lis', 'Mendez, 'ana@rmail.com');
        .row.justify-content-center.mb-4
          .col-lg-4.col-md-8
            .bloque-codigo-personalizado
              .cabecera-bloque-codigo.p-4.py-3
                .bloque-codigo-circulos 
                  .bloque-codigo-circulo.c1
                  .bloque-codigo-circulo.c2
                  .bloque-codigo-circulo.c3
              .cuerpo-bloque-codigo.p-4
                code
                  | UPDATE persona SET nombres = 'Ana Lis' WHERE id_persona = 1;
        .row.justify-content-center.mb-4
          .col-lg-4.col-md-8
            .bloque-codigo-personalizado
              .cabecera-bloque-codigo.p-4.py-3
                .bloque-codigo-circulos 
                  .bloque-codigo-circulo.c1
                  .bloque-codigo-circulo.c2
                  .bloque-codigo-circulo.c3
              .cuerpo-bloque-codigo.p-4
                code
                  | DELETE FROM persona WHERE id_persona = 1;
    

    .fondo-personalizado-burbuja(data-aos="fade-left")
      .burbuja.left(style="bottom: 0;")      
      .cont-titulo-decorativo.p-2.mt-1.mb-5
        .row
          .col-auto.pe-0
            figure
              img(src="@/assets/curso/temas/img-titulo-dec.png")
          .col.align-self-end
            h3.mt-3.mb-0.me-2 Sentencias de control (DCL)
      
      .row.mb-5 
        .col-lg-7
          p.mb-4 Son las sentencias empleadas por los administradores de la base de datos para realizar tareas como por ejemplo, crear usuarios y concederles o revocar los privilegios. Se usa el término DCL del inglés #[em Data Control Language].

          .row.mb-5
            .col-auto.d-none.d-lg-block
              img(src="@/assets/curso/temas/119.png",style="max-width: 85px;")
            .col
              .d-flex.flex-column.h-100.justify-content-between
                p.mb-0 #[b Ejemplo DCL]
                p.mb-0 En el ejemplo se le da permisos a un usuario llamado userdb de la base de datos de nombre biblioteca_db para que pueda insertar, actualizar, borrar y consultar datos de la tabla persona desde el mismo computador donde está instalada la base de datos (localhost).

        .col-lg-5
          figure.mb-4.mb-lg-0
            img.mx-auto(src="@/assets/curso/temas/120.png",style="max-width: 505px;")


      .fondo-personalizado-burbuja__contenido.pb-5(data-aos="fade-right")
        .row.justify-content-center.pb-5
          .col-lg-4.col-md-8
            .bloque-codigo-personalizado
              .cabecera-bloque-codigo.p-4.py-3
                .bloque-codigo-circulos 
                  .bloque-codigo-circulo.c1
                  .bloque-codigo-circulo.c2
                  .bloque-codigo-circulo.c3
              .cuerpo-bloque-codigo.p-4
                code
                  | GRANT INSERT, UPDATE, DELETE, SELECT ON biblioteca_db.persona TO userdb@'localhost';

    .cont-titulo-decorativo.p-2.mt-0.mb-5(data-aos="fade-left")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Sentencias de control de transacciones (TCL)
    p.mb-0 Un pequeño grupo de sentencias que permiten procesar en bloque operaciones DML, garantizando que se efectúen todas y cada una de las operaciones o ninguna. TCL del inglés #[em Transaction Control Language].


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
