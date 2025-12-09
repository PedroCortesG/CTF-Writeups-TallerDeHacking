Corresponde a la practica de esconder un mensaje dentro de otro mensaje u objeto (sea texto, imagen, audio, etc). Se usan diferentes herramientas para esconder y encontrar estos mensajes.

### Codificaciones de texto a binario:
Consiste en transmitir datos arbitrarios (generalmente binarios) por otro medio que solo acepta una cantidad limitada de caracteres. Tipos:
- Base64: Codifica bytes arbitrarios usando caracteres A..Z,a...z,0...9,+,/,=(padding al final). Se representa cada conjunto de 6 bits con un caracter del alfabeto Base64. Esto es, si tenemos un dato tipo "01001010110101" esto es "010010 101101 01" que luego pasa a ser 3 simbolos que estan representados por esos 6 bits cada uno.
- Base32: Lo mismo que Base 32 pero con 5 bits, esto es usando alfabeto A...Z,2...7,=.
- Otras: Siguen la misma idea de BaseXX, una importante es 58 que es para direcciones publicas de Bitcoin.
### Codificación en Lenguajes de Programacion Esotéricos (Esolangs):
Consiste en la codificacion de mensajes usando lenguajes de programacion raritos, por ejemplo:
- Chef: Archivos con texto del tipo receta, con ingredientes, preparacion y porciones.
- Piet: Lenguaje de programación cuyos archivos interpretables son imagenes.
- Whitespace: El interprete del archivo solo considera los espacios, tab y enter en el archivo de texto. Tiene texto normal para que parezca un archivo de texto normal, pero realmente solo importa lo antes mencionado.

### Ofuscación de código
Consiste en aprovechar caracteristicas propias de cada lenguaje de programacion para que no se entienda una o mas lineas. Como escribir una funcion compleja entera en solo 1 linea en C, aprovechandose que basta usar ; despues de cada llamada para que el compilador lo interprete bien. Programas:
- Para ofuscar: Bashfuscator (Bash), Invoke-Obfuscation (Powershell), obfuscator.io (JS)
- Para desofuscar: de4js (JS), jsnice.

### Herramientas para transformar codificaciones:
- Cyebrchef
- Dcode
- Cryptii

## Criptografia Clasica
Los cifradores clásicos fueron muy importantes historicamente, pero hoy en dia son muy facil de romper con ayuda del pc. Suelen trabajar solo con letras del alfabeto inglés, lo que limita los mensajes a cifrar. En general, se __ignoran los espacios y signos de puntuación__.
