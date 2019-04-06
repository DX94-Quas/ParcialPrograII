Diferencias entre lenjuage interpretado y compilado
-------
* el lenguaje interpretado solo necesita el archivo donde esta contenido el programa para ejecutarlo, el compilado solo puede ejecutarse si se tiene el programa ya en codigo maquina despues de compiar
* el lenguaje compilado es mas rapido por que las instrucciones estan en codigo maquina, el lenguaje interpretado debe primero traducir el texto del programa en codigo legible al sistema primero cada vez que el programa se ejecuta
* el lenguaje interpretado es mas portatil ya que solo se necesita adaptar el entorno sobre el que corre al sistema en cuestion. El lenguaje compilado puede requerir que el codigo se adapte segun el sistema sobre el que se vaya a ejecutar

Pasos de Compilacion de un programa en c++
----
* el programa se pasa primero al preprocesador `cpp` que ejecuta macros como `#include` o `#define`. da un archivo en `.i`
* el programa se pasa al compilador, `g++` que toma el archivo anterior y traduce el codigo expandido en c++ a lenguaje ensablador, produce un archivo `.as`
* luego este archivo en lenguaje ensamblador se pasa al assembler `as` que produce ya un codigo objeto `.o`, este aun no se puede ejectutar
* para ejecutarse necesita llevarse el codigo objeto al linker `ld` que enlaza o muestra al programa donde estan las diferentes librerias del sistema que necesita para su ejecucion