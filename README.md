# Taller raster

## Prop贸sito

Comprender algunos aspectos fundamentales del paradigma de rasterizaci贸n.

## Tareas

Emplee coordenadas baric茅ntricas para:

1. Rasterizar un tri谩ngulo;
2. Implementar un algoritmo de anti-aliasing para sus aristas; y,
3. Hacer shading sobre su superficie.

Implemente la funci贸n ```triangleRaster()``` del sketch adjunto para tal efecto, requiere la librer铆a [frames](https://github.com/VisualComputing/framesjs/releases).

## Integrantes

M谩ximo 3.

Complete la tabla:

| Integrante | github nick |
|------------|-------------|
| Juan Nicol醩 Sastoque Espinosa | [NicolasZon](https://github.com/NicolasZon/) |
| Liseth Brice駉 Albarrac韓 | [ligibrial](https://github.com/ligibrial/) | 

## Discusi贸n

Describa los resultados obtenidos. Qu茅 t茅cnicas de anti-aliasing y shading se exploraron? Adjunte las referencias. Discuta las dificultades encontradas.


Para decidir si un punto se encontraba dentro del interior del triangulo fue necesario implementar la formula para calcular la orientaci贸n de los v茅rtices , este calculo corresponde a:
(A1.x - A3.x) * (A2.y - A3.y) - (A1.y - A3.y) * (A2.x - A3.x)

Dado lo anterior si era mayor que sero tenia una orientaci贸n positiva en caso contrario era negativa.

Lo cual gener贸 las siguientes imagen茅s con aliasing y sin antialiasing:

 
Para realizar la t茅cnica de anti-aliasing se tuvo en cuenta que se subdividio cada uno de los pixeles(puntos) en zonas mas peque帽as, y a su vez se tuvo en cuenta que cada regi贸n ten铆a su respectivo  color ,
y en cuanto la t茅cnica de shading se explor贸 el color correspondiente  de cada uno de los puntos del triangulo en RGB, y a partir de este se observa que cada punto dentro dentro triangulo corresponde a una intesidad de color distinto.

Referencias:

* https://www.youtube.com/watch?v=7uGlMA3FV1E
* http://www.dma.fi.upm.es/personal/mabellanas/tfcs/kirkpatrick/Aplicacion/algoritmos.htm#puntoInteriorAlgoritmo
* https://fgiesen.wordpress.com/2013/02/08/triangle-rasterization-in-practice/
* https://fgiesen.wordpress.com/2013/02/06/the-barycentric-conspirac/

Algunas de las dificultades encontradas fue la ubicaci贸n de un punto dentro de un tri谩ngulo, para ello fue necesario entender la explicaci贸n de las  coordenas baric茅ntricas para as铆 mismo calcular la orientaci贸n del triangulo y saber si en este  caso era positivo o  negativo.


## Entrega

* Modo de entrega: [Fork](https://help.github.com/articles/fork-a-repo/) la plantilla en las cuentas de los integrantes (de las que se tomar谩 una al azar).
* Plazo: 1/4/18 a las 24h.
