# Módulo 1: Teoría de Conjuntos — Entrenamiento de Dominio Acelerado

> **Metodología de Aprendizaje Acelerado (4 Pasos):**
> 1. 🧠 **Algoritmo Mental:** La regla o procedimiento exacto paso a paso.
> 2. 👁️ **Ejemplo Modelo:** Observa el proceso aplicado punto por punto.
> 3. ✍️ **Tu Turno (Ejercicio Espejo):** Resuelve un problema idéntico por tu cuenta aplicando el algoritmo.
> 4. 🔍 **Solución y Checkpoint:** Despliega la solución para verificar tu resultado y detectar posibles trampas.

---

## Bloque 1: Pertenencia ($\in$) vs. Inclusión ($\subseteq$)

### 1. 🧠 Algoritmo Mental de Decisión

#### Para evaluar Pertenencia ($x \in A$):
- **Paso 1:** Abre mentalmente las llaves del conjunto $A$.
- **Paso 2:** Busca si el objeto $x$ de la izquierda aparece **literal e idéntico** en la lista de elementos (con o sin llaves, exactamente igual a como está escrito).
- **Paso 3:** Si aparece idéntico $\rightarrow$ **VERDADERO**. Si no está idéntico $\rightarrow$ **FALSO**.

#### Para evaluar Inclusión ($X \subseteq A$):
- **Paso 1 (Regla Universal):** ¿El lado izquierdo es el conjunto vacío ($\emptyset$)? Si es $\emptyset \subseteq A$ $\rightarrow$ **VERDADERO SIEMPRE**.
- **Paso 2 (Verificación de llaves):** ¿Tiene el lado izquierdo llaves exteriores? Si es un elemento simple suelto sin llaves (ejemplo: $3 \subseteq A$) $\rightarrow$ **FALSO DE INMEDIATO** (un elemento individual no puede estar incluido).
- **Paso 3 (Regla del destape):** Retira **únicamente** el par de llaves más exterior de $X$.
- **Paso 4:** Verifica si **cada uno** de los elementos que quedaron dentro pertenece individualmente a $A$.
- **Paso 5:** Si todos pertenecen $\rightarrow$ **VERDADERO**. Si falla aunque sea uno $\rightarrow$ **FALSO**.

---

### 2. 👁️ Ejemplo Modelo: Conjunto Anidado de Examen
Consideremos el conjunto:
$$E = \{ a, \{a\}, \emptyset \}$$

Tiene exactamente 3 elementos:
1. La letra suelta: $a$
2. El subconjunto empaquetado: $\{a\}$
3. El símbolo de vacío: $\emptyset$

| Proposición | Proceso Mental Paso a Paso | V/F |
| :--- | :--- | :---: |
| **$a \in E$** | Buscamos la letra $a$ suelta en la caja $\rightarrow$ Aparece idéntica. | **V** |
| **$\{a\} \in E$** | Buscamos el paquete $\{a\}$ $\rightarrow$ Aparece idéntico como 2.° elemento. | **V** |
| **$a \subseteq E$** | No tiene llaves exteriores. Un elemento no se incluye en un conjunto. | **F** |
| **$\{a\} \subseteq E$** | Quitamos llaves exteriores: queda $a$. Como $a \in E$ (es el 1.° elemento) $\rightarrow$ V. | **V** |
| **$\{\{a\}\} \subseteq E$** | Quitamos llaves exteriores: queda $\{a\}$. Como $\{a\} \in E$ (es el 2.° elemento) $\rightarrow$ V. | **V** |
| **$\emptyset \in E$** | Buscamos $\emptyset$ en la caja $\rightarrow$ Está escrito explícitamente como 3.° elemento. | **V** |
| **$\emptyset \subseteq E$** | Regla de oro universal: el vacío es subconjunto de cualquier conjunto. | **V** |
| **$\{\emptyset\} \subseteq E$** | Quitamos llaves: queda $\emptyset$. Como $\emptyset \in E$ (por el 3.° elemento) $\rightarrow$ V. | **V** |

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 1
Aplica el algoritmo anterior sobre este nuevo conjunto de evaluación:
$$K = \{ 7, \{7\}, \{2\}, \emptyset \}$$

Resuelve en tu cuaderno u hoja de práctica si cada proposición es **V** o **F**:
1. $7 \in K$
2. $\{7\} \in K$
3. $7 \subseteq K$
4. $\{7\} \subseteq K$
5. $\{\{7\}\} \subseteq K$
6. $2 \in K$
7. $\{2\} \in K$
8. $\{2\} \subseteq K$
9. $\{\{2\}\} \subseteq K$
10. $\emptyset \in K$
11. $\emptyset \subseteq K$
12. $\{\emptyset\} \subseteq K$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 1</b></summary>

| Reactivo | Resultado | Justificación con el Algoritmo |
| :--- | :---: | :--- |
| 1. $7 \in K$ | **V** | El número $7$ suelto es el primer elemento de la caja. |
| 2. $\{7\} \in K$ | **V** | El objeto $\{7\}$ con llaves es el segundo elemento de la caja. |
| 3. $7 \subseteq K$ | **F** | No tiene llaves; un elemento no puede ser subconjunto. |
| 4. $\{7\} \subseteq K$ | **V** | Quitamos llaves: queda $7$. Como $7 \in K$, la inclusión se cumple. |
| 5. $\{\{7\}\} \subseteq K$ | **V** | Quitamos llaves exteriores: queda $\{7\}$. Como $\{7\} \in K$, se cumple. |
| 6. $2 \in K$ | **F** | **¡Trampa!** En la caja existe $\{2\}$, pero el número $2$ suelto no está. |
| 7. $\{2\} \in K$ | **V** | El objeto $\{2\}$ figura idéntico como tercer elemento. |
| 8. $\{2\} \subseteq K$ | **F** | Quitamos llaves: queda $2$. Pero $2 \notin K$, por lo que no es subconjunto. |
| 9. $\{\{2\}\} \subseteq K$ | **V** | Quitamos llaves exteriores: queda $\{2\}$. Como $\{2\} \in K$, se cumple. |
| 10. $\emptyset \in K$ | **V** | El profesor escribió $\emptyset$ como cuarto elemento dentro de $K$. |
| 11. $\emptyset \subseteq K$ | **V** | Regla universal: $\emptyset$ siempre está incluido en todo conjunto. |
| 12. $\{\emptyset\} \subseteq K$ | **V** | Quitamos llaves: queda $\emptyset$. Como $\emptyset \in K$, la inclusión es válida. |

</details>

---

## Bloque 2: De Comprensión a Extensión (Restricciones de Universo $\mathbb{N}$ y $\mathbb{Z}$)

### 1. 🧠 Algoritmo Mental de 3 Fases

- **Fase 1 (Resolución Algebraica):** Resuelve la ecuación o desigualdad planteada en el predicado.
- **Fase 2 (Filtro de Universo - ¡Punto Crítico de Examen!):**
  - Si el universo es $\mathbb{N}$ (Naturales): Solo se admiten enteros positivos: $\{1, 2, 3, 4, \dots\}$. **Descarta negativos, cero y fracciones.**
  - Si el universo es $\mathbb{Z}$ (Enteros): Se admiten negativos, cero y positivos: $\{\dots, -2, -1, 0, 1, 2, \dots\}$. **Descarta fracciones y decimales.**
- **Fase 3 (Conectores Lógicos):**
  - Si dice "$\lor$" ($o$): Une las soluciones válidas de ambas condiciones.
  - Si dice "$\land$" ($y$): Solo toma soluciones que cumplan ambas simultáneamente.
- **Fase 4 (Escritura):** Lista los elementos entre llaves $\{ \}$, sin duplicar valores repetidos.

---

### 2. 👁️ Ejemplos Modelo Paso a Paso

#### Ejemplo A (Cuadrática con restricción natural):
$$A = \{ x \in \mathbb{N} \mid x^2 - 5x - 6 = 0 \}$$
- **Paso 1:** Factorizamos: $(x - 6)(x + 1) = 0 \rightarrow x_1 = 6, x_2 = -1$.
- **Paso 2:** Filtramos por $\mathbb{N}$: $6 \in \mathbb{N}$ (válido), $-1 \notin \mathbb{N}$ (se descarta por ser negativo).
- **Resultado:** $A = \{ 6 \}$

#### Ejemplo B (Letras con repetición):
$$B = \{ x \mid x \text{ es letra de "excusa"} \}$$
- **Paso 1:** Letras: $e, x, c, u, s, a$.
- **Paso 2:** No hay repeticiones redundantes; ordenamos: $B = \{a, c, e, s, u, x\}$.

#### Ejemplo C (Disyunción lógica $\lor$ en $\mathbb{Z}$):
$$C = \{ x \in \mathbb{Z} \mid x^2 - 9 = 0 \lor 2x - 1 = 9 \}$$
- **Paso 1:** Ecuación 1: $x^2 = 9 \rightarrow x = 3, x = -3$ (ambos pertenecen a $\mathbb{Z}$).
- **Paso 2:** Ecuación 2: $2x = 10 \rightarrow x = 5$ (pertenece a $\mathbb{Z}$).
- **Paso 3:** Conector $\lor$: Unimos todos los valores encontrados.
- **Resultado:** $C = \{ -3, 3, 5 \}$

#### Ejemplo D (Intervalo acotado en $\mathbb{N}$):
$$D = \{ x \in \mathbb{N} \mid 2 \le x < 7 \}$$
- **Paso 1:** $2 \le x$ incluye al $2$. $x < 7$ es estricto (no incluye al $7$).
- **Resultado:** $D = \{ 2, 3, 4, 5, 6 \}$

#### Ejemplo E (Valor absoluto en $\mathbb{Z}$):
$$E = \{ x \in \mathbb{Z} \mid |x| < 3 \}$$
- **Paso 1:** $|x| < 3 \iff -3 < x < 3$.
- **Paso 2:** Enteros estrictamente entre $-3$ y $3$.
- **Resultado:** $E = \{ -2, -1, 0, 1, 2 \}$

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 2
Determina por extensión los siguientes conjuntos aplicando el algoritmo:
1. $P = \{ x \in \mathbb{N} \mid x^2 - 7x - 8 = 0 \}$
2. $Q = \{ x \mid x \text{ es una letra de la palabra "reconocer"} \}$
3. $R = \{ x \in \mathbb{Z} \mid x^2 - 25 = 0 \lor 3x + 1 = 13 \}$
4. $S = \{ x \in \mathbb{N} \mid 3 < x \le 8 \}$
5. $T = \{ x \in \mathbb{Z} \mid |x - 2| \le 3 \}$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 2</b></summary>

1. **Conjunto $P$:**
   - Factorización: $(x - 8)(x + 1) = 0 \rightarrow x = 8, x = -1$.
   - Como $x \in \mathbb{N}$, descartamos $-1$.
   - **$P = \{ 8 \}$**

2. **Conjunto $Q$:**
   - Letras de "reconocer": $r, e, c, o, n, o, c, e, r$.
   - Eliminamos duplicados y dejamos una sola de cada una.
   - **$Q = \{ c, e, n, o, r \}$**

3. **Conjunto $R$:**
   - Ecuación 1: $x^2 = 25 \rightarrow x = 5, x = -5$ (ambos en $\mathbb{Z}$).
   - Ecuación 2: $3x = 12 \rightarrow x = 4$ (en $\mathbb{Z}$).
   - Unimos: **$R = \{ -5, 4, 5 \}$**

4. **Conjunto $S$:**
   - $3 < x$ no incluye al $3$. $x \le 8$ sí incluye al $8$.
   - Naturales: **$S = \{ 4, 5, 6, 7, 8 \}$**

5. **Conjunto $T$:**
   - Desigualdad: $-3 \le x - 2 \le 3 \rightarrow -1 \le x \le 5$.
   - Enteros en el rango: **$T = \{ -1, 0, 1, 2, 3, 4, 5 \}$**

</details>

---

## Bloque 3: De Extensión a Comprensión (Detección Rápida de Patrones)

### 1. 🧠 Algoritmo Mental de Identificación de Patrones

- **Test 1 (Resta / Progresión Aritmética):** Resta términos consecutivos ($a_2 - a_1, a_3 - a_2$).
  - Si la diferencia es constante $d$ $\rightarrow$ La base de la fórmula es $d \cdot k$. Ajusta el término inicial sumando o restando una constante: $d \cdot k + c$.
- **Test 2 (Potencias de Enteros):** Compara con las tablas de potencias conocidas:
  - $1, 4, 9, 16, 25 \dots \rightarrow k^2$ (cuadrados perfectos).
  - $1, 8, 27, 64, 125 \dots \rightarrow k^3$ (cubos perfectos).
  - $2, 4, 8, 16, 32 \dots \rightarrow 2^k$ (potencias de 2).
- **Test 3 (Infinitos en ambos lados):** Si tiene "$\dots$" a izquierda y derecha $\rightarrow$ Usa el universo $\mathbb{Z}$ (ejemplo: múltiplos de $m$: $\{ m \cdot k \mid k \in \mathbb{Z} \}$).
- **Fase Final:** Delimita el rango de la variable $k$ con precisión (ejemplo: $1 \le k \le 5$).

---

### 2. 👁️ Ejemplos Modelo Paso a Paso

- **Modelo 1:** $F = \{2, 4, 6, 8, 10\}$
  - Diferencia: $4 - 2 = 2, 6 - 4 = 2$. Múltiplos de 2 positivos del 1 al 5.
  - **Fórmula:** $F = \{ 2k \mid k \in \mathbb{N}, 1 \le k \le 5 \}$
- **Modelo 2:** $G = \{1, 4, 9, 16, 25\}$
  - Cuadrados: $1^2, 2^2, 3^2, 4^2, 5^2$.
  - **Fórmula:** $G = \{ k^2 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$
- **Modelo 3:** $H = \{ \dots, -6, -3, 0, 3, 6, \dots \}$
  - Múltiplos de 3 en ambas direcciones infinitas.
  - **Fórmula:** $H = \{ 3k \mid k \in \mathbb{Z} \}$
- **Modelo 4:** $I = \{1, 3, 5, 7, 9, 11\}$
  - Impares positivos: $2k - 1$ con $k = 1, \dots, 6$.
  - **Fórmula:** $I = \{ 2k - 1 \mid k \in \mathbb{N}, 1 \le k \le 6 \}$

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 3
Encuentra la fórmula por comprensión para:
1. $F_2 = \{ 5, 10, 15, 20, 25, 30 \}$
2. $G_2 = \{ 1, 8, 27, 64, 125 \}$
3. $H_2 = \{ \dots, -8, -4, 0, 4, 8, \dots \}$
4. $I_2 = \{ 2, 4, 8, 16, 32, 64 \}$
5. $J_2 = \{ 4, 7, 10, 13, 16 \}$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 3</b></summary>

1. **$F_2$:** Múltiplos de 5 del 1 al 6:
   $$\{ 5k \mid k \in \mathbb{N}, 1 \le k \le 6 \}$$
2. **$G_2$:** Cubos de los primeros 5 números naturales:
   $$\{ k^3 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$$
3. **$H_2$:** Múltiplos enteros de 4 en ambas direcciones:
   $$\{ 4k \mid k \in \mathbb{Z} \}$$
4. **$I_2$:** Potencias de base 2 desde el exponente 1 al 6:
   $$\{ 2^k \mid k \in \mathbb{N}, 1 \le k \le 6 \}$$
5. **$J_2$:** Sucesión que avanza de 3 en 3 con inicio en 4 ($3k + 1$ para $k = 1 \dots 5$):
   $$\{ 3k + 1 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$$

</details>

---

## Bloque 4: Operaciones entre Conjuntos

### 1. 🧠 Algoritmo Operacional

| Operación | Símbolo | Procedimiento Mental |
| :--- | :---: | :--- |
| **Unión** | $A \cup B$ | Junta todos los elementos de $A$ y de $B$, descartando duplicados. |
| **Intersección** | $A \cap B$ | Selecciona **únicamente** los elementos que estén al mismo tiempo en $A$ y en $B$. |
| **Diferencia** | $A - B$ | Toma el conjunto $A$ y tárrale todo elemento que figure en $B$. *(No es conmutativa: $A - B \ne B - A$)*. |
| **Complemento** | $A'$ o $A^c$ | Toma el Universal $U$ y elimina todos los que pertenezcan a $A$. |
| **Diferencia Simétrica** | $A \ \Delta \ B$ | Elementos que están en uno o en otro, pero no en ambos: $(A - B) \cup (B - A)$. |
| **Compuestas** | $(A \cup B) \cap C$ | **Resuelve siempre el paréntesis primero** y luego aplica la operación externa. |

---

### 2. 👁️ Ejemplo Modelo Paso a Paso
Sea $U = \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\}$, $A = \{1, 2, 3, 5, 7\}$, $B = \{2, 4, 6, 7, 8\}$, $C = \{3, 5, 7, 9, 10\}$.

1. **$A \cup B$:** $\{1, 2, 3, 5, 7\} \cup \{2, 4, 6, 7, 8\} = \{1, 2, 3, 4, 5, 6, 7, 8\}$
2. **$A \cap B$:** Elementos comunes $\{2, 7\}$
3. **$A - B$:** A los de $A$ les quitamos 2 y 7 $\rightarrow \{1, 3, 5\}$
4. **$B - A$:** A los de $B$ les quitamos 2 y 7 $\rightarrow \{4, 6, 8\}$
5. **$A'$:** Quitamos de $U$ los de $A \rightarrow \{4, 6, 8, 9, 10\}$
6. **$A \ \Delta \ B$:** $(A - B) \cup (B - A) = \{1, 3, 4, 5, 6, 8\}$
7. **$(A \cup B) \cap C$:** $\{1, 2, 3, 4, 5, 6, 7, 8\} \cap \{3, 5, 7, 9, 10\} = \{3, 5, 7\}$

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 4
Con el mismo universo $U = \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\}$ y los conjuntos:
$$X = \{ 1, 3, 5, 9 \}, \quad Y = \{ 2, 3, 5, 6, 8 \}, \quad Z = \{ 1, 2, 4, 8, 9 \}$$

Calcula:
1. $X \cup Y$
2. $X \cap Y$
3. $X - Y$
4. $Y - X$
5. $X'$
6. $X \ \Delta \ Y$
7. $(X \cup Y) \cap Z$
8. $X - (Y \cap Z)$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 4</b></summary>

1. **$X \cup Y = \{ 1, 2, 3, 5, 6, 8, 9 \}$**
2. **$X \cap Y = \{ 3, 5 \}$**
3. **$X - Y = \{ 1, 9 \}$**
4. **$Y - X = \{ 2, 6, 8 \}$**
5. **$X' = \{ 2, 4, 6, 7, 8, 10 \}$**
6. **$X \ \Delta \ Y = \{ 1, 2, 6, 8, 9 \}$**
7. **$(X \cup Y) \cap Z$:**
   - $X \cup Y = \{ 1, 2, 3, 5, 6, 8, 9 \}$
   - Cruzamos con $Z = \{ 1, 2, 4, 8, 9 \} \rightarrow \mathbf{\{ 1, 2, 8, 9 \}}$
8. **$X - (Y \cap Z)$:**
   - $Y \cap Z = \{ 2, 8 \}$
   - $X - \{ 2, 8 \} = \{ 1, 3, 5, 9 \} - \{ 2, 8 \} = \mathbf{\{ 1, 3, 5, 9 \}}$ (ninguno coincidía para restar).

</details>
