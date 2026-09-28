# 2. Escenas, objetos y recursos

## 2.1. Escenas

Una escena es una pantalla o un nivel. Un proyecto puede tener `Menu`, `Bosque`, `Victoria` y `Derrota`. Cada escena puede incluir sus propios objetos, capas y eventos.

Las escenas no tienen por qué ser niveles completos: también pueden representar una pantalla de pausa, un diálogo o una pantalla de carga.

![Editor de escenas](https://wiki.gdevelop.io/gdevelop5/interface/scene-editor/Level.png)

*Figura 2.1: El editor de escenas sirve para colocar y organizar instancias. Imagen: documentación oficial de GDevelop.*

## 2.2. Objetos e instancias

Un **objeto** es una definición reutilizable. Una **instancia** es una aparición concreta de ese objeto dentro de una escena.

Por ejemplo, `Cristal` puede ser el objeto y los cinco cristales colocados en el bosque son cinco instancias. Si cambias la imagen del objeto, todas sus instancias pueden reflejar ese cambio; si mueves una instancia, solo cambias esa aparición.

### Una comparación sencilla

Piensa en un sello de goma. El sello es el **objeto**: define la forma. Cada marca que haces con él es una **instancia**: aparece en una posición concreta y puede tener un tamaño o ángulo diferente.

Esta diferencia explica por qué no debes crear diez objetos llamados `Cristal1`, `Cristal2`, `Cristal3`... Lo habitual es crear un único objeto `Cristal` y colocar diez instancias.

Tipos frecuentes:

- **Sprite:** imágenes, personajes y elementos animados.
- **Texto:** etiquetas, diálogos y marcadores.
- **Panel de texto:** cajas de conversación o interfaces.
- **Forma dibujada:** rectángulos y círculos simples.
- **Partículas:** humo, chispas, lluvia y efectos.
- **Vídeo y audio:** contenido audiovisual.
- **Objeto 3D:** modelos, planos y elementos tridimensionales, si la versión utilizada los incluye.

![Panel de objetos](https://wiki.gdevelop.io/gdevelop5/interface/scene-editor/Objects.png)

*Figura 2.2: El panel de objetos permite crear definiciones y añadir instancias. Imagen: documentación oficial de GDevelop.*

## 2.3. Sprites y animaciones

Un Sprite puede contener una o varias animaciones. Cada animación está formada por imágenes llamadas fotogramas. Para Luna, puedes crear `Quieta`, `Caminar` y `Daño`.

Consejos:

1. Usa nombres descriptivos.
2. Mantén una escala coherente entre imágenes.
3. Comprueba el punto de origen y el centro del objeto.
4. Decide qué animación debe mostrarse al empezar.
5. Cambia de animación desde eventos cuando cambie el estado del personaje.

### Paso a paso: crear a Luna

1. Abre la escena `Bosque`.
2. En el panel de objetos, elige **Añadir un objeto**.
3. Selecciona un objeto de tipo Sprite.
4. Escribe `Luna` como nombre.
5. Añade una imagen o elige un recurso de ejemplo.
6. Coloca una instancia de Luna cerca de la esquina inferior izquierda.
7. Cambia su tamaño solo si la imagen queda desproporcionada.
8. Guarda y abre la vista previa.

**Resultado esperado:** Luna aparece en el juego exactamente en la posición en la que colocaste su instancia.

Ahora repite el proceso para `Cristal`. Coloca tres instancias del mismo objeto en lugares diferentes. Si al cambiar la imagen se actualizan los tres cristales, has comprobado la diferencia entre objeto e instancia.

## 2.4. Propiedades de una instancia

Una instancia puede tener posición, tamaño, ángulo, opacidad, capa, orden Z y visibilidad. Estas propiedades determinan cómo se presenta en esa escena.

![Propiedades de una instancia](https://wiki.gdevelop.io/gdevelop5/interface/scene-editor/Properties-panel.png)

*Figura 2.3: Las propiedades permiten ajustar una instancia concreta. Imagen: documentación oficial de GDevelop.*

El **orden Z** resuelve qué objeto se dibuja delante de otro dentro de la misma capa. Las **capas** separan grupos visuales: por ejemplo, `Fondo`, `Juego` e `Interfaz`.

### Qué propiedad debes cambiar

| Quiero... | Cambio que necesito |
| :--- | :--- |
| Mover solo un cristal | Posición de su instancia |
| Girar una flecha | Ángulo de su instancia |
| Hacer que todos los cristales tengan otra imagen | Animación del objeto |
| Poner el marcador por delante | Capa u orden Z |
| Preparar un objeto que aparece más tarde | Visibilidad o creación desde un evento |

No uses el tamaño para "mover" un objeto ni el orden Z para resolver una colisión. Cada propiedad tiene una responsabilidad distinta.

## 2.5. Recursos y licencias

Los recursos son imágenes, sonidos, fuentes, vídeos y otros archivos usados por el proyecto. Antes de incorporar un recurso, comprueba su licencia, guarda la atribución cuando sea necesaria y evita descargar imágenes al azar.

Para un proyecto escolar puedes:

- crear tus propios dibujos y sonidos;
- utilizar recursos incluidos por GDevelop;
- emplear bancos con licencia compatible;
- enlazar a la fuente y conservar el texto de atribución.

## 2.6. Comportamientos

Un comportamiento añade capacidades preparadas a un objeto. Ejemplos habituales son:

- movimiento de plataformas;
- movimiento desde arriba;
- movimiento con ocho direcciones;
- física y gravedad;
- obstáculos para plataformas;
- cámara que sigue a un objeto;
- destrucción al salir de la pantalla;
- navegación o búsqueda de rutas, según la extensión.

Los comportamientos aceleran el prototipado, pero no sustituyen la comprensión de los eventos. Puedes combinar un comportamiento con reglas propias para limitar zonas, cambiar estados o reproducir sonidos.

### Paso a paso: añadir movimiento

1. Selecciona el objeto `Luna` en el panel de objetos.
2. Abre sus propiedades.
3. Busca el apartado **Comportamientos**.
4. Añade el comportamiento que corresponda al juego: plataformas, ocho direcciones o movimiento desde arriba.
5. Lee las opciones antes de aceptar: velocidad, aceleración, salto o controles pueden cambiar el resultado.
6. Vuelve a la escena y abre la vista previa.
7. Prueba una tecla cada vez.

**Resultado esperado:** Luna se mueve sin que hayas tenido que crear todavía un evento para cada dirección.

Si Luna atraviesa el suelo, el problema no tiene por qué estar en el movimiento. Comprueba que el suelo tiene el comportamiento que lo convierte en obstáculo y que ambos objetos tienen una posición y un tamaño razonables.

## Actividad: preparar el bosque

1. Crea las escenas `Menu`, `Bosque`, `Victoria` y `Derrota`.
2. En `Bosque`, crea los objetos `Luna`, `Cristal`, `Guardian` y `Suelo`.
3. Añade al menos tres instancias de `Cristal`.
4. Separa el fondo y la interfaz en capas.
5. Añade a Luna un comportamiento de movimiento apropiado para el tipo de juego elegido.
6. Ejecuta una vista previa y comprueba que todo aparece donde esperas.

### Lista de comprobación

- [ ] Las escenas tienen nombres claros.
- [ ] Cada elemento repetido usa instancias del mismo objeto.
- [ ] Luna tiene una imagen visible.
- [ ] Hay tres cristales en lugares distintos.
- [ ] El movimiento elegido corresponde al tipo de juego.
- [ ] El suelo no se confunde con una decoración sin colisión.
- [ ] Has probado el resultado antes de continuar.
