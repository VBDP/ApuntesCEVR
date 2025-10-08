
**07/10/2025**
Software:
DaVinci Resolve (Edición de video)
Conceptos importantes:

- Pixel
- Sprite
- Etalonaje
- 2,5D
- vectores, senos,cosenos,tangentes.
- Mapa de bits
- 1 pixel = 1 bit
- CPU y GPU
- cuda core: Operaciones tradicionales de graficos
- tensor core: Supersampling/DLSS, recalcula los pixeles de la imagen consiguiendo mayor rendimiento y fps con menor esfuerzo. Extrapolar la imagen.
- rt core: Calculos de Ray Tracing (Calculo de luz, sombras, rebote de la luz, etc...)
- Extrapolar: Agregar pixeles simulados entre los ya existentes haciendo el punto medio entre los pixeles de la imagen.

- 16-20 fps: sensacion de movimiento, 25fps en europa minimo 30fps en eeuu, cine:24fps mundialmente.

 Intro:
 2D: Bitmaps (Mapas de bits) y Vectores.
 3D: Modelado, Materiales, Textura y color, Iluminación y Cámara, Animación (Manual o por Físicas),Video.
 FX: CGI, Post-Producción., Títulos de credito, Efectos especiales, Etalonaje(proceso de corrección y ajuste del color).

https://www.shadertoy.com/
--------------------------------------------------------------
**08/10/2025**

Bit,Byte,KB,GB...
Numeros mágicos: 0,1,2,4,8....
- Habla de como funcionan nuestros ojos y de los bastoncitos de 3 tipos que ven rojo,verde y azul.
**El pixel:**
- Que es un pixel:
	- Un pixel es la unidad más pequeña a nivel gráfico, valor mínimo 1 bit.
- ¿Como se usan para visualizar la información?
**Ejemplo del profesor:**
- Ha dibujado un grid con un rombo en la pizarra de 7x7.
- Cada pixel es un bit que en binario es encendido/apagado (1/0).
- Bitmap: Representación en bits de los pixeles que se ven en pantalla.
- La gráfica necesitará una memoria mínima para poder guardar los mapas de bits.
- Los bits necesarios se calculará multiplicando horizontal x vertical para saber el mínimo. (rh x rv)
**Cómo consigue la gráfica mostrar el color en los pixeles?**
- Usa más bits de memoria para albergar los colores.
- Para conseguir más colores se agregan capas de profundidad, que son mapas de bits superpuestos.
**¿Cómo conseguir el RGB con este sistema?**
- Entre blanco y negro hay una escala de grises.
- Con 8 capas de profundidad podemos tener 256 colores diferentes.
- Entonces RGBA seria 8 x 4 = 32 capas de bitmaps, RGB sería 3* x 8 = 24 capas de bitmaps. 
**3 tipos de imagenes:**
- Blanco y Negro (1 capa de mapa de bits).
- Color indexado (Tonalidades de un solo color, 8 capas de mapa de bits).
- Color RGB (Color real requiere 24 capas de mapa de bits).
**2 Sistemas de color**
- Sustractivo: CMYK (Cian,Magenta,Amarillo,Negro).
- Aditivo: RGB, colores básicos.

Las gráficas hacen cálculos en 2D y 3D.

**Elementos que consumen memoria en una gráfica**
- Visualización de las imagenes
	- Para una imagen fullhd necesitamos 6mb.
	- Para una imagen 8k necesitamos 95mb de memoria.
- Cálculos en 2D y 3D.
- Almacenamiento de Texturas, imagenes que envuelven objetos tridimensionales para darles una apariencia diferente.