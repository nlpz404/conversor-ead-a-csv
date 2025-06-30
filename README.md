# Conversor EAD a CSV/XLSX para importación en AtoM

Este programa transforma registros en formato EAD 2002 XML a archivos CSV o XLSX, facilitando el respaldo, la edición e importación masiva de descripciones archivísticas en AtoM.

Diseñado en HTML para su utilización offline. La exportación a XLSX, sin embargo, utiliza la librería SheetJS y requiere conexión a internet.

## Uso

El programa fue desarrollado con la intención de generar respaldos y editar descripciones archivísticas del Archivo General de la Nación (Argentina) alojadas en AtoM. El flujo de trabajo previsto es: exportar los registros en formato EAD XML desde la interfaz de AtoM, convertirlos a CSV o XLSX para su edición utilizando este conversor, y luego importar el CSV actualizado en AtoM.

Debido a que el XML refleja la estructura jerárquica (de arriba a abajo) a partir de la descripción exportada en AtoM, y el AGN utiliza nombres de nivel que difieren del estándar definido en EAD, el usuario deberá seleccionar en la interfaz del conversor los nombres de nivel representados en el XML.

El código infiere la jerarquía a partir del atributo `level` en el XML. Si el valor del atributo difiere del estándar ISAD, se inferirá la jerarquía a partir de la profundidad de anidamiento en la estructura del XML, mapeando los nombres de nivel seleccionados por el usuario.

## Licencias

Este proyecto está licenciado bajo la **GNU General Public License versión 3 (GPLv3)**.

Algunos componentes incluidos en este proyecto, como la librería **SheetJS**, están licenciados bajo la **Apache License 2.0**.

Para más información, consulte los archivos `LICENSE` (GPLv3) y `LICENSE-APACHE` (Apache 2.0) incluidos en este repositorio.

## Contacto
El código está diseñado para ser modificado y reutilizado por otras instituciones que trabajen con descripciones archivísticas en AtoM. Su licencia GPLv3 lo permite expresamente.

Para consultas, sugerencias o contribuciones, podés contactarme a: malopez@mininterior.gob.ar
