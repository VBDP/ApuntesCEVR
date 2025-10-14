Bit, Byte, KB, GB...
- Habla de como funcionan nuestros ojos y de los bastoncitos de 3 tipos que ven rojo, verde y azul.
- ¿Cómo se usan para visualizar la información?
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



Las gráficas hacen cálculos en 2D y 3D.

**Elementos que consumen memoria en una gráfica**
- Visualización de las imágenes
	- Para una imagen FullHD necesitamos 6mb.
	- Para una imagen 8k necesitamos 95mb de memoria.
- Cálculos en 2D y 3D.
- Almacenamiento de Texturas, imágenes que envuelven objetos tridimensionales para darles una apariencia diferente.
- -----------------------------------------------------
- - Capacidad de las gafas de realidad virtual: Meta Quest 2 con 256gb, 3 con  512...
- Memoria ram que tienen nuestros dispositivos.
- Cuanto ocupan algunos videojuegos.
- ¿De donde sale la memoria virtual?: Sale del disco duro, se agarra una porción de la memoria. Por ejemplo tengo 12 de ram + 8 virtual, los 8gb están en el disco duro. La memoria virtual es mucho más lenta que la ram.
	- Si tu guardas 8gb de Vram, al arrancar el sistema guardará 8gb, lo cortará en trozos en algo llamado páginas de memoria y ocupará los espacios necesarios de la vram una vez se ocupe totalmente la memoria ram, pero a costa de cortar y pegar paginas de memoria en el disco duro y hacer la paginación será siempre mucho más lento.
- Frame buffer: Memoria donde almacenar los bitmaps que se envían a las pantallas, origen de las actuales GPU/Tarjetas Gráficas.
- Buffer: Cuando el procesador no puede procesar más, el pc usa el buffer para evitar que se pierda información por el camino. En un reproductor de música con un cd el cd se lee y se va guardando en el buffer desde donde luego reproduce la música.
- Descripción de Buffer: Porción de memoria de una cantidad X cuya finalidad es evitar la perdida de información.
- Todas las cachés son buffers pero no todos los buffers son un caché.
- ¿Qué es un caché?: Igual que un buffer pero además acelera el acceso a la información cuando necesita ser reutilizada.
	- CPU -> CACHE -> VIDEOJUEGO
- Arquitectura vonn newman: CPU,Memoria, E/S.


![[Pasted image 20251013110324.png]]
- El chipset hace de intermediario entre todos los dispositivos y la cpu a través del bus de datos.
- Los canales de la placa base son los caminos donde va la información.
- El controlador de memoria está en la propia cpu aunque antiguamente estaba en el chipset.

BUSCAR COMO FUNCIONAN LOS BUSES DE DATOS Y DE CONTROL Y DIRECCIONES EN LA ARQUITECTURA DE VONN NEWMANN.

               +-------------------------------+
               |           Memoria             |
               |  (Datos e Instrucciones)     |
               +-------------------------------+
                        ^  ^  ^
                        |  |  |
          Bus de Datos  |  |  | Bus de Direcciones
                        |  |  |
                        v  v  v
+--------+       +----------------+       +-----------------+
|        |       | Unidad de      |<----->| Dispositivos de |
|  CPU   |<----->| Control        |       | Entrada/Salida |
|        |       +----------------+       +-----------------+
|        |
|        |       +----------------+
|        |<----->| Unidad Aritmético|
|        |       | y Lógica (ALU)   |
+--------+
          ^
          |
          | Bus de Control

----------------------------------------
Prototipado: Se hace un prototipo para que los posibles inversores vean el juego funcional y usable.
Las primeras versiones es todo muy básico, y el personaje es solo una capsula al principio.