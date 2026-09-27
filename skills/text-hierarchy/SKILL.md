---
name: text-hierarchy
description: Definir con el usuario la dirección visual y densidad de contenido, y ajustar jerarquía tipográfica, legibilidad y espacios al tamaño real de tarjetas, controles, formularios, tablas y secciones web. Usar al diseñar componentes o corregir textos desproporcionados, densidad o desbordes; complementa frontend-design y también funciona por separado.
---

# Text Hierarchy

Adaptá la tipografía al contenido, su importancia y el espacio disponible. Definí primero la dirección visual y la cantidad de información que necesita la experiencia. Conservá el significado y la arquitectura acordada; resolvé contenido y proporciones como un sistema.

## Integración y alcance

Si se está usando `frontend-design`, tomá su dirección estética, familias y tokens como punto de partida. Esta skill concreta densidad de contenido, tamaños, pesos, interlineados, anchos de lectura y espaciado; no modifica esa skill ni reinicia el diseño. Si se usa por separado, obtené la dirección del brief y de la interfaz existente. Las instrucciones explícitas del usuario prevalecen.

En una revisión, entregá hallazgos y correcciones propuestas. En una tarea de implementación, aplicá los ajustes autorizados y verificá el resultado. Limitá los cambios a los componentes solicitados y a los estilos compartidos necesarios, revisando su impacto en otros consumidores.

## 1. Acordar dirección y densidad

Antes de cambiar la interfaz, revisá el brief y las decisiones de la conversación. Si el usuario ya eligió una dirección, aplicala sin repetir preguntas. El estilo que hoy tiene la página es contexto, no prueba de que quiera conservarlo.

Si falta esa decisión, preguntá: «¿Hacia dónde querés llevar el diseño: minimalista, equilibrado o expresivo/maximalista?». Describí las consecuencias en lenguaje concreto:

- **Minimalista:** menos texto visible, mensajes breves, pocos niveles y más espacio entre grupos. Priorizá lo necesario para entender y actuar.
- **Equilibrado:** títulos directos, explicación breve donde aporte y detalle útil sin saturar.
- **Expresivo/maximalista:** mayor contraste de escalas y composición más intensa; la cantidad de texto depende del contenido, no de llenar el espacio.

Recomendá una opción según el propósito de la pantalla y su audiencia. Permití referencias o una dirección propia. Si no queda claro si busca limpieza visual o también menos palabras, preguntá «¿Querés conservar los textos o también simplificarlos?». Una petición explícita de «menos texto» ya autoriza esa simplificación; «minimalista» por sí solo no autoriza borrar contenido.

Separá estética de densidad: una interfaz operativa puede ser visualmente minimalista y necesitar muchos datos; una pieza maximalista puede tener una sola frase. Consultá por audiencia o acción principal solo cuando no puedan inferirse y cambien la decisión.

Antes de implementar, dejá una síntesis breve: dirección elegida, información protagonista, nivel de detalle y libertad para editar textos. Si la elección sigue pendiente, avanzá con inspección y referencias, conservando el contenido.

## 2. Inspeccionar y jerarquizar el contenido

Revisá el componente y sus variantes: contenido real, tokens, familias y pesos disponibles, tamaño e interlineado computados, ancho y alto, padding, gaps, bordes, iconos y acciones. Identificá restricciones fijas, contenido dinámico y comportamiento responsive.

Determiná qué debe leerse primero y asigná roles: título, cuerpo, etiqueta, dato destacado, ayuda y acción. Respetá la semántica de encabezados y etiquetas aunque cambie su apariencia. Terminá esta inspección con una prioridad de lectura y las restricciones concretas del contenedor.

### Decidir qué merece espacio

Para cada bloque, identificá qué ayuda a comprender, decidir o actuar y qué repite algo que ya expresa el título, el dato o la acción. Con simplificación autorizada, eliminá introducciones de relleno, rótulos redundantes y explicaciones que no aportan; condensá frases conservando su significado. Si debe conservarse el texto literal, presentá estas mejoras como propuestas.

En una dirección minimalista, comenzá por el mensaje principal y la acción necesaria. Agregá ayuda solo cuando resuelva una duda real; evitá imponer a todas las tarjetas una combinación de subtítulo, descripción, etiqueta y pie. Conservá nombres accesibles de controles y etiquetas necesarias para entender formularios.

Preservá datos, unidades, condiciones, advertencias y diferencias relevantes para decidir. El detalle secundario solo puede moverse a una vista desplegable si el alcance permite cambiar la interacción, sigue siendo accesible y no oculta información necesaria antes de actuar. Nunca reemplaces ese detalle con un recorte silencioso.

Por ejemplo, una tarjeta titulada «Reservas» con el dato «12 pendientes» no necesita además «En esta sección podés ver las reservas pendientes». Simplificar esa explicación no autoriza a quitar fechas, estados o condiciones de cada reserva.

## 3. Consultar referencias visuales

Buscá en la web referencias pertinentes de minimalismo y maximalismo para el tipo de interfaz y su audiencia. Preferí sitios originales y sistemas de diseño documentados. Seleccioná pocos ejemplos útiles, enlazá las páginas y explicá brevemente qué criterio tomás: proporción título/cuerpo, densidad, ancho de lectura, agrupación o ritmo vertical.

Inspeccioná las páginas o imágenes cuando haya herramientas disponibles; una descripción de búsqueda no demuestra su composición visual. Si no hay acceso web o visual, indicá la limitación y distinguí lo observado de lo inferido.

Si existe una dirección aprobada, usá las referencias para calibrarla, sin pedir otra elección ni mezclar estéticas por obligación. Si no existe, proponé una dirección fundamentada y consultala antes de implementar cambios visuales. Reutilizá la investigación pertinente de la tarea actual.

Minimalismo significa selección y precisión del espacio; maximalismo, abundancia organizada con focos claros. La legibilidad y la prioridad de lectura se mantienen en ambos.

## 4. Construir una escala contextual

Reutilizá los tokens del proyecto. Si faltan, definí una escala pequeña por roles y aplicala a componentes equivalentes. Como punto de partida, considerá cuerpo de 16–18 px y texto auxiliar de 14 px; son orientaciones según fuente, audiencia y densidad, no mínimos universales ni garantías de accesibilidad.

Evaluá altura de x, peso, contraste con el fondo, longitud de línea e interlineado en la fuente renderizada. Un número de píxeles aislado no determina si el texto es legible. Preferí unidades relativas para tipografía y un interlineado que tolere ampliación; cualquier escala fluida debe conservar límites legibles.

Diferenciá roles combinando tamaño, peso y espacio; el color no debe ser la única señal. Dimensioná títulos según el componente: una tarjeta no hereda la escala del hero. Acercá los elementos relacionados y separá más los grupos distintos. Mantené ritmo, alineaciones y reglas comunes entre tarjetas hermanas, aun cuando tengan distinta cantidad de texto.

## 5. Encajar sin sacrificar información

Estimá el ancho útil descontando bordes, padding y el espacio ocupado por iconos, controles y gaps en la misma fila. Para altura fija, contemplá líneas por interlineado, separaciones y elementos no textuales. Confirmá estas estimaciones con medidas del navegador cuando sea posible: la cantidad de caracteres no predice por sí sola los saltos.

Ajustá primero las inconsistencias de estilos y la asignación del espacio existente. Permití saltos naturales, corregí restricciones de flex/grid que impidan encoger el área de texto y calibrá gaps, padding e interlineado dentro de la estructura aprobada. Ajustá tamaños dentro de una escala legible y consistente, no mediante reducción automática hasta que el texto entre.

Aplicá la política de contenido acordada: texto literal cuando se pidió conservarlo, o redacción simplificada cuando esté autorizada. Conservá siempre la información esencial. No agregues truncado, line-clamp, ocultamiento, alturas nuevas ni redistribuciones para disimular un conflicto. Evitá saltos manuales que solo funcionen con una frase o viewport.

Si el texto no cabe conservando legibilidad y arquitectura, detené la corrección conflictiva: explicá qué restricción lo impide y pedí elegir entre simplificar más el texto, si es viable sin perder información esencial, o adaptar dimensiones/distribución. Presentá una propuesta concreta y continuá con ajustes independientes. Si el usuario ya autorizó esa alternativa, aplicala dentro de ese alcance.

## 6. Validar y comunicar

Cuando haya navegador disponible, verificá con las fuentes cargadas, contenido real y los estados relevantes. Usá los viewports objetivo del proyecto; si no existen, comenzá con 375 px y 1440 px de ancho y comprobá también el ancho más restrictivo del componente. Revisá ampliación al 200 % y, si es posible, ampliación solo del texto.

Comprobá que el texto siga visible y legible, sin desbordes accidentales, superposiciones, cortes ni acciones desplazadas fuera del área utilizable. Revisá contraste, orden de lectura, consistencia entre pares y conservación de información y semántica. Si una restricción impide superar la comprobación, reportala como pendiente de decisión.

Usá estos escenarios según correspondan:

| Escenario | Resultado esperado |
| --- | --- |
| Tarjeta pequeña con título largo | Título acordado completo con saltos naturales y jerarquía local, sin reducirlo hasta volverlo ilegible. |
| Tarjetas hermanas con contenido desigual | Misma escala y reglas de espacios; diferencias de contenido no crean estilos arbitrarios. |
| Pedido de minimalismo sin definir libertad editorial | Consulta si debe conservar o simplificar textos antes de eliminarlos. |
| Pedido explícito de menos texto | Elimina redundancias y acorta redacción sin pedir autorización por cada frase; preserva datos y condiciones. |
| Dirección ya acordada | Aplica esa decisión sin volver a abrir la consulta. |
| Diseño maximalista con poco contenido | Usa composición y escala expresivas sin inventar párrafos de relleno. |
| Interfaz densa | Etiquetas, datos y acciones se distinguen sin depender exclusivamente del color o texto diminuto. |
| Página maximalista | Expresividad compatible con un foco dominante, lectura clara y contraste suficiente. |
| Componente de altura fija cuyo texto no entra | Conflicto explicado y decisión solicitada; contenido y estructura preservados mientras tanto. |
| Móvil y texto ampliado | Información accesible sin recortes ni superposiciones; límites incompatibles identificados. |

Cerrá con la dirección aplicada, los ajustes realizados o propuestos (incluyendo qué se simplificó), las referencias usadas y la verificación efectivamente ejecutada. Distinguí revisión de código, medición de layout e inspección visual. Si no pudiste renderizar, indicá que la validación visual queda pendiente; no la presentes como aprobada.
