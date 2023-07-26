# streamdeck-macropad-hw
A simple handmade macropad with arduino pro micro and VIAL or QMK.
## Contenido / Content
- [streamdeck-macropad-hw](#streamdeck-macropad-hw)
  - [Contenido / Content](#contenido--content)
- [ES](#es)
  - [Case](#case)
  - [Esquema de conexión](#esquema-de-conexión)
  - [QMK/VIAL](#qmkvial)

# ES
Hacer un macropad con un arduino pro micro es fácil, ya que podemos hacerlo con VIAL o QMK.  
Solamente sería soldar, compilar y listo.

Necesitariamos:
* Cable.
* Diodos (1N4148). (uno por switch).
* Switches.
* Keycaps.
* Arduino Pro Micro USB C
* Case y Plate
* Tornillos M3x16mm.

## Case 
El case a elegir está en `case/4x4/PM_xxx`, podés elegir entre recto o inclinado (con ángulo en la base). Están hechos para tornillos M3x16mm.
Por el momento sólo tengo el modelo hecho en 4x4 para pro micro, más adelante lo voy a hacer para 3x3.

## Esquema de conexión
Para la conexión soldamos las filas con los diodos, y las columnas simplemente con cable.
Luego unimos primero las filas de arriba para abajo y después las columnas de derecha a izquierda, mirando el macropad desde las conexiones. 
![Imagen](https://i.imgur.com/dGGI7zD.png)

## QMK/VIAL
Utilizamos el método que está descripto en [este repo](https://github.com/brockar/redox-handwired-3dp#qmk), pero ponemos la carpeta `void16` (está dentro de `vial/`) en `vial-qmk/keyboards` o `qmk/keyboards`.  
Para compilar podemos hacerlo con QMK o con Vial.
Escribimos en QMK MSYS, `qmk compile -kb void16 -km default` para compilarlo en QMK.  
Escribimos en QMK MSYS, `qmk compile -kb void16 -km default` para compilarlo con VIAL.

Luego [cargamos el firmware](https://github.com/brockar/redox-handwired-3dp#cargar-firmware) y listo, ya tenemos nuestro macropad.

