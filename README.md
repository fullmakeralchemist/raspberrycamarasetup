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
* Si utilizas el Case, necesitarás tornillos a la medida [M2.5](https://www.adafruit.com/product/3299), necesitaremos de 12mm y 8mm de largo, aunque para aprovechar puedes comprar algunos de 10mm y 5mm pueden ser útiles para otros proyectos, los puedes conseguir en Amazon o tiendas especializadas en electrónica.

En caso hicieras uso del modelo 3D aquí tienes una imagen de cómo se vería, esta increíble no lo crees?


Ahora hablaremos de los dos modulos que mencione.

### 1.1 HQ Camera module

Este módulo es el más reciente accesorio de cámara Raspberry Pi. Ofrece una resolución más alta (12 megapíxeles, en comparación con la anterior de 8 megapíxeles) y sensibilidad (aproximadamente un 50% más de área por píxel para rendimiento mejorado en condiciones de poca luz) que el módulo de cámara v2 existente, y está diseñado para funcionar con lentes intercambiables en montura C y CS. Se pueden utilizar otros lentes utilizando adaptadores.

Los lentes de 6 mm con montura CS y [16 mm](https://www.adafruit.com/product/4562) con montura C son ejemplos de todos los compatibles que existen.
La cámara de alta calidad ofrece una alternativa al módulo de cámara v2.

Para aplicaciones industriales y de consumo, incluidas cámaras de seguridad, que requieren los más altos niveles de fidelidad visual y/o integración con óptica especializada. Es compatible con todos los modelos de Raspberry Pi, la última versión de software.


### 1.2 Raspberry Pi Camera Board v2 (8 Mp)

Este módulo de cámara de 8 Mp es capaz de capturar video de 1080 px e imágenes, se puede conectar a todos los modelos de Raspberry Pi. Listo para conectar y usar, muy adecuado para fotografiar por lapsos, grabar video o para usarlo en aplicaciones de seguridad y en detección de movimientos. Sólo hay que conectar el cable incluido al puerto CSI de la Raspberry Pi.

El módulo es pequeño mide 25 mm x 23 mm x 9 mm y tiene una peso de 3 gr, haciéndola perfecta para aplicaciones móviles u otras en donde el peso es un factor muy importante.

El sensor tiene una resolución de 8 megapíxeles y tiene un lente de enfoque. En cuanto a las imágenes, la cámara es capaz de tomar imágenes estáticas hasta de 3280 x 2464 pixeles y videos de 1830p30.


## 2.Configuración de la cámara

### 2.1 Conexión física

Todos los modelos actuales de Raspberry Pi tienen un puerto para conectar el módulo de la cámara.

**Nota: Si desea utilizar una Raspberry Pi Zero, necesita un [cable](https://www.adafruit.com/product/3157) del módulo de la cámara que se ajuste al puerto del módulo de la cámara más pequeño de la Raspberry Pi Zero.**


Conecte el módulo de la cámara.

**Asegúrese de que su Raspberry Pi esté apagada.**

1.   Localice el puerto del módulo de la cámara
2.   Tire suavemente hacia arriba de los bordes del clip de plástico del puerto
3. Inserte el cable plano del módulo de la cámara (**Nota: asegúrese de que el cable esté en la dirección correcta. El lado azul del cable va mirando hacia el conector jack y de los puertos USB**)
4. Vuelva a colocar el clip de plástico en su lugar.


La forma mas simple de conectar el modulo HQ en mi caso se vería de la siguiente forma:


Yo opté por solamente utilizar el soporte de la cámara con la Raspberry por lo que te mostraré un poco de cómo utilice los tornillos y el resultado final.


Ahora solo faltaría conectar el lente que en esta ocasión utilicé el de 6mm, puedes saltarte esta parte y pasar a 2.2 si es que utilizaste la opción V2 de 8 Mp.


Tenemos que quitar la tapa anti-polvo para el lente de 6mm y el adaptador C-CS entonces nos quedaría de la siguiente forma:


Los lentes vienen con dos tapas una del lado del lente y otra por la entrada que conecta al modulo.