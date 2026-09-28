# 6. Pruebas, publicación y trabajo en equipo

## 6.1. Vista previa

La vista previa permite probar el juego sin generar todavía una versión final. Ejecuta pruebas cortas después de cada cambio importante. Comprueba el comportamiento, no solo el aspecto.

Lista mínima:

- ¿La escena inicial es correcta?
- ¿Se puede iniciar y reiniciar la partida?
- ¿Los controles responden?
- ¿Las colisiones funcionan en los bordes?
- ¿La puntuación se actualiza una sola vez?
- ¿Se puede ganar y perder?
- ¿La interfaz se lee en la resolución prevista?
- ¿El sonido se puede silenciar?

### Prueba guiada de una partida

1. Abre la escena `Menu` y pulsa el botón de empezar.
2. Comprueba que llegas a `Bosque`.
3. Mueve a Luna hasta el primer cristal.
4. Confirma que desaparece una sola instancia.
5. Comprueba que el texto y la variable aumentan una unidad.
6. Toca un Guardian y observa la pérdida de vida.
7. Recoge todos los cristales y verifica la escena `Victoria`.
8. Repite la partida hasta llegar a `Derrota`.
9. Reinicia y confirma que las variables vuelven a sus valores iniciales.

Escribe el resultado de cada paso. Una prueba escrita convierte "creo que funciona" en una comprobación que otra persona puede repetir.

## 6.2. Depuración

Cuando algo falla, reduce el problema:

1. Describe qué esperabas.
2. Describe qué ocurre realmente.
3. Identifica el primer evento que podría cambiar ese estado.
4. Observa variables y objetos en la vista previa.
5. Desactiva temporalmente reglas no relacionadas.
6. Cambia una sola cosa y vuelve a probar.

Los comentarios y nombres precisos ayudan más que acumular eventos sin orden.

### Método de las tres preguntas

Cuando algo falle, responde:

1. **¿Qué esperaba ver?** Por ejemplo: "el cristal desaparece".
2. **¿Qué ha ocurrido?** Por ejemplo: "Luna lo atraviesa y el cristal sigue ahí".
3. **¿Qué parte más pequeña puedo comprobar?** Por ejemplo: "si la condición de colisión llega a cumplirse".

Después añade una prueba temporal, observa una variable o desactiva un evento no relacionado. El objetivo es localizar la primera regla que se comporta de forma diferente a lo esperado.

## 6.3. Pruebas de aceptación

Escribe pruebas que otra persona pueda repetir:

| Prueba | Pasos | Resultado esperado |
| :--- | :--- | :--- |
| Recoger cristal | Mover Luna hasta un cristal | Desaparece y suma 1 |
| Perder vida | Tocar un Guardian | Las vidas disminuyen |
| Victoria | Recoger tres cristales | Aparece la escena de victoria |
| Reinicio | Pulsar reiniciar | Comienza un nivel nuevo |

Añade también casos límite:

- recoger dos cristales en el mismo instante;
- chocar con dos Guardianes;
- pulsar reiniciar durante una transición;
- cambiar el tamaño de la ventana;
- jugar sin sonido.

## 6.4. Compartir y colaborar

Antes de trabajar en equipo, acordad nombres de escenas, objetos y variables. Divide el proyecto por responsabilidades: diseño de nivel, arte, eventos, audio y pruebas. Conserva copias y registra cambios importantes.

No compartas credenciales ni datos personales en el proyecto. Revisa los permisos de cualquier servicio en línea utilizado.

## 6.5. Publicar el juego

GDevelop puede preparar versiones para web, escritorio, móvil y otras plataformas, según la edición y las opciones disponibles. El flujo general es:

1. Guardar y probar el proyecto.
2. Revisar escenas, recursos y licencias.
3. Elegir una plataforma de destino.
4. Configurar nombre, icono, orientación y resolución.
5. Generar una versión de prueba.
6. Probarla fuera del editor.
7. Generar la versión final y distribuirla según las normas de la plataforma.

Las tiendas y servicios de publicación pueden requerir cuentas, firmas, identificadores, políticas de privacidad y materiales gráficos. Consulta la [guía oficial de publicación](https://wiki.gdevelop.io/gdevelop5/publishing/) antes de subir un proyecto.

### Publicar para la web: recorrido general

1. Completa una prueba local.
2. Revisa el nombre y la descripción del juego.
3. Comprueba que todas las imágenes y sonidos tienen una licencia adecuada.
4. Elige la opción de exportación para web.
5. Genera una versión de prueba.
6. Abre esa versión y prueba el juego fuera del editor.
7. Revisa que los controles, el audio y los cambios de escena funcionan.
8. Comparte solo la versión que hayas probado.

Los botones exactos pueden cambiar según la versión y la plataforma. El principio no cambia: **probar primero, publicar después**.

## 6.6. Accesibilidad y diseño responsable

Un juego más accesible beneficia a más personas. Considera:

- subtítulos y textos legibles;
- contraste suficiente;
- controles alternativos;
- volumen regulable;
- señales visuales y sonoras redundantes;
- dificultad ajustable;
- ausencia de destellos peligrosos;
- instrucciones que no dependan solo del color.

## Proyecto final

Entrega una versión jugable de *La expedición de Luna* con:

- cuatro escenas;
- al menos tres tipos de objeto;
- un comportamiento de movimiento;
- eventos con condiciones y acciones;
- variables de puntuación y vidas;
- una interfaz en una capa independiente;
- sonido o música con licencia adecuada;
- pantalla de victoria y pantalla de derrota;
- una tabla de pruebas completada;
- una breve nota de recursos y atribuciones.

### Guion de trabajo recomendado

| Fase | Producto que debe quedar terminado |
| :--- | :--- |
| Diseño | Boceto de escenas, objetivo y controles |
| Prototipo | Luna se mueve y la vista previa funciona |
| Reglas | Cristales, Guardianes, vidas y victoria |
| Presentación | Capas, interfaz, animaciones y sonido |
| Pruebas | Tabla de fallos y soluciones |
| Publicación | Versión exportada y ficha de recursos |

## Autoevaluación

1. Explica con tus palabras la diferencia entre un objeto y una instancia.
2. Escribe un evento con una condición y dos acciones.
3. Indica qué variable debería ser global y cuál debería pertenecer a una escena.
4. ¿Por qué conviene probar después de cada cambio pequeño?
5. ¿Qué comprobarías antes de compartir un juego con otras personas?

## Para ampliar

Consulta la [documentación oficial de GDevelop 5](https://wiki.gdevelop.io/gdevelop5/) para estudiar funciones concretas, cambios de versión, extensiones y opciones de publicación. La documentación es la referencia adecuada cuando el nombre de una acción o la ubicación de un menú cambie.
