# Configuración de Cámara Raspberry

Una de las aplicaciones más utilizadas en Raspberry es el uso de cámaras, para utilizar Tensorflow y darle la capacidad de detectar objetos. Ahora que la Raspberry Pi es lo suficientemente rápida para realizar el aprendizaje automático, agregar estas funciones en proyectos es más sencillo.
 
Esta guía le mostrará los pasos para aprender a conectar el módulo de cámara Raspberry Pi, tome fotografías, grabe videos y aplique efectos de imagen.
 
Es importante conocer bien el módulo de cámara antes de comenzar a crear nuestras aplicaciones.
 
Sin mas que decir comencemos.

## 1.Materiales

Existen múltiples opciones pero en esta guía te daré dos opciones para que elijas la que te agrade más, por parte de Raspberry Pi existen dos módulos de cámara hablaré de ellos más adelante.
 
*   Laptop
*   Raspberry Pi 4
*   Fuente de alimentación (De preferencia adquirir junto con tu Raspberry la fuente oficial para no tener ningún problema, si es que no tienes mucha experiencia [USB-C Power Supply](https://www.raspberrypi.org/products/type-c-power-supply/))
* Smartphone con función Mobile Hotspot
*  Tarjeta Micro SD 
*  [Raspberry Pi High Quality Camera](https://www.adafruit.com/product/4561) (es la que usare en esta guía, pero puedes utilizar la [Raspberry Pi Camera Board v2](https://www.adafruit.com/product/3099) es la versión anterior y mas económica.)
* [6mm 3MP Wide Angle Lens for Raspberry Pi HQ Camera - 3MP](https://www.adafruit.com/product/4563) (el modulo HQ camera, nos permite utilizar lentes, este elemento es opcional en caso de utilizar la segunda opción de cámara.
* [Flex Cable for Raspberry Pi Camera](https://www.adafruit.com/product/2087) (suele venir incluido en la compra de los módulos Raspberry Pi Camera).
* Trípode de cámara (**Nota: solo en caso de usar el módulo HQ.** la ventaja del módulo HQ es que cuenta con una montura para trípodes con standard 1/4”-20, que es con el que cuentan la mayoría  de los trípodes actuales, te dejo un link de una opción de compra en [Amazon](https://www.amazon.com.mx/Ubeesize-tel%C3%A9fono-ajustable-distancia-Universal/dp/B06Y2VP3C7/ref=sr_1_3?__mk_es_MX=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=%C2%BC%22-20+tripod&qid=1620010127&refinements=p_36%3A9841539011&rnid=9754432011&s=electronics&sr=1-3))
 
Opcional:
* [Raspberry Pi HQ Camera Case](https://learn.adafruit.com/raspberry-pi-hq-camera-case/3d-printing) (En caso de que cuentes con una impresora 3D o de hacer impresiones 3D te dejo un link para que puedas imprimir una carcasa en forma de cámara, mas adelante te dejo la imagen de como se vería).
*Si utilizas el Case, necesitarás tornillos a la medida [M2.5](https://www.adafruit.com/product/3299), necesitaremos de 12mm y 8mm de largo, aunque para aprovechar puedes comprar algunos de 10mm y 5mm pueden ser útiles para otros proyectos, los puedes conseguir en Amazon o tiendas especializadas en electrónica.