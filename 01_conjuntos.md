GUIA DE ESTUDIO: MATEMATICAS DISCRETAS - MODULO 1: CONJUNTOS
=============================================================

Bienvenido. Este documento esta redactado para leerse de corrido, como si fuera una explicacion hablada, sin formulas raras de programacion, sin codigos LaTeX y sin tablas que corten la lectura.


PARTE 1: LA DIFERENCIA ENTRE PERTENENCIA (∈) E INCLUSION (⊆)
-------------------------------------------------------------

Esta es la trampa principal de los examenes. La mayoria de estudiantes reprueba esta parte porque confunden pertenecer con estar incluido. Vamos a entenderlo con una analogia muy sencilla.

Imagina que un conjunto es una caja. Todo lo que metas dentro de esa caja, tal cual como este empacado, es un elemento.

1. Pertenencia (simbolo ∈):
Cuando te preguntan si algo PERTENECE a un conjunto (por ejemplo, x ∈ A), lo unico que tienes que hacer es asomarte a la caja y buscar si ese objeto exacto esta alli adentro, exactamente igual a como esta escrito. Si esta identico, es VERDADERO. Si le falta algo o le sobra algo (incluso unas llaves), es FALSO.

2. Inclusion (simbolo ⊆):
Cuando te preguntan si un conjunto esta INCLUIDO en otro (por ejemplo, A ⊆ B), ya no estas buscando un objeto suelto. Estas afirmando que todos los miembros del primer grupo tambien estan adentro del segundo grupo.
Para no enredarte jamas con las llaves, usa esta regla practica:
Toma lo que esta a la izquierda del simbolo ⊆ y quitale las llaves de afuera. Los elementos que te queden sueltos deben estar adentro del conjunto de la derecha. Si todos estan adentro, es VERDADERO.
Ademas, hay una regla universal que debes memorizar: el conjunto vacio (∅) siempre esta incluido en cualquier conjunto. Por lo tanto, ∅ ⊆ A es SIEMPRE VERDADERO, sin importar que conjunto sea A.


PARTE 2: EL EJERCICIO CLAVE DEL TALLER RESUELTO DE CORRIDO
----------------------------------------------------------

En tu taller aparece este conjunto especifico:
E = { a, {a}, ∅ }

Fijate bien en lo que hay adentro de la caja E. Tiene exactamente tres cosas distintas:
- Primera cosa: la letra simple 'a'.
- Segunda cosa: una cajita que contiene a la letra 'a', es decir, '{a}'. Aqui las llaves forman parte del nombre del elemento.
- Tercera cosa: el simbolo del conjunto vacio '∅'.

Ahora analicemos las 8 preguntas del taller de corrido:

Pregunta 1: ¿a ∈ E?
Respuesta: VERDADERO. Nos asomamos a la caja E y vemos la letra 'a' suelta, exactamente igual.

Pregunta 2: ¿{a} ∈ E?
Respuesta: VERDADERO. Nos asomamos a la caja E y vemos que efectivamente existe un elemento llamado '{a}' (con sus llaves).

Pregunta 3: ¿a ⊆ E?
Respuesta: FALSO. Para hablar de inclusion (⊆), el lado izquierdo debe ser un conjunto, es decir, debe tener llaves. La letra 'a' sola es un elemento simple, no un conjunto.

Pregunta 4: ¿{a} ⊆ E?
Respuesta: VERDADERO. Aplicamos la regla: le quitamos las llaves a '{a}' y nos queda la letra 'a'. ¿Esta la letra 'a' adentro de E? Si, la vimos en la pregunta 1. Por lo tanto, el conjunto {a} si esta incluido en E.

Pregunta 5: ¿{{a}} ⊆ E?
Respuesta: VERDADERO. Aplicamos la misma regla: le quitamos las llaves exteriores a '{{a}}' y nos queda '{a}'. ¿Existe el elemento '{a}' adentro de E? Si, es el segundo elemento de la caja. Por lo tanto, {{a}} esta incluido en E.

Pregunta 6: ¿∅ ∈ E?
Respuesta: VERDADERO. Solo es verdadero porque dentro de E el profesor escribio explicitamente el simbolo ∅. Si no estuviera escrito adentro de las llaves, seria falso.

Pregunta 7: ¿∅ ⊆ E?
Respuesta: VERDADERO. Recuerda la regla universal: el conjunto vacio siempre es subconjunto de cualquier conjunto existente. Esta afirmacion siempre sera verdadera en cualquier examen.

Pregunta 8: ¿{∅} ⊆ E?
Respuesta: VERDADERO. Le quitamos las llaves a '{∅}' y nos queda el simbolo ∅. Como ∅ pertenece a E (lo vimos en la pregunta 6), entonces {∅} esta incluido en E.


PARTE 3: CONJUNTOS POR COMPRENSION Y POR EXTENSION
--------------------------------------------------

Definir por extension significa hacer una lista con todos los elementos, uno por uno: por ejemplo, {1, 2, 3}.
Definir por comprension significa dar la regla o propiedad que cumplen esos elementos: por ejemplo, "los numeros enteros positivos menores que 4".

La trampa en los parciales esta en el universo que te dan al principio:
- Si te dicen N (Numeros Naturales), son los enteros positivos: 1, 2, 3, 4, ... (no se admiten negativos ni fracciones).
- Si te dicen Z (Numeros Enteros), se admiten positivos, negativos y el cero: ..., -2, -1, 0, 1, 2, ...

Resolvamos los ejercicios del taller de corrido:

Ejercicio 1: A = { x ∈ N tal que x^2 - 5x - 6 = 0 }
Aqui tenemos una ecuacion cuadratica. Al resolverla o factorizarla buscando dos numeros que multiplicados den -6 y sumados den -5, obtenemos (x - 6)(x + 1) = 0.
Esto nos da dos posibles soluciones: x = 6 y x = -1.
Pero mucho cuidado con la trampa: la condicion dice que x debe pertenecer a N (numeros naturales). Como -1 es un numero negativo, no pertenece a los naturales y lo descartamos.
Por lo tanto, la solucion por extension es unicamente:
A = {6}

Ejercicio 2: B = { x tal que x es una letra de la palabra "excusa" }
Las letras que forman la palabra son e, x, c, u, s, a.
En teoria de conjuntos los elementos repetidos no se vuelven a escribir y el orden no cambia el conjunto.
Por lo tanto, por extension queda:
B = {a, c, e, s, u, x}

Ejercicio 3: C = { x ∈ Z tal que x^2 - 9 = 0  o  2x - 1 = 9 }
Tenemos dos condiciones unidas por la palabra "o", lo que significa que cualquier solucion de cualquiera de las dos ecuaciones es valida.
En la primera ecuacion: x^2 - 9 = 0 significa que x^2 = 9, cuyas soluciones son 3 y -3. Ambos son enteros (pertenecen a Z).
En la segunda ecuacion: 2x - 1 = 9, pasamos el 1 a sumar: 2x = 10, luego x = 5. Tambien es entero.
Juntamos todas las respuestas encontradas:
C = {-3, 3, 5}

Ejercicio 4: D = { x ∈ N tal que 2 <= x < 7 }
Buscamos los numeros naturales que sean mayores o iguales a 2, pero estrictamente menores que 7.
Incluimos el 2 (porque tiene el signo menor o igual), pero el 7 no entra (porque tiene solo menor).
Por extension queda:
D = {2, 3, 4, 5, 6}

Ejercicio 5: E = { x ∈ Z tal que |x| < 3 }
El valor absoluto menor que 3 significa que buscamos numeros enteros cuya distancia al cero sea menor que 3. Es decir, numeros estrictamente entre -3 y 3.
Por extension son:
E = {-2, -1, 0, 1, 2}


PARTE 4: ESCRIBIR POR COMPRENSION CONJUNTOS DADOS POR EXTENSION
---------------------------------------------------------------

Ahora hacemos el camino inverso: nos dan la lista y debemos descubrir el patron para escribir la formula.

Conjunto F = {2, 4, 6, 8, 10}
Observamos que son numeros pares positivos que van desde el 2 hasta el 10.
Podemos escribirlo en palabras matematicas como:
F = { x ∈ N tal que x es par y 2 <= x <= 10 }
O tambien con formula: F = { 2k con k ∈ N, 1 <= k <= 5 }

Conjunto G = {1, 4, 9, 16, 25}
Observamos los numeros: 1 al cuadrado es 1, 2 al cuadrado es 4, 3 al cuadrado es 9, 4 al cuadrado es 16, y 5 al cuadrado es 25. Son cuadrados perfectos.
Por comprension queda:
G = { x^2 con x ∈ N, 1 <= x <= 5 }

Conjunto H = {..., -6, -3, 0, 3, 6, ...}
Los puntos suspensivos a ambos lados indican que va al infinito positivo y negativo. Son todos los multiplos de 3.
Por comprension queda:
H = { 3k con k ∈ Z }

Conjunto I = {1, 3, 5, 7, 9, 11}
Son los numeros impares positivos que llegan hasta el 11.
Por comprension queda:
I = { x ∈ N tal que x es impar y 1 <= x <= 11 }
O con formula: I = { 2k - 1 con k ∈ N, 1 <= k <= 6 }
