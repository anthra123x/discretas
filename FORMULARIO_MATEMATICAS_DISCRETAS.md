# Formulario Oficial y Fichero de Reglas — Matemáticas Discretas

> Guía rápida de fórmulas y algoritmos de decisión para resolver todos los ejercicios del taller y preparar evaluaciones parciales.

---

## 1. Pertenencia ($\in$) vs. Inclusión ($\subseteq$)

### Reglas y Algoritmos de Decisión

| Operación / Símbolo | Condición / Fórmula | Regla Práctica de Cuaderno |
| :--- | :--- | :--- |
| **Pertenencia ($x \in A$)** | $x \text{ es elemento directo de } A$ | Abre la caja $A$: el objeto $x$ debe estar **idéntico tal cual** (con o sin llaves). |
| **No pertenencia ($x \notin A$)** | $x \text{ no está en la caja } A$ | Si le falta o sobra algo al objeto $\rightarrow$ Verdadero que no pertenece. |
| **Inclusión ($X \subseteq A$)** | $\forall y \ (y \in X \implies y \in A)$ | **Regla del destape:** Quita el par exterior de llaves de $X$. Cada elemento resultante debe pertenecer a $A$. |
| **Elemento sin llaves $\subseteq A$** | **SIEMPRE FALSO** | Ejemplo: $3 \subseteq A$ es FALSO de inmediato (un número suelto no tiene llaves). |
| **Vacío subconjunto ($\emptyset \subseteq A$)** | **SIEMPRE VERDADERO** | El conjunto vacío está incluido por definición en **cualquier** conjunto existente. |
| **Vacío elemento ($\emptyset \in A$)** | Depende de la caja | Solo es VERDADERO si el profesor escribió explícitamente el símbolo $\emptyset$ dentro de $A$. |
| **Conjunto del vacío ($\{\emptyset\} \subseteq A$)** | $\{\emptyset\} \subseteq A \iff \emptyset \in A$ | Al destapar queda $\emptyset$. Si $\emptyset$ figura dentro de $A$, entonces $\{\emptyset\} \subseteq A$ es VERDADERO. |

---

## 2. De Comprensión a Extensión (Resolución de Condiciones y Filtros)

### Fórmulas Algebraicas y Filtros de Universo

#### 1. Ecuación Cuadrática ($ax^2 + bx + c = 0$):
- **Fórmula General:**
  $$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$
- **Factorización directa ($x^2 + sx + p = 0$):**
  $$(x - r_1)(x - r_2) = 0 \implies x = r_1, \quad x = r_2$$
- **Filtro estricto por Universo:**
  - Si $x \in \mathbb{N}$ (Naturales) $\implies$ **Solo enteros estrictamente positivos:** $\{1, 2, 3, \dots\}$. *(Se descartan raíces negativas, el cero y fracciones)*.
  - Si $x \in \mathbb{Z}$ (Enteros) $\implies$ **Admite negativos, cero y positivos:** $\{\dots, -2, -1, 0, 1, 2, \dots\}$. *(Solo se descartan fracciones o decimales)*.

#### 2. Letras de una palabra:
- **Regla:** Se extrae cada letra individual, **eliminando cualquier repetición**.
  $$\text{"excusa"} \implies \{ a, c, e, s, u, x \}$$

#### 3. Conectores Lógicos:
- **Disyunción ("$\lor$" o "$o$"):** Se unen las soluciones de ambas partes.
  $$x \in (Condición_1 \lor Condición_2) \implies Sol_1 \cup Sol_2$$
- **Conjunción ("$\land$" o "$y$"):** Solo se toman las soluciones comunes (intersección).
  $$x \in (Condición_1 \land Condición_2) \implies Sol_1 \cap Sol_2$$

#### 4. Intervalos Numéricos:
- $a \le x < b \implies$ Incluye a $a$, **no** incluye a $b$.
- $a < x \le b \implies$ **No** incluye a $a$, incluye a $b$.
- $a \le x \le b \implies$ Incluye ambos extremos.

#### 5. Ecuaciones e Inecuaciones con Valor Absoluto:
- **Menor estricto:** $|u| < k \iff -k < u < k$
- **Menor o igual:** $|u| \le k \iff -k \le u \le k$
- **Mayor estricto:** $|u| > k \iff u < -k \quad \lor \quad u > k$
- **Mayor o igual:** $|u| \ge k \iff u \le -k \quad \lor \quad u \ge k$

---

## 3. De Extensión a Comprensión (Catálogo de Sucesiones y Fórmulas de Término General)

### Fórmulas Directas de Término General ($a_n$)

| Tipo de Sucesión | Secuencia de Ejemplo | Fórmula de Cuaderno ($a_n$) | En Comprensión de Conjunto |
| :--- | :--- | :--- | :--- |
| **Números Pares** | $2, 4, 6, 8, 10$ | $a_n = 2n$ | $\{ 2k \mid k \in \mathbb{N}, 1 \le k \le 5 \}$ |
| **Números Impares** | $1, 3, 5, 7, 9, 11$ | $a_n = 2n - 1$ | $\{ 2k - 1 \mid k \in \mathbb{N}, 1 \le k \le 6 \}$ |
| **Aritmética (diferencia constante $d$)** | $2, 5, 8, 11, 14 \quad (d = +3)$ | $a_n = a_1 + (n - 1)d$ <br> $\implies a_n = d \cdot n + (a_1 - d)$ | $\{ 3k - 1 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$ |
| **Cuadrados Perfectos** | $1, 4, 9, 16, 25$ | $a_n = n^2$ | $\{ k^2 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$ |
| **Cubos Perfectos** | $1, 8, 27, 64, 125$ | $a_n = n^3$ | $\{ k^3 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$ |
| **Potencias de 2 (Geométrica)** | $2, 4, 8, 16, 32, 64$ | $a_n = 2^n$ | $\{ 2^k \mid k \in \mathbb{N}, 1 \le k \le 6 \}$ |
| **Potencias Fraccionarias** | $1, \frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \dots$ | $a_n = \frac{1}{2^{n-1}}$ | $\left\{ \frac{1}{2^{k-1}} \;\middle|\; k \in \mathbb{N} \right\}$ |
| **Múltiplos Enteros Infinitos** | $\dots, -6, -3, 0, 3, 6, \dots$ | $a_n = 3k \quad (k \in \mathbb{Z})$ | $\{ 3k \mid k \in \mathbb{Z} \}$ |
| **Alternancia de Signos (Empieza $-$)** | $-3, +9, -27, +81, \dots$ | $a_n = (-1)^n \cdot 3^n$ | $\{ (-1)^k \cdot 3^k \mid k \in \mathbb{N} \}$ |
| **Alternancia de Signos (Empieza $+$)** | $+3, -9, +27, -81, \dots$ | $a_n = (-1)^{n+1} \cdot 3^n$ | $\{ (-1)^{k+1} \cdot 3^k \mid k \in \mathbb{N} \}$ |
| **Sucesión Recurrente** | $f_1 = -2, f_2 = 1$ | $f_k = 3f_{k-1} - f_{k-2}$ para $k \ge 3$ | Calculas hacia adelante término a término. |

---

## 4. Operaciones entre Conjuntos y Leyes de De Morgan

### Fórmulas Operacionales

| Operación | Definición Formal | Procedimiento de Cálculo |
| :--- | :--- | :--- |
| **Unión ($A \cup B$)** | $\{ x \mid x \in A \lor x \in B \}$ | Junta todos los elementos de $A$ y de $B$, sin duplicar. |
| **Intersección ($A \cap B$)** | $\{ x \mid x \in A \land x \in B \}$ | Solo los elementos presentes al mismo tiempo en $A$ y en $B$. |
| **Diferencia ($A - B$)** | $\{ x \mid x \in A \land x \notin B \}$ | Elementos de $A$ menos los que coincidan con $B$. *(Ojo: $A - B \ne B - A$)*. |
| **Complemento ($A'$ o $A^c$)** | $\{ x \in U \mid x \notin A \} = U - A$ | Quita del conjunto universal $U$ todos los elementos de $A$. |
| **Diferencia Simétrica ($A \ \Delta \ B$)** | $(A - B) \cup (B - A)$ | Elementos que están en uno o en el otro, pero no en ambos: <br> **Fórmula alternativa:** $A \ \Delta \ B = (A \cup B) - (A \cap B)$ |

### Leyes Fundamentales para Operaciones Combinadas

1. **Leyes de De Morgan (Cruciales en Parciales):**
   $$(A \cap B)' = A' \cup B'$$
   $$(A \cup B)' = A' \cap B'$$

2. **Diferencias con Intersecciones:**
   $$A - (B \cap C) = (A - B) \cup (A - C)$$
   $$A - (B \cup C) = (A - B) \cap (A - C)$$
   $$(A - C) \cup (B - C) = (A \cup B) - C$$

3. **Doble Complemento e Identidades:**
   $$(A')' = A, \quad U' = \emptyset, \quad \emptyset' = U$$
   $$A \cup A' = U, \quad A \cap A' = \emptyset$$

---

## 5. Regla de Cramer y Determinantes

### 1. Determinante $2 \times 2$:
$$\begin{vmatrix} a & b \\ c & d \end{vmatrix} = a d - b c$$

### 2. Determinante $3 \times 3$ (Regla de Sarrus):
$$\Delta = \begin{vmatrix} a & b & c \\ d & e & f \\ g & h & i \end{vmatrix}$$
Duplicando las dos primeras filas abajo:
$$\Delta = \underbrace{(a e i + d h c + g b f)}_{\text{Suma Diagonales Principales } (\searrow)} - \underbrace{(c e g + f h a + i b d)}_{\text{Suma Diagonales Secundarias } (\swarrow)}$$

### 3. Fórmulas de la Regla de Cramer para Sistemas $3 \times 3$:
$$x = \frac{\Delta_x}{\Delta}, \quad y = \frac{\Delta_y}{\Delta}, \quad z = \frac{\Delta_z}{\Delta} \quad (\text{Siempre que } \Delta \ne 0)$$

- $\Delta$: Matriz de coeficientes de $x, y, z$.
- $\Delta_x$: Sustituir columna de las $x$ por los términos independientes.
- $\Delta_y$: Sustituir columna de las $y$ por los términos independientes.
- $\Delta_z$: Sustituir columna de las $z$ por los términos independientes.

### 4. Regla de la Variable Ausente:
Si en una ecuación falta una variable (ej: $2y - z = 1$), su coeficiente es obligatoriamente **$0$** ($0x + 2y - 1z = 1$).

---

## 6. Operaciones con Matrices

### 1. Suma y Resta ($A \pm B$):
- **Condición:** Ambas matrices deben tener exactamente la misma dimensión ($m \times n$).
- **Fórmula:** $(A \pm B)_{ij} = A_{ij} \pm B_{ij}$ (se suma/resta posición a posición).

### 2. Multiplicación por Escalar ($k \cdot A$):
- **Fórmula:** Cada entrada de la matriz se multiplica por el número $k$:
  $$(k A)_{ij} = k \cdot A_{ij}$$

### 3. Multiplicación de Matrices ($A \cdot B$):
- **Condición de compatibilidad:** El número de **columnas de $A$** debe ser igual al número de **filas de $B$**:
  $$(m \times k) \cdot (k \times n) \implies \text{Matriz resultante de orden } (m \times n)$$
- **Fórmula (Fila $\times$ Columna):**
  $$(A \cdot B)_{ij} = \sum_{p=1}^k A_{ip} \cdot B_{pj} = A_{i1}B_{1j} + A_{i2}B_{2j} + \dots + A_{ik}B_{kj}$$
- **Propiedad crítica:** La multiplicación de matrices **NO es conmutativa** ($A \cdot B \ne B \cdot A$).

### 4. Matriz Transpuesta ($A^T$):
- Se intercambian filas por columnas: si $A$ es de orden $m \times n$, $A^T$ es de orden $n \times m$:
  $$(A^T)_{ij} = A_{ji}$$
- **Propiedades:**
  $$(A^T)^T = A, \quad (A + B)^T = A^T + B^T, \quad (A \cdot B)^T = B^T \cdot A^T$$
