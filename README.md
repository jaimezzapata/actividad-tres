# Paleta de Colores - Actividad Tres (Agencia Creativa)

Para esta tercera actividad, hemos construido el portafolio de una **Agencia Creativa / Estudio de Diseño**. 

El diseño explora un "Modo Oscuro Cálido" que utiliza grises tierra (Stones) en lugar de grises azulados, acentuados con un naranja vibrante para darle un toque creativo. Además, se invirtió la disposición del Héroe y se usaron tarjetas horizontales.

Se mantuvieron rigurosamente las reglas del proyecto:
- Únicamente Box Model y Flexbox (sin Grid).
- Estilos aplicados solo con clases independientes.
- HTML altamente semántico.
- Colores planos, sin degradados.

## Colores Implementados

| Hexadecimal | Nombre Aproximado | Uso Principal |
| :--- | :--- | :--- |
| **`#1c1917`** | Stone 900 (Marrón Muy Oscuro) | Fondo general del documento |
| **`#292524`** | Stone 800 (Gris Cálido Oscuro)| Fondo de cabecera y tarjetas de servicios |
| **`#0c0a09`** | Stone 950 (Casi Negro) | Fondo del pie de página |
| **`#f97316`** | Orange 500 (Naranja Vivo) | Acento visual: Textos de Logo, Botón principal, y títulos de servicios |
| **`#fafaf9`** | Stone 50 (Blanco Cálido) | Títulos principales e importantes y color de fuente base |
| **`#d6d3d1`** | Stone 300 (Gris Cálido Claro)| Textos de navegación y descripciones de servicios |
| **`#a8a29e`** | Stone 400 (Gris Medio Cálido)| Subtítulo del hero |
| **`#78716c`** | Stone 500 (Gris Pardo) | Texto de copyright en el footer |

## Cómo incluir una imagen de fondo en una etiqueta

Para colocar una imagen de fondo (background) utilizando CSS, tal como se documentó en las actividades previas, debes seguir estos sencillos pasos:

1. **Añade una clase a tu etiqueta HTML:**
   Asegúrate de que el contenedor donde irá el fondo tenga una clase (recuerda que en este proyecto usamos únicamente clases).
   ```html
   <header class="hero-section">
       <!-- Tu contenido -->
   </header>
   ```

2. **Enlázalo usando `background-image` en tu archivo CSS:**
   En tu hoja de estilos, llama a la clase y usa la propiedad `background-image` con la función `url()` para indicar la ruta de la imagen. 
   
   * **Origen de la imagen:** La imagen puede estar previamente descargada y guardada dentro de la misma carpeta de tu proyecto, o bien, puedes colocar una URL externa completa de una imagen que esté en internet.
   * **Uso de comillas:** Dentro de la función `url()`, el uso de comillas simples o dobles es **completamente opcional**. Es válido escribir `url(hero_bg.jpg)` sin comillas. Sin embargo, usar comillas es una buena práctica recomendada, especialmente si la ruta o el nombre del archivo contiene espacios o caracteres especiales.

   ```css
   .hero-section {
       background-image: url('hero_bg.jpg');
   }
   ```

3. **Controla la apariencia del fondo (Explicación de propiedades):**
   Por defecto, las imágenes de fondo se muestran en su tamaño original y se repiten infinitamente (como un mosaico) para rellenar el espacio. Para que la imagen luzca profesional y adaptada a la caja, usamos estas propiedades adicionales:

   * **`background-image`**: Es la propiedad principal que le ordena al contenedor qué imagen gráfica debe pintar de fondo.
   * **`background-size: cover;`**: Esta propiedad obliga a la imagen a crecer o encogerse hasta **cubrir el 100% de la caja** sin perder sus proporciones. Esto evita que la imagen se vea estirada o achatada. Si la caja y la imagen tienen proporciones diferentes, `cover` recortará el sobrante.
   * **`background-position: center;`**: Define el punto de anclaje de la imagen. Al establecerlo en `center`, nos aseguramos de que el centro exacto de la fotografía siempre esté alineado con el centro de la caja, garantizando que el recorte sea simétrico en los bordes.

   ```css
   .hero-section {
       background-image: url('hero_bg.jpg');
       background-size: cover;      
       background-position: center; 
   }
   ```
