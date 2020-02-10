# Proyecto de datos


La base de datos elegida para el trabajo es la de [Incidentes viales reportados por C5](https://datos.cdmx.gob.mx/explore/dataset/incidentes-viales-c5/information/?disjunctive.incidente_c4), que contiene el conjunto de datos con los incidentes viales reportados por el Centro de Comando, Control, Cómputo, Comunicaciones y Contacto Ciudadano de la Ciudad de México (C5) desde 2014 y actualizado mensualmente.

## Definición del proyecto

En este conjunto se reporta: folio, fecha de creación del reporte, hora de creación del reporte, día de la semana de creación del reporte, fecha de cierre de reporte, hora de cierre de reporte, alcaldía donde sucedió el incidente, motivo del incidente dependiendo del tipo de emergencia, latitud y longitud del incidente, clasificación del incidente, medio por el cual se dió aviso del incidente, alcaldía en que se dio resolución al incidente o emergencia.

Los registros que se reciben en el C5 se clasifican internamente por medio de un código de cierre:

A = “Afirmativo”: Una unidad de atención a emergencias fue despachada, llegó al lugar de los hechos y confirmó la emergencia reportada

N = “Negativo”: Una unidad de atención a emergencias fue despachada, llegó al lugar de los hechos, pero en el sitio del evento nadie confirmo la emergencia ni fue solicitado el apoyo de la unidad

I = “Informativo”: Corresponde a solicitudes de información

F = “Falso”: El incidente reportado inicialmente fue considerado como falso en el lugar de los hechos.

D = “Duplicados”: El incidente reportado se registró en dos o más ocasiones procediendo a mantener un solo reporte como el original. Para el uso e interpretación correctos de la información, debe considerarse:

Cada incidente registrado genera un folio único identificador, excepto las llamadas no procedentes o “falsas” (bromas, niños jugando, etc.) que se reciben por distintos medios.  Mientras un folio está abierto; es decir, mientras el registro está siendo atendido, éste no se carga en la base de datos interna, una vez que el folio ha sido cerrado éste se refleja en el sistema y es posible visibilizarlo internamente con un día de vencimiento, pues se realiza una recarga diaria (por esta razón las fechas de inicio y cierre de folio no necesariamente coinciden).

El proyecto tiene como objetivo crear un modelo para clasificar cada incidente según el código de cierre establecido actualmente. La utilidad en este producto de datos recide en poder priorizar con antelación cada uno de los incidentes antes de ser atendido, de manera de poder eficientar la atención y operación en temas de seguridad pública, urgencias médicas, medio ambiente, protección civil, movilidad y servicios a la comunidad en la capital del país.

## Diseño del producto de datos (mockup)

El producto de datos a entregar sería un tablero que le de al usuario la posible clasificación (e incluso una segunda opción) del incidente, con base en la información disponible. De esta manera el usuario podrá valorar la prioridad de cada incidente.
