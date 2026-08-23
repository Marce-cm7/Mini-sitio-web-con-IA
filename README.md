#  Mini-sitio-web-con-IA

##  ¿Qué voy a recomendar?

Los dos parques de Disney que hay en Anaheim, California, y cuáles son las mejores **6 atracciones y 6 tierras temáticas** de cada uno de los parques.

---

##  ¿A quién va dirigida la página?

A aquellas personas que quieren visitar alguno de los dos parques de Disney, pero no saben cuál de los dos visitar.

---

## ¿Qué información tendrá cada recomendación?

Cada recomendación tendrá:

1. Imagen de la recomendación.
2. Nombre de la atracción o tierra temática.
3. Breve información acerca de la recomendación.
4. Botón con enlace que abrirá un video en YouTube de cada atracción o tierra temática.

---

##  ¿Qué quiero que suceda cuando el usuario interactúe con mi página?

Quiero que la página genere en el usuario muchas ganas de visitar alguno de los dos parques, a tal grado de querer comprar sus tickets y sus boletos de avión. 

---

# 1.  Nombre del proyecto

**Mini-sitio-web-con-IA**

---

# 2.  Descripción

Recomiendo cuál de los dos parques de Disney ubicados en Anaheim, California, visitar dependiendo de los gustos del usuario.

De cada parque recomiendo mis atracciones y tierras temáticas favoritas.

---

# 3.  Tecnologías

- HTML
- CSS
- Bootstrap
- JavaScript
- Git
- GitHub
- IA utilizada: **ChatGPT**

---

# 4.  Proceso con IA

## Prompts principales

### 1.  Ideas para el sitio web

> Actúa como tutor de desarrollo web para principiantes. Estoy creando un sitio web donde recomiendo los parques de Disney en Anaheim, California. Estoy utilizando HTML, CSS, Bootstrap y variables básicas de JavaScript. Yo sola ya hice más o menos la estructura de las secciones que tendrá mi sitio web y ya tengo el navbar, las 12 cards de recomendaciones, 2 carruseles con imágenes, h1, h2 y párrafos. Ahora necesito que me recomiendes qué más puedo agregar como secciones.

### 2. Cards con efecto giratorio

> Hice unas cards con ayuda de Bootstrap, estas cards tienen imagen, h4, párrafo y más texto, pero me gustaría que la card no quedara tan alargada y que una parte del contenido quede atrás, o sea, que la card al dar clic se gire y muestre contenido. Oriéntame para hacer el código del efecto de la card giratoria, pero no me generes el código. No puedo usar JavaScript porque solo he visto variables, por lo que necesito lograr ese efecto giratorio de la card con sólo HTML y CSS.

### 3.  Footer

> Estoy intentando que mi footer tenga los menús que tengo en el navbar, pero no lo estoy logrando. Quise intentar replicar un poco del código del navbar, pero no lo logro. Este es el fragmento de código. Ayúdame a identificar el problema, pero no me des directamente la solución. Te estaré preguntando muchas cosas y dudas si no entiendo.

### 4.  Diseño responsivo

> Terminé mi sitio web, pero el responsivo versión móvil no se ve muy estético y las 12 cards que tengo en el sitio se ven muy mal y quedan muy juntas. La verdad me siento perdida en hacer que mi sitio sea responsivo. Necesito que me expliques cómo puedo lograr que el sitio sea responsivo. Debo lograrlo con sólo HTML, CSS y Bootstrap, ya que de JavaScript sólo he visto variables y no he aprendido funciones, ciclos ni manipulación del DOM.

---

# 5. Código generado vs. código propio

## ¿Qué generó la IA?

La IA generó o ayudó a generar las siguientes partes del proyecto:

- Las 2 cards con su efecto giratorio de la sección **"Dos parques, dos experiencias"**, tanto el HTML como el CSS.
- El código del footer, ya que yo quería que tuviera el mismo contenido del navbar y no estaba logrando hacerlo por mi cuenta. Posteriormente, le pedí que me explicara los elementos que relacionaban el footer con el navbar.
- Código para hacer el sitio responsivo. La IA me explicó que debía modificar algunos `<div>` que ya tenía en mi código.

## ¿Qué modifiqué?

- Personalicé a mi gusto los estilos que me dio la IA para las dos cards con efecto giratorio.
- Agregué y modifiqué los `id` de las secciones para que funcionaran correctamente los enlaces del navbar.
- Modifiqué a mi gusto el CSS que generó la IA, incluyendo los estilos relacionados con los `id`.
- Del código generado para hacer el sitio responsivo, también modifiqué los estilos CSS a mi gusto y realicé diferentes cambios en el HTML.

###  Cambios realizados para hacer las cards responsivas

Lo que hice fue reemplazar algunas partes del código que ya tenía para las 12 cards.

### 1. Cambié `row`

**Antes:**

```html
<div class="row">
```

**Después:**

```html
<div class="row g-4">
```

### 2. Cambié `col`

**Antes:**

```html
<div class="col">
```

**Después:**

```html
<div class="col-12 col-md-6 col-lg-4">
```

### 3. Cambié el ancho fijo de las cards

**Antes:**

```html
<div class="card" style="width: 18rem;">
```

**Después:**

```html
<div class="card">
```

Al eliminar el `width` fijo, permití que el sistema de columnas de Bootstrap pudiera controlar mejor el ancho de las cards dependiendo del tamaño de la pantalla.

###  Cambios realizados en CSS

También agregué una regla `@media` para adaptar diferentes elementos cuando la pantalla tiene un ancho máximo de 768px:

```css
@media (max-width: 768px) {

    h1, h2 {
        font-size: 35px;
    }

    h3 {
        font-size: 28px;
    }

    .card-parque {
        width: 300px;
        height: 400px;
    }

    .footer-container {
        flex-direction: column;
        gap: 25px;
    }

}
```

---

# 6.  Aprendizaje

## ¿Qué concepto nuevo comprendí gracias a la IA?

### 1.  Sistema de columnas de Bootstrap

Comprendí cómo funciona el sistema de columnas de Bootstrap para crear sitios responsivos.

Aprendí que clases como:

```html
col-12
col-md-6
col-lg-4
```

permiten indicar cuánto espacio ocupará un elemento dependiendo del tamaño de la pantalla.

También comprendí que:

```text
row
→ crea una fila
```

y:

```text
col-12 col-md-6 col-lg-4
→ determina el espacio que ocupa la card según el tamaño de pantalla
```

### 2.  Efecto de voltear cards sin JavaScript

Aprendí a crear un efecto para voltear las cards sin tener que utilizar JavaScript, utilizando HTML y CSS.

Aprendí conceptos como:

```text
card-front
card-back
```

que permiten organizar el contenido de la parte frontal y posterior de la card.

También aprendí la lógica de utilizar:

```html
<input type="checkbox">
```

para controlar el efecto giratorio de las cards sin utilizar JavaScript.

### 3.  Uso de `@media`

Aprendí que añadir reglas `@media` es fundamental para crear un sitio responsivo y adaptativo.

Las reglas `@media` permiten modificar determinados estilos cuando la pantalla tiene un tamaño específico, por ejemplo, cuando el usuario visita la página desde un celular.

### 4.  Ancho de las cards de Bootstrap

De Bootstrap obtuve el código de las cards que utilicé y observé que por defecto se incluye:

```html
style="width: 18rem;"
```

Comprendí que este `width` fijo puede dificultar un poco la adaptación de las cards a diferentes tamaños de pantalla.

Por esta razón lo modifiqué y eliminé el ancho fijo, permitiendo que las columnas de Bootstrap controlaran mejor el ancho de las cards.

---

# 7.  Reflexión

## ¿Hubo algún momento en que la IA generó código que no comprendía?

Sí. Sobre todo con el código CSS de las 2 cards que se voltean, ya que al principio no comprendía la funcionalidad de muchos de los elementos utilizados.

Por esta razón, tuve que pedirle a la IA que me explicara la funcionalidad de cada estilo y de cada elemento del código.

En lugar de solamente copiar y pegar el código, fui preguntando qué hacía cada parte para poder comprender cómo funcionaba el efecto giratorio y posteriormente poder modificarlo a mi gusto.

Mis apuntes acerca de este proceso y de la explicación de los estilos se encuentran escritos en mi archivo `styles.css`.

Esta experiencia me ayudó a comprender que la IA puede ser una herramienta de apoyo para aprender programación, pero es importante **entender el código que genera, hacer preguntas, probarlo y modificarlo**, en lugar de utilizarlo sin comprender su funcionamiento.