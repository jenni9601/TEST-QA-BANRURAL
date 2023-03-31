# Plan de ataque - Juego adivina tu número

## Lista de defectos detectados

A continuación, se detallan los hallazgos detectados durante el testeo de la apliación, así como la solución implementada.

|Id defecto|Descripción del defecto |Detalle de la solución |Tester | 
|----------|------------------------|-----------------------|-----------------------|
|DEF-001|Se detectó que el aplicativo aceptaba números negativos y con punto decimal.|A nivel de html se cambio la propiedad type="text" a type="number" del input "guessField" para que al usuario unicamente le permita el ingreso de números, asimismo, a nivel de javascript se validó que el usuario no ingresara números negativos ni con punto decimal.|Jennifer Contreras|
|DEF-002|El número random que generaba el aplicativo unicamanete se generaba de 0 a 9 y con decimales.|El valor de la función Math.random() se multiplicó por 100 y luego se aplicó un redondeo para que el número a adivinar sea un número entre 1 y 100. Quedando de la siguiente manera: let randomNumber = Math.round(Math.random() * 100);|Jennifer Contreras|
|DEF-003|La cantidad de intentos para adivinar el número random se encontraba en 5|Se cambió el valor de intentos a 10. |Jennifer Contreras|
|DEF-004|El valor de la contante lowOrHi se encontraba en nulo|Existía un error de sintaxis al identificar el selector, el error estaba en la falta de un punto en la instrucción: const lowOrHi = document.querySelector(**'.lowOrHi'**); |Jennifer Contreras|
|DEF-005|La sintaxis en la instrucción if del método checkGuess() se encontraba implementada incorrectamente.|Se cambió la lógica de las condiciones, asimismo, se aplicó el formato de color respectivamente según los requerimientos establecidos. Texto rojo al llegar a la cantidad de intentos máximos, texto verde al adivinar el número y texto negro cuando el número era incorrecto.|Jennifer Contreras|
|DEF-006|La sintaxis del listener para el objeto "guessSubmit" se encontraba mal escrita, por lo cual la aplicación no reconocía el método.|Se corrigió el nombre del método de add**e**ventListener a add**E**ventListener |Jennifer Contreras|
|DEF-007|La sintaxis del listener para el objeto "resetButton" se encontraba mal escrita, por lo cual la aplicación no reconocía el método.|Se corrigió el nombre del método de add**e**ventListener a add**E**ventListener |Jennifer Contreras|
