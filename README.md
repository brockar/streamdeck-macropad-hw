# streamdeck-macropad-hw
A simple handmade macropad with arduino pro micro and VIAL or QMK.
## Contenido / Content
- [streamdeck-macropad-hw](#streamdeck-macropad-hw)
  - [Contenido / Content](#contenido--content)
- [ES](#es)
  - [Case](#case)
  - [Esquema de conexión](#esquema-de-conexión)
  - [QMK/VIAL](#qmkvial)
- [EN](#en)
  - [Case](#case-1)
  - [Connection diagram](#connection-diagram)
  - [QMK/VIAL](#qmkvial-1)

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

# EN
Making a macropad with an arduino pro micro is easy, since we can do it with VIAL or QMK.  
It would only be soldering, compiling and ready.

We would need:
* Cable.
* Diodes (1N4148). (one per switch).
* Switches.
* Keycaps.
* Arduino Pro Micro USB C
* Case and Plate
* 4x M3x16mm screws.

## Case 
The case to choose is in `case/4x4/PM_xxx`, you can choose between straight or slanted (angled at the base). They are made for M3x16mm screws.
At the moment I only have the model made in 4x4 for pro micro, later I will make it for 3x3.

## Connection diagram
For the connection we solder the rows with the diodes, and the columns simply with wire.
Then we join first the rows from top to bottom and then the columns from right to left, looking at the macropad from the connections. 
![Image](https://i.imgur.com/dGGI7zD.png)

## QMK/VIAL
We use the method that is described in [this repo](https://github.com/brockar/redox-handwired-3dp#qmk), but we put the `void16` folder (it is inside `vial/`) in `vial-qmk/keyboards` or `qmk/keyboards`.  
To compile we can do it with QMK or with Vial.
We write in QMK MSYS, `qmk compile -kb void16 -km default` to compile it in QMK.  
Type in QMK MSYS, `qmk compile -kb void16 -km default` to compile with VIAL.

Then [load the firmware](https://github.com/brockar/redox-handwired-3dp#cargar-firmware) and that's it, we have our macropad.