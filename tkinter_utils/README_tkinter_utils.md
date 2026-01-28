## __tkinter_utils__

Esta carpeta contiene una serie de utilidades reutilizables en Python que facilitan la configuración de GUI's (interfaces de usuario) usando la libreria tkinter de forma limpia, dinámica y escalable mediante el uso de kwargs.

No pretende ser una refactorización completa de la libreria tkinter sino más bien __un sistema hibrido donde se pueden combinar atributos (y métodos) nativos de tkinter con atributos (y métodos) personalizados__ que simplifican en gran medida el código cuando se configuran GUI's con tkinter en otros proyectos.

Esta carpeta ira incorporando con el tiempo __nuevas versiones incrementales, cada una se almacenara en una subcarpeta distinta__  a medida que necesite incorporar más widgets personalizados en mis proyectos personales (que también publicare en Github). No hay fechas previstas para estas futuras implementaciones.

---

## __v1.0__

__Fecha implementación__: 19/01/2026

La carpeta se compone de 3 ficheros:

* __tkinter_utils_v1_0__: fichero .py que contiene el sistema que se ha de incorporar en los proyectos Python donde se quiera usar.
* __EJEMPLO_USO_tkinter_utils_v1_0__: fichero .py con los ejemplos que se documentan en el manual que se comenta a continuación.
* __MANUAL_tkinter_utils_v1_0__: fichero pdf que explica el sistema y lo ilustra con ejemplos documentados de como implementarlo en otros proyectos.

Se adjuntan asismismo 2 archivos para que funcionen los ejemplos:

* __ico_tapar_pluma_tkinter__: es un archivo .ico que se usa en el módulo .py de ejemplos.
* __png_para_boton__: es un archivo .png que se usa en el módulo .py de ejemplos.

Se incorporara en el futuro un log de errores de configuración de kwargs que ayude al usuario para entender porque no se configura correctamente su GUI. A dia de hoy, los errores de configuración se omiten lo que exige al usuario ser muy meticuloso en la configuración.

__Actualización (22/01/2026)__

Ser han modificado los archivos siguientes:
* __tkinter_UTILS_v1_0__
* __EJEMPLO_USO_tkinter_UTILS_v1_0__
* __MANUAL_tkinter_UTILS_v1.0__

```
CORRECIONES:

frame_con_scrollbar: --> cuando se configuraba tupla_coord_place = (0, 0) no generaba
                         correctamente el objeto.

                     --> generaba error cuando se hacia llamada a la clase sin tener
                         dicc_frame_scrollbar configurado en los kwargs.

treeview_propio: no se generaba correctamente el borde a la derecha del titulo la última columna.

controltiptext: generaba un error al usar el atributo propio en otros widgets que no fueran botones.
```
```
MEJORAS (clase entry_propio)

Se introduce una mejora en la clase entry_propio para hacer las validaciones
más flexibles para el usuario al intentar salir de un entry.
Se incorpora la posibilidad para el usuario de crear en su proyecto
una función personalizada de validación de datos (de momento en el módulo de su GUI)
que se integra dentro de los kwargs de configuración de un objeto entry_propio.
No requiere retocar el código de la clase entry_propio.

Se ha retocado el documento MANUAL_tkinter_UTILS_v1.0 tanto en la explicación
de la clase entry_propio como en el ejemplo 7 de los anexos.
```
Las clases siguientes (gui_tkinter_widgets, entry_propio y treeview_propio) a dia de hoy cuando
se les asigna una rutina (o función) esta última tiene que estar declarada en el mismo módulo Python
donde se realiza la llamada a la clase. __La semana que viene (semana del 26/01/2026) subire una mejora que permitira usar
rutinas (o funciones) declaradas en otros módulos Python__.

__Actualización (28/01/2026)__

Las actualizaciones comentadas en el bloque __Actualización (22/01/2026)__ se posponen a la semana del 02/02/2026. Se publicaran como una nueva versión (v1.1), habran otros añadidos no comentados, Esta nueva versión sirve de base a otro proyecto que publicare también en Github la misma semana en un nuevo repositorio.


