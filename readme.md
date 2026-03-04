## 1. El JSON como "Contrato de Datos"
En la primera entrega, el JSON era solo una forma de ordenar el texto. Ahora, lo tratas como un interfaz técnica.

Explicación: Al optimizar las claves (los nombres de los campos en el JSON), obligas al modelo a "encajonar" su razonamiento. Si el prompt de la Etapa 2 sabe que siempre recibirá un campo llamado punto_critico, no tiene que "adivinar" qué es lo más importante del texto original; simplemente lee ese campo. Esto elimina la variabilidad y hace que el sistema sea confiable.

## 2. Encadenamiento (Chaining) y Eficiencia
Aquí es donde aplicas el Fast Prompting puro.

Explicación: En la Entrega 1, el proceso era: Input -> Prompt 1 -> Output 1 -> (Manual) -> Prompt 2 -> Output 2.

En esta Entrega 2, el proceso es: Input -> Sistema Orquestado -> Output Final.
Al reducir la cantidad de interacciones manuales y agrupar instrucciones, reduces la latencia (el tiempo que tarda en responder) y el consumo de tokens (el costo), porque no tienes que volver a explicarle el contexto a la IA en cada paso.

## 3. Ingeniería de Visión y Control de Artefactos
Las imágenes generadas por IA suelen fallar cuando intentan escribir texto o cuando el concepto es muy abstracto.

Internalización al Inglés: Los modelos como DALL-E o Midjourney fueron entrenados mayoritariamente en inglés. Traducir el concepto automáticamente asegura que la IA entienda las sutilezas técnicas (por ejemplo, "Nuclear Fuel Cycle" es mucho más preciso para la IA que su traducción al español).

Control de Artefactos (Negative Constraints): Al añadir "No text, no letters", aplicas una restricción negativa. Esto le dice al modelo qué no hacer, lo cual es vital en infografías para evitar que aparezcan caracteres extraños que restan profesionalismo al activo visual.

## 4. Viabilidad y Rentabilidad (El enfoque de Negocio)
Un proyecto de IA puede ser muy bueno, pero si consume demasiados recursos, no es viable.

Explicación: Al fraccionar las tareas, permites que el sistema use modelos más pequeños y baratos para tareas simples (como el JSON) y reserve el "poder de cómputo" caro solo para la generación final. El uso de formatos ligeros (JSON) facilita que esta herramienta se pueda integrar en una página web o una app móvil sin que el servidor colapse.