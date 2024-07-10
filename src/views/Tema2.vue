<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="flip-up")
      .titulo-principal__numero
        span 2
      h1 Modelo entidad relación
    
    .row.mb-5
      .col-lg-7(data-aos="fade-right")
        p.mb-0 Las bases de datos relacionales, inicialmente no son fáciles de modelar, por lo que se requiere de cierto nivel de abstracción, es decir, se va ocultando la complejidad del diseño de la base de datos, primero analizando el requerimiento desde un punto de vista conceptual, entendido como las necesidades de la empresa o del sistema de información, luego se va analizando desde el punto de vista de la lógica de los datos y, finalmente, se analiza físicamente cómo se almacenarán los datos. A continuación,  se presentan algunos conceptos:
      .col-lg-5.order-first.order-lg-last(data-aos="fade-left")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/25.png",style="max-width: 503px;")

    
    .row.mb-5 
      .col-lg-5(data-aos="fade-left")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/26.png",style="max-width: 505px;")
      .col-lg-7(data-aos="fade-right")
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

    p.mb-5(data-aos="fade") Se presentará más claro en un diagrama, pero antes se deben considerar los siguientes elementos:

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
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4(data-aos="zoom-in-out")
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/32.png",style="max-width: 1029px;",alt="Imagen que representa la entidad relación persona cuenta bancaria.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/33.png",style="max-width: 458px;",alt="Imagen que representa la entidad relación persona cuenta bancaria.")

    .row.mb-5
      .col-lg-7.mb-4.mb-lg-0(data-aos="fade-right")
        p.mb-4 Para una base de datos de un sistema bancario consistente en clientes (es decir personas) y sus cuentas bancarias, en la figura anterior se muestra el diagrama Entidad Relación. En ellos se indica que hay dos entidades que son persona y cuenta, con los atributos descritos anteriormente para cada una. El diagrama también representa la relación titular entre persona y cuenta.
        .row.mb-5
          .col-auto.d-none.d-md-block
            img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
          .col
            p.mb-0 Se debe tener en cuenta que el modelo relacional convierte las entidades en tablas, por lo tanto, se puede poner como ejemplo que las entidades personas se conviertan en tablas, como muestra la siguiente figura.
      .col-lg-5(data-aos="fade-left")
        figure
          img.mx-auto(src="@/assets/curso/temas/34.png",style="max-width: 505px;")

    .row.justify-content-center.mb-5
      .col-lg-8
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 3.] Tablas de una entidad relación
        figure(data-aos="fade")
          img.mx-auto(src="@/assets/curso/temas/35.png",style="max-width: 820px;",alt="Imagen que presenta las tablas de una entidad relación.")
    
    .row.justify-content-center.mb-5(data-aos="fade-left")
      .col-lg-10
        .fondo-color-sistema-n.p-3.ps-4.borde-10
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/36.svg",style="max-width: 86px;")
            .col
              p.mb-0 Las tablas de la figura anterior muestran cada uno de los conjuntos de registros, la “tabla persona” muestra 6 registros y la “tabla cuenta” muestra 9 de ellas; cada uno de estos registros representa un objeto, es decir, de la tabla persona hay 6 (objetos) o personas. A la agrupación de los datos de cada registro se le llama TUPLA y, en términos sencillos, una TUPLA de una base de datos, es el conjunto de todos los atributos (columnas) de una fila.

    Separador

    #t_2_1.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 2.1 Relaciones entre entidades

    .fondo-personalizado-4.mb-5
      .fondo-personalizado-4__contenido 
        .row.align-items-center.p-4
          .col-lg-7.mb-4.mb-lg-0(data-aos="fade-up")
            p.mb-0 Como se observa en las figuras anteriores, una entidad se puede representar con una tabla, sin embargo, la relación titular aún no se sabe cómo representarla y para ello se debe definir algunas propiedades de los atributos.
          .col-lg-5(data-aos="fade-down")
            figure
              img.mx-auto(src="@/assets/curso/temas/37.png",style="max-width: 502px;")
    
    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="fade")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Principio de unicidad
    
    p.mb-4(data-aos="fade") En una tabla nunca deben existir TUPLAS repetidas, es decir, no debe haber más de una fila con exactamente los mismos valores en cada columna que otra fila de la misma tabla. En otras palabras, cada fila debe diferir al menos en un elemento (columna) en relación con las demás.

    .row 
      .col-lg-7.mb-4.mb-lg-0(data-aos="fade-right")
        .fondo-color-sistema-n.borde-10.p-4
          p.mb-0 En una base de datos relacional, las relaciones permiten evitar datos redundantes. En el ejemplo anterior, una persona puede tener varias cuentas bancarias, pero no es deseable que, por cada una de las cuentas bancarias asociadas a la misma persona, se deban repetir los datos de la misma persona, sino más bien, se debe encontrar un mecanismo para relacionar la información de las dos tablas y para ello se introducen algunos conceptos útiles.
      .col-lg-5(data-aos="fade-left")
        figure
          img.mx-auto(src="@/assets/curso/temas/38.png",style="max-width: 502px;")

    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="fade")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Claves

    .fondo-personalizado-burbuja
      .burbuja.left(style="bottom: 0;")
      .fondo-personalizado-burbuja__contenido
        .row.mb-5(data-aos="flip-up")
          .col-auto.d-none.d-md-block
            img(src="@/assets/curso/temas/18.svg",style="max-width: 85px;")
          .col
            p.mb-0 Dado que en una tabla no hay filas repetidas, se pueden distinguir unas de otras, es decir, se pueden identificar de manera única (por el principio de unidad). Por lo tanto, la manera de identificarlas inequívocamente es según los valores de los atributos. De esta forma, se conoce como claves a los atributos que sirven para identificar un registro de forma inequívoca.

        .row.justify-content-center.mb-5
          .col-lg-8
            .fondo-color-sistema-k.p-3.ps-4.borde-20(data-aos="flip-down")
              .row.align-items-center 
                .col-md-auto
                  figure.mb-4.mb-md-0
                    img.mx-auto(src="@/assets/curso/temas/39.svg",style="max-width: 110px;")
                .col
                  p.mb-4 #[b Ejemplo]
                  p.mb-0 En la tabla persona de la figura 3, es sabido por todos que no existen dos personas con el mismo número de documento de identidad, por lo tanto, se puede emplear el atributo identificación como clave de la tabla persona. Así mismo, no deben existir dos cuentas bancarias con el mismo número de cuenta, entonces, el atributo numero_cuenta se puede emplear como clave de la tabla cuenta. Esto se puede presentar en un diagrama de entidad relación cuando a los atributos que componen una clave, se les marca con subrayado el nombre del atributo, tal como se muestra en la siguiente figura.

    .titulo-sexto.color-acento-contenido
      p.mb-0 #[b Figura 4.] Claves de las entidades persona y cuenta
    
    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-5(style="overflow: hidden;",data-aos="fade")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/40.svg",style="max-width: 1029px;",alt="Imagen que representa las claves de las entidades persona y cuenta.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/41.svg",style="max-width: 1029px;",alt="Imagen que representa las claves de las entidades persona y cuenta.")
    
    p.mb-0(data-aos="fade") Nótese como los atributos #[b identificación y numero_cuenta] tiene subrayada la palabra identificadora del atributo, representado así que ese atributo es la clave (que hace que se cumpla el criterio de unicidad) de su entidad.
    
    .cont-titulo-decorativo.p-2.mt-5.mb-5(data-aos="flip-up")
      .row
        .col-auto.pe-0
          figure
            img(src="@/assets/curso/temas/img-titulo-dec.png")
        .col.align-self-end
          h3.mt-3.mb-0.me-2 Claves candidata, superclave y clave primaria
    
    .row.mb-5(data-aos="flip-up")
      .col-lg-7
        p.mb-4 Supongamos el caso que el banco es internacional, que es un banco moderno y solo diseñado para transacciones vía internet o virtuales, por lo tanto, el correo del cliente (persona) es necesario y obligatorio.
        p.mb-4 En este caso, ocurren un par de asuntos a analizar: al ser internacional el banco, puede existir un cliente en un país con el mismo número de identificación de otro cliente en otro país, por lo tanto, el atributo #[b identificación] ya no puede ser una clave de la entidad, sin embargo, es importante y obligatorio saber a qué país corresponde cada cliente, el conjunto de datos #[b identificación y país] y si ambos cumplen con el criterio de unidad, porque no existen dos personas en el mismo país con el mismo número de identificación.
        .fondo-color-sistema-n.p-4.borde-10
          p.mb-4 #[b Clave compuesta:] si se escogiera el conjunto de atributos, #[b identificación y país] como clave de la entidad, se está haciendo una clave compuesta, porque es un conjunto de más de un atributo el que se usa para este fin.
          p.mb-0 #[b Clave compuesta:] el otro asunto a considerar es que se puede emplear el correo electrónico como clave, porque no existen dos usuarios con el mismo #[b correo] electrónico, esto es válido si se definió como regla del banco que cada cliente tenga su correo electrónico diferente de los demás. Estos dos casos se representan en la siguiente figura.
      .col-lg-5.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/42.png",style="max-width: 505px;")

    .row.justify-content-center
      .col-lg-8
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 5.] Claves candidata
    
    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-5(style="overflow: hidden;")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/43.svg",style="max-width: 1029px;",alt="Imagen que presenta claves candidata.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/44.svg",style="max-width: 1029px;",alt="Imagen que presenta claves candidata.")
    
    .row.justify-content-center.mb-5(data-aos="fade-right")
      .col-lg-8
        .fondo-personalizado-1.borde-12.p-3
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/45.png",style="max-width: 88px;")
            .col
              p.mb-0.text-white #[b Clave candidata:] los dos caminos propuestos en la figura anterior son válidos, y se denominan claves candidatas porque con ambas se puede lograr el principio de unicidad, y es potestad de cada diseñador o analista de sistemas, determinar cuál de las dos emplear.
    
    .row.mb-5
      .col-lg-7(data-aos="fade-down")
        p.mb-0 Sin embargo, existe otro tipo de solución y es asignarle un atributo identificador a la entidad persona que se encargue exclusivamente de identificar inequívocamente cada tupla o fila, a este atributo se le puede llamar id_persona que sería un número que el programa o #[em software] para el que se está desarrollando la base, le asignará a cada cliente cada vez que se registren por primera vez, los datos de una persona (generalmente una secuencia). De esta forma, se tendrían 3 claves candidatas; la siguiente figura presenta cómo sería la entidad y la tabla que representa.
      .col-lg-5.order-first.order-lg-last(data-aos="fade-up")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/46.png",style="max-width: 505px;")
    
    .titulo-sexto.color-acento-contenido
      p.mb-0 #[b Figura 6.] Claves candidatas secuencia

    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-4(style="overflow: hidden;")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4(data-aos="fade")
        figure
          img.mx-auto(src="@/assets/curso/temas/47.svg",style="max-width: 610px;",alt="Imagen que representa las claves candidatas secuencia.")

    p.mb-5(data-aos="fade-right") Este último enfoque es el más empleado y recomendado por los diseñadores o analistas de #[em software], pues reduce, significativamente, la complejidad del diseño y facilita la relación con otras tablas o entidades. Por lo tanto, se usará cada vez que se tenga oportunidad de hacerlo.


    .container.tarjeta.tarjeta--blanca
      .tarjeta--container.row.mb-5
        .col-md.tarjeta.fondo-color-sistema-q.p-5(data-aos="fade-right")
          .row.justify-content-center.mb-4
            .col-6
              figure
                img.mx-auto(src='@/assets/curso/temas/48.png',style="max-width: 153px;")
            
          h2.text-center.mb-4.text-white Superclave
          p.text-white Es un conjunto de uno o más atributos que, tomados juntos, permiten identificar de forma única una entidad en el conjunto de entidades. Por ejemplo, el atributo id_persona del conjunto de entidades persona, es suficiente para distinguir una persona cliente del banco de las otras. Así, id_persona es una superclave. Análogamente, la combinación de identificación y país es una superclave del conjunto de entidades persona. El atributo correo de persona es otra superclave, pero el atributo nombres no lo es, porque varias personas podrían tener el mismo nombre.

        .col-md.tarjeta.color-primario.text-white.p-5(data-aos="fade-left")
          .row.justify-content-center.mb-4
            .col-6
              figure
                img.mx-auto(src='@/assets/curso/temas/48.png',style="max-width: 153px;")
            
          h2.text-center Clave primaria
          p Se emplea el término clave primaria para nombrar una clave candidata que es elegida por el diseñador o analista de la base de datos como clave principal para identificar las tuplas dentro de una entidad. Una clave (primaria, candidata y superclave) es una propiedad del conjunto de entidades, más que de las entidades individuales. Dos tuplas individuales en el conjunto, no pueden tener el mismo valor en sus atributos clave primaria al mismo tiempo. La designación de una clave primaria es en sí una restricción que modela una característica del mundo real.
    
    Separador

    .fondo-personalizado-5.mb-5
      .fondo-personalizado-5__contenido
        #t_2_2.titulo-segundo.color-acento-contenido(data-aos="flip-up")
          h2 2.2 Relaciones de uno a muchos
        .row.pb-5
          .col-lg-7(data-aos="fade-down")
            p.mb-4 Una relación de uno a varios o de uno a muchos, es el tipo de relación más empleada. En este tipo de relación, una fila de la tabla A puede tener muchas filas coincidentes en la tabla B. Pero una fila de la tabla B solo puede tener una fila coincidente en la tabla A. Por ejemplo, las tablas persona y cuenta tienen una relación de uno a muchos. Es decir, cada persona puede tener más de una cuenta, pero, por ejemplo, cada título proviene de una sola editorial.

            .fondo-color-sistema-n.p-3.borde-10
              .row.align-items-center 
                .col-md-auto
                  figure.mb-4.mb-md-0
                    img.mx-auto(src="@/assets/curso/temas/36.svg",style="max-width: 86px;")
                .col
                  p.mb-0 En un diagrama de entidad relación esto se representa con lo que se denomina multiplicidad, como se presenta en la siguiente figura.
          .col-lg-5.order-first.order-lg-last(data-aos="fade-up")
            figure.mb-4.mb-lg-0
              img.mx-auto(src="@/assets/curso/temas/50.png",style="max-width: 505px;")
    
    .titulo-sexto.color-acento-contenido(data-aos="fade")
      p.mb-0 #[b Figura 7.] Relaciones de uno a muchos

    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-5(style="overflow: hidden;",data-aos="flip-up")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/51.svg",style="max-width: 1030px;",alt="Imagen que presenta las relaciones de uno a muchos.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/52.svg",style="max-width: 460px;",alt="Imagen que presenta las relaciones de uno a muchos.")

    .row.justify-content-center.mb-5(data-aos="zoom-in-out")
      .col-lg-8
        .fondo-personalizado-1.borde-12.p-3
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/53.png",style="max-width: 86px;")
            .col
              p.mb-0.text-white A esta representación se le denomina multiplicidad #[b 1:N] y se lee de la siguiente forma: #[b UNA persona] es titular de #[b N] cuentas bancarias, de esta forma una persona puede tener N (que puede ser cero, uno o más de una) cuentas bancarias. Se puede leer en forma inversa que el resultado es el mismo: muchas o varias cuentas bancarias pueden tener un mismo titular.
    
    p.mb-5(data-aos="zoom-in-out") Cuando una relación es de uno a muchos y se mapea un modelo de base de datos relacional, la relación #[b titular] (rombo) se termina convirtiendo una columna de la tabla de los muchos.

    .row.justify-content-center.mb-5(data-aos="fade")
      .col-lg-8
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 8.] Tablas de un modelo relacional 1:N
        figure.mb-5
          img.mx-auto(src="@/assets/curso/temas/54.png",style="max-width: 820px;",alt="Imagen que presenta las tablas de un modelo relacional 1:N.")
        .fondo-personalizado-1.borde-12.p-3
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/53.png",style="max-width: 86px;")
            .col
              p.mb-0.text-white Como se puede ver en la figura anterior, Ana Lis Méndez, es titular de dos cuentas bancarias (67.789.901 y 32.443.171), y todos los datos de la columna titular en la tabla cuenta se conoce como #[b LLAVE FORÁNEA] de la tabla persona.
    
    .row.mb-5(data-aos="flip-up")
      .col-lg-7
        .fondo-color-sistema-n.borde-10.p-4.h-100.d-flex.align-items-center
          p.mb-0 #[b REGLA DE MAPEO 1:N de Modelo entidad-relación a modelo relacional:] una relación de uno a muchos (1:N), se transforma en una columna en la tabla que tiene la multiplicidad de los muchos (cuenta). Y todos los datos de esta columna existen como llave primaria en la tabla que tiene la multiplicidad uno (tabla persona).
      .col-lg-5.order-first.order-lg-last
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/55.png",style="max-width: 502px;")

    .row.justify-content-center.mb-5(data-aos="zoom-in-out")
      .col-lg-6.col-md-9
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 9.] Diagrama relacional 1:N
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/56.png",style="max-width: 610px;",alt="Imagen que presenta un diagrama relacional 1:N.")

        .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
          .burbuja2.right(style="top: 19%;")
          .burbuja2(style="bottom: -100px;left: 40px;")
          .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
            figure
              img.mx-auto(src="@/assets/curso/temas/57.png",style="max-width: 286px;",alt="Imagen que presenta un diagrama relacional 1:N.")
    
    .row.mb-5
      .col-lg-7.mb-4.mb-lg-0(data-aos="fade")
        p.mb-4 En la figura se puede ver el nombre de las entidades (persona y cuenta), los atributos haciendo especial énfasis en los que representan la llave primaria con el indicador PK (del inglés #[em Primary Key]), y también se observa la relación titular (columna de la tabla), indicando que es una clave o llave foránea de la tabla persona, lo que se indica con el indicador FK (del inglés #[em Foreign Key]).
        p.mb-0 Algunos diagramas relacionales agregan metadatos para hacer más claro el modelo al diseñador, así como la naturaleza de los datos del modelo.
      .col-lg-5(data-aos="fade-left")
        figure
          img.mx-auto(src="@/assets/curso/temas/58.png",style="max-width: 502px;")
    
    .row.justify-content-center.mb-5
      .col-lg-6.col-md-9
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 10.] Diagrama relacional 1:N con metadatos
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/59.png",style="max-width: 610px;",alt="Imagen que presenta el diagrama relacional 1:N con metadatos.")

        .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
          .burbuja2.right(style="top: 19%;")
          .burbuja2(style="bottom: -100px;left: 40px;")
          .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
            figure
              img.mx-auto(src="@/assets/curso/temas/60.png",style="max-width: 331px;",alt="Imagen que presenta el diagrama relacional 1:N con metadatos.")

    .row.justify-content-center.mb-4
      .col-lg-8
        .fondo-personalizado-1.borde-12.p-3
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/61.png",style="max-width: 86px;")
            .col
              p.mb-0.text-white #[b Conclusión:] la relación de uno a muchos se termina convirtiendo en una columna en la tabla que tiene la multiplicidad de los muchos.

    Separador

    #t_2_3.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 2.3 Relación de muchos a muchos

    .row.mb-5
      .col-lg-7(data-aos="flip-right")
        p.mb-0 En una relación de muchos a muchos, una fila de la tabla A puede tener relación con muchas filas en la tabla B y también, en sentido contrario, una fila de la tabla B con respecto de varias filas de la tabla A. Esta relación se crea definiendo una tercera tabla denominada tabla de relación. Esta nueva tabla tiene una clave principal de la tabla compuesta de las claves foráneas de la tabla A y de la B.
      .col-lg-5.order-first.order-lg-last(data-aos="flip-left")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/62.png",style="max-width: 502px;")
    
    .row.justify-content-center.mb-5(data-aos="flip-up")
      .col-lg-8
        .fondo-color-sistema-k.p-3.ps-4.borde-20
          .row.align-items-center 
            .col-md-auto
              figure.mb-4.mb-md-0
                img.mx-auto(src="@/assets/curso/temas/63.svg",style="max-width: 112px;")
            .col
              p.mb-4 #[b Ejemplo]
              p.mb-4 Se necesita almacenar la información de unas referencias bibliográficas o publicaciones de libros, tesis, artículos, que escriben los estudiantes de una universidad, y como se sabe, un libro, tesis, artículo o cualquier publicación puede ser elaborada por más de una persona, y a su vez, una persona (docente, estudiante o investigador) puede tener más de una publicación de su autoría.
              p.mb-0 Como se observa en la siguiente figura, la entidad publicación tiene una llave primaria llamada identificación, y existe una relaciona llamada #[b autor], y representa que una persona puede ser autor de una o muchas publicaciones, y que una publicación puede ser de autoría de una o muchas personas, la multiplicidad en este caso es de muchos a muchos y se representa como N:N.
    
    .titulo-sexto.color-acento-contenido(data-aos="flip-up")
      p.mb-0 #[b Figura 11.] Diagrama de entidad de publicaciones bibliográficas

    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-5.borde-lg-10(style="overflow: hidden;",data-aos="zoom-in-out")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/64.png",style="max-width: 1030px;",alt="Imagen que presenta un diagrama de entidad de publicaciones bibliográficas.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/65.png",style="max-width: 451px;",alt="Imagen que presenta un diagrama de entidad de publicaciones bibliográficas.")
    
    .row.mb-4(data-aos="flip-up")
      .col-lg-7.mb-4.mb-lg-0
        .borde-10.fondo-color-sistema-n.p-4.h-100.d-flex.align-items-center
          p.mb-0 #[b REGLA DE MAPEO N:N de modelo entidad-relación a modelo relacional:] en una relación de muchos a muchos (N:N) se transforma en una tabla, cuya llave primaria está compuesta por las llaves primarias de las otras dos tablas.
      .col-lg-5
        figure
          img.mx-auto(src="@/assets/curso/temas/66.png",style="max-width: 502px;")

    p.mb-5(data-aos="fade") Como se puede ver en la siguiente figura, la “tabla autor”, dice que la persona Ana Lis, es autora de los libros de título Grandes hazañas y Pellentesque, también que el libro Pellentesque es escrito además de Ana Lis por Luis Darío y Jose Nicolás. Lo anterior haciendo referencia a las llaves primarias de las tablas a) persona y b) publicación.

    .row.justify-content-center.mb-5(data-aos="fade")
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 12.] Tablas de relación N:N
        figure
          img.mx-auto(src="@/assets/curso/temas/67.png",style="max-width: 1030px;",alt="Imagen que presenta las tablas de relación N:N.")

    .row.align-items-center.mb-5
      .col-lg-8.mb-4.mb-lg-0
        p.mb-0(data-aos="fade") La representación de la relación N:N con un diagrama relacional se muestra en la figura a continuación, donde se usan los prefijos #[b FK1] y #[b FK2], para indicar llave foránea uno y dos, para las entidades persona y publicación 2, respectivamente. También se puede ver el prefijo #[b UK] (#[em Unique Key]) en la tabla publicación, en la columna ISBN, el cual significa que en toda la tabla publicación no puede existir más de una fila con el mismo ISBN, es decir, nunca ninguna publicación tendrá el mismo ISBN que otra.
      .col-lg-4(data-aos="zoom-in-out")
        figure
          img.mx-auto(src="@/assets/curso/temas/68.png",style="max-width: 403px;")

    .row.justify-content-center.mb-4
      .col-lg-10
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 13.] Diagrama relacional N:N
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/69.png",style="max-width: 1028px;",alt="Imagen que presenta el diagrama relacional N:N.")

        .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
          .burbuja2.right(style="top: 19%;")
          .burbuja2(style="bottom: -100px;left: 40px;")
          .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
            figure
              img.mx-auto(src="@/assets/curso/temas/70.png",style="max-width: 331px;",alt="Imagen que presenta el diagrama relacional N:N.")
    
    Separador

    #t_2_4.titulo-segundo.color-acento-contenido(data-aos="flip-up")
      h2 2.4 Relaciones de uno a uno
    
    .row.mb-5
      .col-lg-7
        p.mb-0 En una relación uno a uno, una fila de la tabla A solo puede tener una fila coincidente en la tabla B y viceversa. Se crea, entonces, una relación uno a uno si ambas columnas relacionadas son claves principales o tienen restricciones únicas. Este tipo de relación no es común, porque la mayoría de la información que está relacionada de esta manera estaría en una tabla. Se puede usar una relación uno a uno por alguno de estos motivos:
      .col-lg-5.order-first.order-lg-last(data-aos="zoom-in-out")
        figure.mb-4.mb-lg-0
          img.mx-auto(src="@/assets/curso/temas/71.png",style="max-width: 502px;")

    .fondo-personalizado-10.mb-5
      .fondo-personalizado-10__contenido.py-5
        .row(data-aos="flip-up")
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/72.png",style="max-width: 89px;")
              p.mb-0.text-center Dividir una tabla con muchas columnas.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/72.png",style="max-width: 89px;")
              p.mb-0.text-center Aislar parte de una tabla por motivos de seguridad.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/72.png",style="max-width: 89px;")
              p.mb-0.text-center Almacenar datos de corta duración y que podrían eliminarse fácilmente, borrando la tabla periódicamente.
          .col-lg-3.col-md-6.mb-4
            .fondo-personalizado-9.pos-1.px-4.pb-5.h-100
              .d-flex
                .fondo-color-sistema-m.p-4.borde-23.mb-5.mx-auto.d-inline-block
                  figure
                    img.mx-auto(src="@/assets/curso/temas/72.png",style="max-width: 89px;")
              p.mb-0.text-center Almacenar información que solo se aplique a un subconjunto de la tabla principal.


    p.mb-5(data-aos="fade") Volviendo al ejemplo del banco, esta vez se supone que la empresa necesita información sobre sus empleados lo que, a la vez, pueden ser clientes del banco.

    .titulo-sexto.color-acento-contenido
      p.mb-0 #[b Figura 14.] Diagrama entidad relación persona-empleado

    .fondo-personalizado-burbuja.fondo-color-sistema-p.mb-5.borde-lg-10(style="overflow: hidden;",data-aos="flip-up")
      .burbuja2.d-none.d-lg-block.left(style="top: 35px;")
      .burbuja2.d-none.d-lg-block.right(style="top: -75px;")
      .burbuja2.d-none.d-lg-block(style="bottom: -100px;left: 13%;")
      .burbuja2.right.d-lg-none(style="top: 19%;")
      .burbuja2.d-lg-none(style="bottom: -100px;left: 40px;")
      .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/74.svg",style="max-width: 1029px;",alt="Imagen que presenta el diagrama entidad relación persona-empleado.")
        figure.d-lg-none
          img.mx-auto(src="@/assets/curso/temas/75.svg",style="max-width: 451px;",alt="Imagen que presenta el diagrama entidad relación persona-empleado.")

    .row.mb-5
      .col-lg-7.mb-4.mb-lg-0
        .fondo-color-sistema-n.px-4.py-5.borde-10.mb-4(data-aos="fade-up")
          p.mb-0 #[b REGLA DE MAPEO 1:1 de modelo entidad-relación a modelo relacional:] en el momento de convertir la relación o con multiplicidad 1:1 a tablas, la relación uno a uno se convierte en una columna de la tabla empleado con restricción de unicidad (#[em Unique Key o Primary Key]), como se muestra en el siguiente diagrama relacional.
        p.mb-0(data-aos="fade-down") Como se puede inferir de la siguiente figura, se crea una tabla donde se relacionan los datos de las personas que son empleados del banco, a través de una columna que se llama #[b id_persona], pero es común entre algunos diseñadores ponerle el nombre que los relacione con la tabla a la que pertenece, es decir, #[b id_empleado], pero esto queda al criterio del diseñador.
      .col-lg-5(data-aos="fade-left")
        figure
          img.mx-auto(src="@/assets/curso/temas/76.png",style="max-width: 502px;")

    .row.justify-content-center(data-aos="fade")
      .col-lg-6
        .titulo-sexto.color-acento-contenido
          p.mb-0 #[b Figura 15.] Diagrama relacional 1:1
        figure.d-none.d-lg-block
          img.mx-auto(src="@/assets/curso/temas/77.png",style="max-width: 1028px;",alt="Imagen que presenta el diagrama relacional 1:1.")

        .fondo-personalizado-burbuja.fondo-color-sistema-p.borde-10.mb-5.d-lg-none(style="overflow: hidden;")
          .burbuja2.right(style="top: 19%;")
          .burbuja2(style="bottom: -100px;left: 40px;")
          .fondo-personalizado-burbuja__contenido.p-4.py-5.py-lg-4
            figure
              img.mx-auto(src="@/assets/curso/temas/78.png",style="max-width: 331px;",alt="Imagen que presenta el diagrama relacional 1:1.")
    



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
