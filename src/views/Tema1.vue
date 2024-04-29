<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span 1
      h1 Conceptos generales de base de datos

    .row.mb-4
      .col-lg-7.mb-4.mb-lg-0
        p.mb-4 Como concepto general de bases de datos podemos encontrar:

        .bloque-texto-b.bloque-texto-personalizado-1.p-5(data-aos="fade-left")
          .bloque-texto-b__texto
            i.fas.fa-quote-left
            h4.mb-0 El conjunto de datos organizado de tal modo que permita obtener con rapidez diversos tipos de información
            i.fas.fa-quote-right
          p.mb-0.position-relative (RAE, 2001).
      .col-lg-5
        figure
          img.mx-auto(src="@/assets/curso/temas/4.png",style="max-width: 505px;")
    
    .fondo-personalizado-3.mb-4
      .fondo-personalizado-3__contenido.py-4
        img.position-absolute(src="@/assets/curso/temas/9.png",style="max-width: 81px;bottom: 50px;right: 0;")
        .row.justify-content-center.py-5
          .col-lg-4.col-md-6.mb-4
            .fondo-color-primario.borde-10.p-4.h-100
              figure.mb-4
                img.mx-auto(src="@/assets/curso/temas/5.png",style="max-width: 108px;")
              p.mb-0.text-white De acuerdo con esta definición, una hoja de cálculo de Excel puede considerarse una base de datos, o un conjunto de archivos debidamente organizados, o la lista de nombres y teléfonos que está en nuestros #[em smartphones]. En principio, es correcto llamarle base de datos a estos ejemplos, sin embargo, en el contexto de desarrollo de #[em software], se referirá a ese conjunto de información que puede ser almacenada en grandes cantidades de forma organizada y es gestionada a través de un #[b Sistema de Gestión de Bases de Datos] (SGBD).
          .col-lg-4.col-md-6.mb-4
            .fondo-color-primario.borde-10.p-4.h-100
              figure.mb-4
                img.mx-auto(src="@/assets/curso/temas/7.png",style="max-width: 108px;")
              p.mb-0.text-white Para organizar y definir la información de forma sistemática, las bases de datos también deben poder almacenar una descripción precisa de los datos que contiene, conocida como #[b metadatos], a los que se le relaciona el tipo de información que es conceptualmente guardada (es decir, si se agrega una explicación de la naturaleza del dato en la empresa), se da origen a lo que conoce como #[b diccionario de datos o catálogo de datos].
          .col-lg-4.col-md-6.mb-4
            .fondo-color-sistema-j.borde-10.h-100.align-content-end
              figure
                img.mx-auto(src="@/assets/curso/temas/6.png",style="max-width: 389px;")

    .row.justify-content-center.mb-5
      .col-lg-10
        .fondo-color-sistema-k.p-3.ps-4.borde-10
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/10.png",style="max-width: 106px;")
            .col
              p.mb-4 #[b Ejemplo 1 - Determinar los metadatos del siguiente problema ]
              p.mb-0 Estos diseños están concebidos para emplear Sistemas de Gestión de Bases de Datos (en adelante SGDB), que es un sistema o servicio informático que permite a las personas definir, crear, dar soporte y mantenimiento a las bases de datos, controlando el acceso de forma segura.

    .row.justify-content-center.mb-4
      .col-lg-8
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 1.] Base de datos de llamadas telefónicas
        figure
          img.mx-auto(src="@/assets/curso/temas/11.svg",style="max-width: 820px;",alt="Base de datos de llamadas telefónicas.")

    .row.mb-4.align-items-center
      .col-lg-8
        p.mb-4 La figura muestra una tabla de datos que donde en cada columna se agrupa un tipo de dato particular, y cada fila es el conjunto de datos que se llama registro y comparten una relación (la relación es que cada fila corresponde a una única llamada telefónica); a esta estructura se le llama bidimensional, aquí filas y columnas son las dos dimensiones.

        p.mb-0.color-sistema-l Los metadatos de la figura anterior serían la definición de cada tipo de dato como se lista a continuación.
        p.mb-4.color-sistema-l #[b calldate]: tiene la estructura YYYY-MM-DD HH:MI:SS.Z, donde:

        .fondo-color-sistema-m.p-2.borde-12.mb-4
          ul.lista-ul.lista-personalizada-1
            li
              i.fas.fa-database
              span YYYY sería el año un dato numérico entero de cuatro dígitos.
            li
              i.fas.fa-database
              span MM el mes un dato numérico entero de dos dígitos entre 01 y 12.
            li
              i.fas.fa-database
              span DD un dato numérico entero de dos dígitos entre 01 y 31.
            li
              i.fas.fa-database
              span HH un dato numérico de dos dígitos entre 00 y 23.
            li
              i.fas.fa-database
              span MI y SS un dato numérico de dos dígitos entre 00 y 59.
            li
              i.fas.fa-database
              span Z un dato numérico de un digito (para representar milésimas de segundo).

        p.mb-0 Como este es el conjunto de datos de la primera columna, puede que use un término que describa lo anterior con una sola palabra que es TIMESTAMP, de esta forma esa primera columna puede quedar correctamente descrita como:
      .col-lg-4.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/12.png",style="max-width: 400px;")

    .row.justify-content-center.mb-5
      .col-lg-8
        .fondo-color-sistema-n.p-3.ps-4.borde-10
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/13.svg",style="max-width: 71px;")
            .col
              p.mb-0 #[b calldate TIMESTAMP(1)]  Donde 1 es el número de dígitos de milisegundos (Z).
    
    p.mb-5 src y dst: empleado para fuente de la llamada o llamante (src) y destino de la llamada (dst), puede ser un número telefónico o de extensión telefónica. Algunos tienen el código de país seguido del signo más, ejemplo: 57+3155008002. Por lo tanto, se puede describir como una cadena de texto que no superará los 25 caracteres, pero puede tener menos de 25 caracteres, así el metadato iría descrito:

    .row.align-items-center.mb-5
      .col-lg-7
        ul.lista-ul.lista-personalizada-1
          li
            i.fas.fa-database
            span #[b src VARCHAR(25)] De esta forma decimos que es una cadena de caracteres.
          li
            i.fas.fa-database
            span #[b dst VARCHAR(25)]  Que varía en longitud de 0 a 25 caracteres.
          li
            i.fas.fa-database
            span #[b duration] Tiene la estructura HH:MI:SS y como se vio antes, representa el tiempo en horas, minutos y segundos: src TIME TIME se usa para esta estructura de dato en particular.
          li
            i.fas.fa-database
            span #[b disposition] Indica si la llamada es atendida ANSWER, no atendida NO ANSWER, o si falló la FAIL. Se puede representar con una cadena de 10 caracteres.

      .col-lg-5.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/14.png",style="max-width: 502px;")

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
              | calldate TIMESTAM(1),
              br
              | src VARCHAR(25),
              br
              | dst VARCHAR(25),
              br
              | src TIME,
              br
              | disposition VARCHAR(10)

    p.mb-5 Note que cada uno de ellos fue separado por una coma, para que se diferencie de los demás.

    .row.justify-content-center.mb-5
      .col-lg-8
        .fondo-color-sistema-k.p-3.ps-4.borde-20
          .row.align-items-center
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/15.svg",style="max-width: 108px;")
            .col
              p.mb-4 #[b Ejemplo 2]
              p.mb-0 Conociendo el objetivo de la base de datos y los metadatos de la figura anterior, crear un diccionario de datos o un catálogo de datos.
              p.mb-0 Solución:

    .titulo-sexto.color-acento-contenido
      p.mb-0 #[b Tabla 1.] Diccionario de datos
    
    .tabla-a.tabla-personalizada-1.mb-4.tam-1
      table
        thead
          tr
            th.text-start Nombre
            th(colspan="3").text-start Diccionario de datos base de llamadas telefónicas
        tbody
          tr
            td Creación
            td(colspan="3") 27/02/2021
          tr
            td Descripción
            td(colspan="3",style="min-width: 300px;") Registro de las llamadas telefónicas de la PBX de la empresa STD LTDA.
          tr
            td Campo
            td #[b Tipo dato]
            td #[b Tamaño]
            td #[b Descripción]
          tr
            td calldate
            td TIMESTAMP
            td 1
            td Representa el momento exacto en que entra o sale la llamada.
          tr
            td src
            td VARCHAR
            td 25
            td Fuente (#[em source]) de la llamada, número de quien hace la llamada telefónica.
          tr
            td dst
            td VARCHAR
            td 25
            td Número del destino de la llamada telefónica.
          tr
            td duration
            td TIME
            td 0
            td Duración de la llamada telefónica.
          tr
            td disposition
            td VARCHAR
            td 10
            td Estado final en que se considera quedó la llamada.

    .row.mb-4
      .col-lg-7.mb-4.mb-lg-0
        p.mb-0 Como se puede notar en la tabla anterior, un diccionario de datos aporta información de la estructura de los datos y el uso que se da a cada dato en la empresa, organización o sistema de información, pero no sin antes darle un nombre a todo el conjunto de datos (primera fila), una fecha (segunda fila) y una descripción (tercera fila) del conjunto de los datos. En la tabla se puede identificar la independencia que existe entre la lógica de los datos (representado por la columna DESCRIPCIÓN del dato) y el almacenamiento físico (estructura de almacenamiento representado por las columnas TIPO DE DATO y TAMAÑO).
      .col-lg-5
        figure
          img.mx-auto(src="@/assets/curso/temas/16.png",style="max-width: 505px;")
    
    Separador

    #t_1_1.titulo-segundo.color-acento-contenido
      h2 1.1 Tipos de datos y restricción de no nulidad

    p.mb-5 Existen muchos tipos de datos y varían según el SGDB, porque cada sistema gestor define sus propios tipos de datos, aunque existen las equivalencias notables y otras no tan notables. A continuación, se presenta una tabla que relaciona el tipo de datos según los SGDB más comunes del mercado, como ORACLE, PostgeSQL, MySQL y SQLServer.

    .row.justify-content-center.mb-5
      .col-lg-9
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Tabla 2.] Tipos de datos según bases de datos
        
        .tabla-a.tabla-personalizada-1
          table
            thead
              tr
                th.text-start Tipo de dato
                th.text-start ORACLE
                th.text-start PostgreSQL
                th.text-start MySQL
                th.text-start SQLServer
                
            tbody
              tr
                td Cadena caracteres
                td VARCHAR2
                td CHARACTER VARYING
                td VARCHAR
                td VARCHAR
              tr
                td Cadena texto
                td TEXT
                td TEXT
                td TEXT
                td NTEXT
              tr
                td Entero pequeño
                td SMALLINT
                td SMALLINT
                td SMALLINT
                td SMALLINT
              tr
                td Entero
                td INTEGER
                td INTEGER
                td INT
                td INT
              tr
                td Fecha
                td DATE
                td DATE
                td DATE
                td DATE
              tr
                td Fecha y hora
                td DATE
                td TIMESTAMP WITH TIME ZONE
                td DATETIME
                td DATETIME2
              tr
                td Hora
                td DATE
                td TIME
                td TIME
                td TIME
              tr
                td Entero con decimales
                td FLOAT
                td REAL
                td FLOAT
                td FLOAT

    .row.mb-5 
      .col-lg-7.mb-4.mb-lg-0
        p.mb-0 Según el tipo de sistema gestor de bases de datos, cada uno define sus tipos de datos que, de alguna forma, son muy parecidos entre ellos, o existen equivalencias; las diferencias son pocas y están relacionadas con aspectos técnicos del almacenamiento. Se pueden consultar más detalles de cada uno de ellos en los sitios oficiales de cada motor de base de datos:
      .col-lg-5
        figure
          img.mx-auto(src="@/assets/curso/temas/17.png",style="max-width: 502px;")

    .fondo-personalizado-burbuja
      .burbuja.right(style="bottom: 33%;")
      .fondo-personalizado-burbuja__contenido
        .row.justify-content-center.mb-5
          .col-lg-10
            .tabla-a.tabla-personalizada-1.tam-1
              table
                thead
                  tr
                    th.text-start Nombre
                    th.text-start Enlace de acceso
                    
                tbody
                  tr
                    td ORACLE
                    td https://docs.oracle.com/cd/E11882_01/server.112/e41085/sqlqr06002.htm#SQLQR959
                  tr
                    td PostgreSQL
                    td https://www.postgresql.org/docs/13/datatype.html#DATATYPE-TABLE
                  tr
                    td MySQL
                    td https://dev.mysql.com/doc/refman/8.0/en/data-types.html
                  tr
                    td SQLServer
                    td https://docs.microsoft.com/en-us/sql/t-sql/data-types/data-types-transact-sql?view=sql-server-ver15
          
        .row.align-items-center.mb-4
          .col-auto.d-none.d-sm-block
            img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
          .col
            p.mb-0 Existen varios tipos de restricciones, por ahora se verá la restricción de longitud, por ejemplo:
        
        .row.justify-content-center.mb-4
          .col-lg-3.col-md-5.col-sm-7
            .fondo-color-sistema-n.p-4.borde-10
              p.mb-0.text-center src VARCHAR(25)
        
        .row.align-items-center.mb-5
          .col-lg-7
            p.mb-0 En él se define que el src, es una columna que no puede exceder los 25 caracteres. De la misma forma, existe una forma de definir que es obligatoria: registrar un dato en esa columna y se llama #[b restricción de no nulidad], es decir, que ninguna fila puede tener valor nulo. Así, en el ejemplo de la base de datos de llamadas telefónicas, si se define que todo y cada uno de los datos son obligatorios (usando las palabras #[b NOT NULL]), la metadata que define la estructura de los datos, quedaría así:
          .col-lg-5.order-first.order-lg-last
            figure.mb-4.mb-lg-0
              img.mx-auto(src="@/assets/curso/temas/19.png",style="max-width: 505px;")
        
        .row.justify-content-center
          .col-lg-4.col-md-8
            .bloque-codigo-personalizado
              .cabecera-bloque-codigo.p-4.py-3
                .bloque-codigo-circulos 
                  .bloque-codigo-circulo.c1
                  .bloque-codigo-circulo.c2
                  .bloque-codigo-circulo.c3
              .cuerpo-bloque-codigo.p-4
                code
                  | calldate TIMESTAM(1) NOT NULL,
                  br
                  | src VARCHAR(25)NOT NULL,
                  br
                  | dst VARCHAR(25)NOT NULL,
                  br
                  | src TIME NOT NULL,
                  br
                  | disposition VARCHAR(10) NOT NULL
        


        
      
</template>

<script>
export default {
  name: 'Tema1',
  components: {},
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
