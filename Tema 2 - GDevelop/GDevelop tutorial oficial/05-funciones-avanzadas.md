# 5. Funciones avanzadas y JavaScript

## 5.1. Eventos externos

Cuando varias escenas comparten una misma regla, puedes colocarla en un conjunto de eventos externo. Así evitas copiar y pegar la lógica de controles, pausas o interfaz.

Una buena regla para decidir: si el comportamiento debe corregirse en varios lugares a la vez, probablemente conviene reutilizarlo.

### Ejemplo práctico

Imagina que `Menu`, `Bosque` y `Victoria` necesitan un botón de volver al menú. En lugar de copiar la misma regla tres veces, crea un conjunto de eventos externo con la lógica del botón y añádelo a las escenas que lo necesiten.

Esto reduce errores: si el nombre de la escena cambia, corriges una sola regla.

## 5.2. Funciones

Una función recibe parámetros, realiza una tarea y puede devolver un resultado. En GDevelop, las funciones de eventos permiten convertir una secuencia repetida en una acción con nombre.

Ejemplos de funciones propias:

- `MostrarMensaje(texto)`;
- `CrearGuardian(posicionX, posicionY)`;
- `ReiniciarNivel()`;
- `SumarPuntos(cantidad)`.

Las funciones reducen duplicaciones y hacen que los eventos se lean como una descripción del diseño.

### Paso a paso: función para sumar puntos

1. Crea una función llamada `SumarPuntos`.
2. Añade un parámetro numérico llamado `cantidad`.
3. Dentro de la función, suma `cantidad` a la puntuación.
4. Desde el evento de recoger un cristal, llama a `SumarPuntos` con el valor `1`.
5. Desde el evento de derrotar un Guardian, llama a la misma función con el valor `5`.

Ahora existe una única regla para modificar la puntuación. Si decides cambiar cómo se calcula, solo debes cambiar la función.

## 5.3. Extensiones

Las extensiones añaden objetos, comportamientos, condiciones o acciones. Antes de instalarlas, comprueba su origen, versión y compatibilidad. Una extensión puede ahorrar mucho trabajo, pero también añade una dependencia que el equipo deberá entender y mantener.

### Antes de instalar una extensión

1. Comprueba si GDevelop ya incluye una acción equivalente.
2. Lee para qué versión está preparada.
3. Revisa qué objetos y eventos añade.
4. Prueba la extensión en una copia del proyecto.
5. Anota su nombre y su finalidad en la documentación del equipo.

## 5.4. Plantillas y objetos reutilizables

Las plantillas sirven para partir de una estructura ya preparada. Los objetos reutilizables permiten compartir un personaje, botón o componente entre escenas. Personaliza los nombres y documenta los cambios para que el proyecto siga siendo comprensible.

## 5.5. JavaScript como ampliación

GDevelop permite usar JavaScript cuando los eventos visuales no son suficientes o cuando se necesita integrar una lógica específica. No es necesario para empezar.

Antes de escribir JavaScript:

1. Comprueba si existe una condición o acción equivalente.
2. Mantén el código pequeño y con una responsabilidad clara.
3. Usa nombres descriptivos.
4. Comprueba que los objetos existen antes de acceder a ellos.
5. Prueba la lógica en una escena pequeña.

El código debe convivir con los eventos, no duplicar sin motivo lo que ya está hecho visualmente.

### Cuándo usarlo

Usa JavaScript solo si necesitas una operación difícil de expresar con eventos, una integración concreta o una transformación de datos. Para mover a Luna, detectar una colisión o cambiar un texto, los eventos visuales suelen ser más fáciles de leer en 4º de ESO.

Un buen primer experimento es escribir una pequeña operación que lea una variable y muestre un resultado. Hazlo en una escena de prueba, guarda antes una copia y comprueba qué ocurre si la variable todavía no existe.

## 5.6. Datos estructurados

Una variable de estructura puede guardar datos relacionados, por ejemplo:

```text
Jugador
  nombre: Luna
  vidas: 3
  inventario
    cristales: 2
    llaves: 1
```

Esta organización resulta útil para inventarios, configuraciones y perfiles. Si una estructura se vuelve demasiado compleja, simplifica el diseño o divide la responsabilidad entre varias funciones.

## 5.7. Multijugador y servicios externos

El multijugador exige pensar qué información pertenece a cada jugador, qué datos deben sincronizarse y qué ocurre cuando una conexión se pierde. Empieza por una experiencia local y añade red solo cuando el diseño básico sea estable.

Los servicios externos, anuncios, compras o clasificaciones deben cumplir las normas de la plataforma y respetar la privacidad. En proyectos educativos, basta con comprender el concepto y documentar cualquier dependencia.

## 5.8. Rendimiento

Para que el juego responda bien:

- evita crear y destruir grandes cantidades de objetos innecesariamente;
- elimina o reutiliza instancias que ya no hacen falta;
- reduce imágenes y audio excesivamente grandes;
- limita efectos y partículas simultáneos;
- prueba en el dispositivo menos potente previsto;
- mide antes de optimizar.

### Señales de un problema de rendimiento

- el juego responde tarde a los controles;
- aparecen tirones cuando hay muchos enemigos;
- el sonido se corta o la ventana tarda en actualizarse;
- la memoria aumenta sin parar.

No soluciones todos estos problemas cambiando valores al azar. Reproduce el fallo, elimina temporalmente una parte del juego y comprueba si el comportamiento cambia.

## Actividad de refactorización

Revisa los eventos del prototipo y localiza una regla repetida. Conviértela en una función o evento externo. Escribe qué recibe, qué modifica y en qué escenas se utiliza.

### Qué debes entregar

- nombre de la función o evento externo;
- problema que evita repetir;
- parámetros que recibe;
- variables u objetos que modifica;
- escenas donde se utiliza;
- una prueba que demuestre que sigue funcionando.
