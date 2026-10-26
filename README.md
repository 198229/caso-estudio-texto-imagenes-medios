# Caso de estudio: textos erróneos en imágenes de medios

Análisis de dos casos de texto que acompaña imágenes en notas de medios argentinos: un pie de foto que describía a una persona herida como un disfraz, y un texto alternativo copiado del pie de foto. El objetivo es mostrar cómo verificar el origen de un error antes de atribuirle una causa.

## Qué se encontró

**Caso 1: Infobae (30/09/2026).** En una nota sobre una emergencia aérea, el pie de foto describía la imagen de una persona herida con máscara de oxígeno como "una persona con disfraz y maquillaje durante un festejo". El atributo `alt` de la misma imagen decía otra cosa, una descripción neutra. Se reportó el caso y el pie fue corregido a más tardar el 01/10/2026.

**Caso 2: La Nación (26/10/2026).** El `alt` de una foto de agencia es una copia exacta del pie de foto, incluido un error de redacción, y nombra a cuatro personas cuando la imagen recortada muestra dos. El mismo texto aparece en `og:image:alt`.

## Qué se verificó y qué no

| Verificado | No verificado |
|---|---|
| El pie erróneo existió (captura y código archivado) | Quién o qué produjo el pie erróneo |
| El `alt` era distinto del pie | Si el reporte causó la corrección |
| El pie fue corregido | Si hubo otras notas afectadas |
| En La Nación, el `alt` copia el pie | |

El informe no atribuye el error de Infobae a un sistema de IA, porque no hay evidencia para afirmarlo.

## Medidas propuestas

Valen sin importar quién produjo el texto (persona, plantilla o modelo):

1. Revisión humana obligatoria de pies de foto y textos alternativos en notas de emergencia, tragedia o conflicto.
2. Validación de coherencia entre la nota, el pie y el `alt` antes de publicar.
3. Escribir el `alt` aparte del pie, en lugar de copiarlo.
4. `alt` más informativo en emergencias.
5. Si hay un modelo en el proceso: contexto editorial como entrada, umbral calibrado con datos reales y derivación a revisión humana.
6. Set de pruebas con imágenes sensibles antes de cada cambio de proceso o modelo.

## Contenido del repositorio

- `Informe_Incidente_Infobae_v3.pdf`: informe completo con capturas, código y copias archivadas.

## Evidencia archivada

- Infobae, antes: https://archive.ph/08u7S
- Infobae, después: https://ghostarchive.org/archive/KiREG
- La Nación: https://ghostarchive.org/archive/3LOnF

## Autor

Diego Leonardi · [LinkedIn](https://www.linkedin.com/in/die1982)
