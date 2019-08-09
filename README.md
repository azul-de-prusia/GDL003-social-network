# Creando una Red Social. Uniapp

## Introducción

El tema elegido para este proyecto es la educación superior, creamos una red social para el uso de los integrantes de una comunidad universitaria de educación privada. 
La idea principal es generar una plataforma donde se facilite la comunicación entre los miembros de la comunidad sin tener que hacer uso de las redes de mensajería personal como Whatsapp, y así poder estar en contacto para temas académicos, administrativos y de difusión. 
La app será gratuita y se fomentará su uso para tenerla como el canal de comunicación en la universidad.


## Consideraciones generales

Este proyecto se resolvío en un equipo formado por Karina Cabrera, Laura Maya y Coral Quiñones.

La lógica del proyecto está implementada completamente en JavaScript (ES6),
HTML y CSS. Sin utilización de frameworks de JS. Es de desarrollo mobile first.

### Definición del producto

De acuerdo a nuestra experiencia las redes sociales cumplen la función de conectar personas, creando redes donde pueden interactuar con otros usuarios de manera directa, publicar y compartir información.
Generalmente estas redes están enfocadas en un objetivo específico en función de lo que desean compartir, por ejemplo imágenes y videos en el caso de Instagram, mensajería en Whatsapp, etc.

Elegimos como tema la educación universitaria porque en un centro de estudios como este es necesario estar en contacto con otros compañeros para realizar trabajos, con docentes para definir fechas y características de lostrabajos en casa, así como dudas que puedan surgir de los estudiantes, también la comunidad administrativa y de difusión estarían en contacto con los miembros del plantel para recordar sobre límites de pago y avisos. Pensamos que todo lo anterior sería más profesional si estos usuarios contaran con un medio de comunicación de estas características sin tener que recurrir a los teléfonos personales.

En nuestro caso, debido a que nuestros usuarios son variados (estudiantes, académicos, administrativos y directivos),desde el planteamiento del prototipo se buscó que fuera similar a la red de Facebook ya que la gran mayoría de las personas están familiarizadas con esta app móvil. Por lo tanto, los íconos y la estructura general pretende ser familiar para el usuario.

Se realizó un prototipo de baja fidelidad https://www.figma.com/file/YUhRsbgzgrF751DuG2FYz0/Untitled?node-id=19%3A7
y una encuesta https://docs.google.com/forms/d/1KINgzFx4rHqlHBUAKjfzHSXZhAhFUxc7RM6-DKD85gw/edit para conocer mejor las necesidades de los posibles usuarios.

### Historias de usuario

Una vez que entiendas las necesidades de tu usuario, escribe las Historias de
Usuario que representen todo lo que el usuario necesita hacer/ver. Asegúrate
de incluir una definición de terminado (definition o done) para cada una.
1. Los usuarios de la app requieren poder iniciar sesión para ingresar a la comunidad.
Definition of done:
- Crear el inicio de sesión con firebase para acceder a la siguiente página.
2. Los usuarios de la app requieren autenticarse con facebook y gmail para ingresar a la app de forma más fácil y rápida.
Definition of done:
- Implementar autenticación con facebook.
- Implementar autenticación de gmail.
3. Los usuarios de la app requieren seguridad al ingresar sus correos y contraseñas.
Definition of done:
- Cubrir los caracteres del password.
- Verificar que el correo electrónico no esté ya vinculado a una cuenta existente.
- Añadir cierre de sesión.
4. Los usuarios de la app requieren poder realizar publicaciones para comunicarse entre ellos.
- Agregar publicaciones en el muro.
- No permitir publicar posts vacíos.
5. Los usuarios de la app requieren poder dar likes, estrellas o algún icono a las publicaciones.
Definition of done:
- Implementar likes para cada post realizado.
- Llevar un conteo de los likes a cada post. 
6. Los usuarios de la app requieren poder eliminar o editar sus publicaciones.
Definition of done:
- Editar publicaciones y almacenarlas con esos cambios.
- Brindar la posibilidad de eliminar posts por el autor.
7. Los usuarios de la app requieren poder filtrar sus publicaciones para mostrarlas a público o amigos.
- Brindar la opción de mostrar a todo público o sólo a amigos cada vez que un post sea creado.

### Diseño de la Interfaz de Usuario (prototipo de baja fidelidad)


El prototipo de alta fidelidad se planteó para que el producto final fuese similar al formato y estilo de facebook para móvil, ya que es una red muy conocida y los usuarios ya están familiarizados con ella.

![alt text](https://i.ibb.co/mh5sHCk/67916332-346249096282493-8611885615799074816-n.jpg)
![alt text](https://i.ibb.co/g6Pr5kJ/68730180-900748293621841-3966325181718200320-n.jpg)

Lo primero que se muestra es la pantalla de inicio de sesión o registro para crear una cuenta, una vez que el usuario ya tiene cuenta e inició sesión se pasa al muro donde encontrará las publicaciones recientes de su comunidad universitaria. También se planea poder acceder a distintos servicios mediante íconos en la parte superior; nueva publicación, perfil personal, búsqueda, grupos, notificaciones y mensajes. Por último para cada post el autor debe tener las opciones de eliminar, editar y seleccionar si desea que sea público o para amigos, asimismo cada publicación podría tener likes y comentarios.

### Responsive

Debe verse bien en dispositivos de pantallas grandes
(computadoras/es, laptops, etc.) y pequeñas (tablets, celulares, etc.). Te
sugerimos seguir la técnica de `mobile first` (más detalles sobre esta técnica
al final).

### Hacker edition

* Crear posts con imágenes.
* Permite ver una parte de la aplicación así el usuario no tenga conexión a Internet usando [LocalStorage](https://developer.mozilla.org/es/docs/Web/API/Window/localStorage)
* Permite agregar amigos.
* Permite eliminar amigos.
* Permite compartir publicación (en twitter esto es retwittear, en facebook
  es compartir).
* Permite comentar o responder una publicación.
* Permite editar perfil.
* Permite ver perfil o resumen desde el _muro_ o lista de publicaciones.
* Que nuestra red social sea [_Single Page Application_](https://es.wikipedia.org/wiki/Single-page_application) 

### Consideraciones técnicas

El corazón de este proyecto incluye:

* Separar la manipulación del DOM de la lógica (Separación de responsabilidades).
* Que el sitio sea responsive.
* Alterar y persistir datos. Los datos que agregues o modifiques deberán
  persistir a lo largo de la aplicación, te recomendamos que uses
  [Firebase](https://firebase.google.com/).

Además, podrías agregar algunas tareas nuevas de acuerdo a tus decisiones:

* Recuerda que no hay un setup de **tests** definido, dependerá de
  la estructura de tu proyecto también, pero algo que no debes de olvidar es
  pensar en éstas pruebas, incluso te podrían ayudar a definir la estructura y
  nomenclatura de tu lógica.

### Consideraciones UX

Desde el punto de vista de UX, deberás:

* Se realizó una entrevista a usuarios.
* Se realizó un  prototipo de baja fidelidad.
* Se realizó un prototipo de alta fidelidad.
* Hacer sesiones de testing con el producto en HTML.

### Habilidades Blandas

Trabajar en equipo es un gran desafío porque coordinarse no es una tarea fácil,
y es más difícil entre tres que entre dos. Trata que tu equipo te entienda,
facilitando siempre el diálogo en dentro del squad.

Planifica enumerando las tareas y distribuyéndolas, considerando los
recursos, las habilidades, y el tiempo del que dispones. Planifica de manera
que te permita avanzar en los distintos aspectos del proyecto de forma paralela,
teniendo un tablero donde puedas ver en qué está trabajando cada compañera.

Entrega tu trabajo a tu equipo a tiempo y colabora con el objetivo
final del proyecto, lo que puede implicar ayudar a los demás miembros del equipo
con sus pendientes, con el fin de entregar una red social de calidad.

**La división del trabajo debe permitir que todo el equipo
practique el aprendizaje de todas las habilidades esperadas. No se dividan el
trabajo como en una fábrica**

Para conocer a los usuario para eso debes salir e investigar. Tienes que
ejercitar tus habilidades de comunicación y toma de decisiones.
Existen infinitas opciones, depende de ti el camino que escoges.
Para que tu red social responda a las necesidades de sus usuarios, probablemente
deberás adquirir nuevos conocimientos para implementar sus preferencias.

Esta vez, haz _code review_(feedback de tu código) con **otro squad**, para
que puedas mejorar el producto. Mientras más feedback reciban, mejor.

Esperamos que valores y escuches los comentarios y críticas de los demás,
rescatando aquellos aspectos que sirven para tu crecimiento. Entrega siempre
tu opinión de manera constructiva, fundamentada y coherente, con el propósito
de ayudar a tus compañeras. Estos comentarios los debes hacer de manera honesta,
empática e inmediata.

Finalmente, deberás presentar el proyecto que creaste, al usuario que escogiste
y las necesidades que lograste resolver en este proceso. Como siempre, sabemos
que presentar puede ser una tarea difícil, esperamos que tengas capacidad de
síntesis y articules tus ideas con claridad para que logres mostrar tu trabajo
y que los demás lo comprendan.

## Entrega

El proyecto será _entregado_ subiendo tu código a GitHub (`commit`/`push`) y la
interfaz será desplegada usando GitHub pages u otro servicio de hosting que
puedas haber encontrado en el camino.


## Checklist

### General

* [ ] Producto final sigue los lineamientos del diseño.

### `README.md`

* [✔] Definición del producto
* [✔] Resumen de entrevistas con usuarios.
* [✔] Link/screenshots prototipo de baja fidelidad.
* [ ] Conclusiones de pruebas con el producto en HTML.

### Pruebas / tests

* [ ] Pruebas unitarios cubren un mínimo del 70% de statements, functions,
  lines, y branches.
* [ ] Pasa tests (y linters) (`npm test`).

### Creación de cuenta (sign up)

* [✔] Permite crear cuenta.
* [✔] Valida email.
* [✔] Valida password.
* [✔] Muestra mensajes de error.

### Inicio de sesión (sign in)

* [✔] Permite iniciar sesión.
* [✔] Valida email.
* [✔] Valida password.
* [✔] Muestra mensajes de error.

### Muro (wall/feed)

* [✔ ] Muestra _muro_, o lista de publicaciones.
* [✔] Permite hacer nuevas publicaciones.
* [ ] Permite eliminar publicaciones.
* [ ] Pide confirmación antes de borrar publicación.
* [ ] Permite editar publicación en el mismo lugar (in place).
* [ ] Permite filtrar publicaciones por público/privado.
* [ ] Permite marcar publicaciones como _gustados_ (like, corazón, estrella,
  etc...).
* [ ] Permite ver cuántas marcas, likes, estrellas, corazones o lo que se haya
  elegido, ha recibido una publicación.

### Hacker Edition

* [ ] Permite agregar amigos.
* [ ] Permite eliminar amigos.
* [ ] Permite compartir publicación (en twitter esto es retwittear, en facebook
  es compartir).
* [ ] Permite comentar o responder una publicación.
* [ ] Permite editar perfil.
* [ ] Permite ver perfil o resumen desde el _muro_ o lista de publicaciones.
* [ ] Permite ver cuántas marcas, likes, estrellas, corazones o lo que se haya
  elegido, ha recibido una publicación.
* [ ] Single Page Application (Incluye refactorización)
