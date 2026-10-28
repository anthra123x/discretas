# Módulo 3: Práctica Explicada de Conjuntos — Banco Intensivo Paso a Paso

> **Metodología de Aprendizaje Acelerado (4 Pasos):**
> 1. 🧠 **Algoritmo Mental:** Criterios exactos de evaluación y resolución.
> 2. 👁️ **Ejemplo Modelo:** Demostración con justificación formal paso a paso.
> 3. ✍️ **Tu Turno (Ejercicio Espejo):** Reactivos tipo parcial para resolver por tu cuenta.
> 4. 🔍 **Solución y Checkpoint:** Despliega para validar tus respuestas y comprobar tu dominio.

---

## Bloque 1: Los 12 Reactivos Críticos de Pertenencia ($\in$) e Inclusión ($\subseteq$)

### 1. 🧠 Algoritmo de Evaluación Rápida

- **Pertenencia ($x \in M$):** Abre $M$. ¿Está el elemento $x$ exactamente igual a como está escrito (con o sin llaves)? Si sí $\rightarrow$ **V**. Si no $\rightarrow$ **F**.
- **Inclusión ($X \subseteq M$):**
  - ¿Es $\emptyset \subseteq M$? $\rightarrow$ **V SIEMPRE** (por axioma universal).
  - ¿Tiene llaves exteriores? Si no tiene llaves $\rightarrow$ **F INMEDIATO**.
  - Destapa las llaves exteriores: Comprueba si cada elemento interno pertenece a $M$. Si todos están $\rightarrow$ **V**. Si falta uno $\rightarrow$ **F**.

---

### 2. 👁️ Ejemplo Modelo: Análisis Exhaustivo sobre $M = \{ 3, \{3\}, \{4\}, \emptyset \}$

Elementos de $M$:
1. $3$ (número suelto)
2. $\{3\}$ (paquete con llaves)
3. $\{4\}$ (paquete con llaves; el $4$ suelto no existe)
4. $\emptyset$ (símbolo de vacío)

| # | Proposición | Algoritmo Aplicado | Dictamen |
| :-: | :--- | :--- | :---: |
| 1 | **$3 \in M$** | Vemos el $3$ suelto en la lista. | **V** |
| 2 | **$\{3\} \in M$** | Vemos el objeto $\{3\}$ como 2.° elemento. | **V** |
| 3 | **$3 \subseteq M$** | No tiene llaves; un elemento no incluye. | **F** |
| 4 | **$\{3\} \subseteq M$** | Destapamos $\{3\} \rightarrow 3$. Como $3 \in M$ (1.° elem). | **V** |
| 5 | **$\{\{3\}\} \subseteq M$** | Destapamos $\{\{3\}\} \rightarrow \{3\}$. Como $\{3\} \in M$ (2.° elem). | **V** |
| 6 | **$4 \in M$** | **¡Trampa!** En $M$ está $\{4\}$, pero el 4 suelto no. | **F** |
| 7 | **$\{4\} \in M$** | Vemos el objeto $\{4\}$ como 3.° elemento. | **V** |
| 8 | **$\{4\} \subseteq M$** | Destapamos $\{4\} \rightarrow 4$. Pero $4 \notin M$. | **F** |
| 9 | **$\{\{4\}\} \subseteq M$** | Destapamos $\{\{4\}\} \rightarrow \{4\}$. Como $\{4\} \in M$. | **V** |
| 10 | **$\emptyset \in M$** | Está escrito explícitamente en la lista. | **V** |
| 11 | **$\emptyset \subseteq M$** | Regla universal del conjunto vacío. | **V** |
| 12 | **$\{\emptyset\} \subseteq M$** | Destapamos $\{\emptyset\} \rightarrow \emptyset$. Como $\emptyset \in M$. | **V** |

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 1
Dado el conjunto de examen:
$$W = \{ 5, \{5\}, \{1, 2\}, \emptyset \}$$

Determina si cada una de las 12 afirmaciones es **V** o **F**:
1. $5 \in W$
2. $\{5\} \in W$
3. $5 \subseteq W$
4. $\{5\} \subseteq W$
5. $\{\{5\}\} \subseteq W$
6. $1 \in W$
7. $\{1, 2\} \in W$
8. $\{1, 2\} \subseteq W$
9. $\{\{1, 2\}\} \subseteq W$
10. $\emptyset \in W$
11. $\emptyset \subseteq W$
12. $\{\emptyset\} \subseteq W$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 1</b></summary>

| # | Reactivo | V/F | Justificación con el Algoritmo |
| :-: | :--- | :---: | :--- |
| 1 | $5 \in W$ | **V** | El número $5$ suelto es el 1.° elemento. |
| 2 | $\{5\} \in W$ | **V** | El objeto $\{5\}$ figura como 2.° elemento. |
| 3 | $5 \subseteq W$ | **F** | No tiene llaves exteriores. |
| 4 | $\{5\} \subseteq W$ | **V** | Al destapar queda $5$, que pertenece a $W$. |
| 5 | $\{\{5\}\} \subseteq W$ | **V** | Al destapar queda $\{5\}$, que pertenece a $W$. |
| 6 | $1 \in W$ | **F** | **¡Trampa!** En $W$ está el paquete $\{1, 2\}$, no el $1$ suelto. |
| 7 | $\{1, 2\} \in W$ | **V** | El paquete $\{1, 2\}$ es el 3.° elemento. |
| 8 | $\{1, 2\} \subseteq W$ | **F** | Al destapar quedan $1$ y $2$, pero ninguno está suelto en $W$. |
| 9 | $\{\{1, 2\}\} \subseteq W$ | **V** | Al destapar queda $\{1, 2\}$, que sí pertenece a $W$. |
| 10 | $\emptyset \in W$ | **V** | El símbolo $\emptyset$ está explícito en la lista de $W$. |
| 11 | $\emptyset \subseteq W$ | **V** | Regla universal: el vacío siempre es subconjunto. |
| 12 | $\{\emptyset\} \subseteq W$ | **V** | Al destapar queda $\emptyset$, que pertenece a $W$. |

</details>

---

## Bloque 2: Comprensión a Extensión con Restricciones Críticas

### 1. 🧠 Algoritmo de 3 Pasos
1. **Resolver:** Despejar la variable o resolver la ecuación.
2. **Filtrar:**
   - En $\mathbb{N}$: descarta soluciones $\le 0$ o no enteras.
   - En $\mathbb{Z}$: conserva positivos, negativos y cero. Descarta fracciones.
3. **Combinar:** Unir si hay disyunción ($\lor$), o intersectar si hay conjunción ($\land$).

---

### 2. 👁️ Ejemplos Modelo

- **Modelo 1:** $A = \{ x \in \mathbb{N} \mid x^2 - 2x - 8 = 0 \}$
  - $(x - 4)(x + 2) = 0 \rightarrow x = 4, x = -2$.
  - En $\mathbb{N}$: solo $4 \in \mathbb{N}$. **$A = \{ 4 \}$**
- **Modelo 2:** $B = \{ x \mid x \text{ es letra de "universidad"} \}$
  - Letras: $u, n, i, v, e, r, s, i, d, a, d$.
  - Descartamos repeticiones de 'i' y 'd'. **$B = \{ a, d, e, i, n, r, s, u, v \}$**
- **Modelo 3:** $C = \{ x \in \mathbb{Z} \mid x^2 - 16 = 0 \lor 3x + 2 = -7 \}$
  - $x^2 = 16 \rightarrow x = 4, x = -4$.
  - $3x = -9 \rightarrow x = -3$.
  - Unimos: **$C = \{ -4, -3, 4 \}$**
- **Modelo 4:** $D = \{ x \in \mathbb{Z} \mid -3 \le x < 3 \}$
  - **$D = \{ -3, -2, -1, 0, 1, 2 \}$**
- **Modelo 5:** $E = \{ x \in \mathbb{Z} \mid |x - 1| \le 2 \}$
  - $-2 \le x - 1 \le 2 \rightarrow -1 \le x \le 3$.
  - **$E = \{ -1, 0, 1, 2, 3 \}$**

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 2
Expresa por extensión:
1. $A_2 = \{ x \in \mathbb{N} \mid x^2 - 3x - 10 = 0 \}$
2. $B_2 = \{ x \mid x \text{ es letra de "probabilidad"} \}$
3. $C_2 = \{ x \in \mathbb{Z} \mid x^2 - 36 = 0 \lor 2x + 5 = -1 \}$
4. $D_2 = \{ x \in \mathbb{Z} \mid -4 < x \le 2 \}$
5. $E_2 = \{ x \in \mathbb{Z} \mid |x + 1| \le 3 \}$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 2</b></summary>

1. **$A_2 = \{ 5 \}$** (Factoriza $(x - 5)(x + 2) = 0$, se descarta $-2 \notin \mathbb{N}$).
2. **$B_2 = \{ a, b, d, i, l, o, p, r \}$** (Eliminadas repeticiones de 'b', 'a', 'i').
3. **$C_2 = \{ -6, -3, 6 \}$** ($x = \pm 6$ y $2x = -6 \rightarrow x = -3$).
4. **$D_2 = \{ -3, -2, -1, 0, 1, 2 \}$** (No incluye $-4$, sí incluye $2$).
5. **$E_2 = \{ -4, -3, -2, -1, 0, 1, 2 \}$** ($-3 \le x + 1 \le 3 \rightarrow -4 \le x \le 2$).

</details>

---

## Bloque 3: Extensión a Comprensión (Fórmulas y Sucesiones)

### 1. 🧠 Algoritmo de Detección
- Diferencia constante $d$: Progresión $d \cdot k + c$.
- Múltiplos infinitos en ambos sentidos: $m \cdot k$ con $k \in \mathbb{Z}$.
- Crecimiento acelerado: Comparar con $k^2, k^3, 2^k$.

---

### 2. 👁️ Ejemplos Modelo
- $F = \{ 5, 10, 15, 20, 25, 30 \} \rightarrow \{ 5k \mid k \in \mathbb{N}, 1 \le k \le 6 \}$
- $G = \{ 1, 8, 27, 64, 125 \} \rightarrow \{ k^3 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$
- $H = \{ \dots, -8, -4, 0, 4, 8, \dots \} \rightarrow \{ 4k \mid k \in \mathbb{Z} \}$
- $I = \{ 2, 4, 8, 16, 32, 64 \} \rightarrow \{ 2^k \mid k \in \mathbb{N}, 1 \le k \le 6 \}$
- $J = \{ 4, 7, 10, 13, 16 \} \rightarrow \{ 3k + 1 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 3
Escribe la fórmula por comprensión:
1. $F_3 = \{ 6, 12, 18, 24, 30, 36 \}$
2. $G_3 = \{ 1, 16, 81, 256 \}$
3. $H_3 = \{ \dots, -15, -10, -5, 0, 5, 10, 15, \dots \}$
4. $I_3 = \{ 3, 9, 27, 81, 243 \}$
5. $J_3 = \{ 5, 9, 13, 17, 21 \}$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 3</b></summary>

1. **$F_3 = \{ 6k \mid k \in \mathbb{N}, 1 \le k \le 6 \}$**
2. **$G_3 = \{ k^4 \mid k \in \mathbb{N}, 1 \le k \le 4 \}$** (Potencias cuartas).
3. **$H_3 = \{ 5k \mid k \in \mathbb{Z} \}$**
4. **$I_3 = \{ 3^k \mid k \in \mathbb{N}, 1 \le k \le 5 \}$**
5. **$J_3 = \{ 4k + 1 \mid k \in \mathbb{N}, 1 \le k \le 5 \}$** (Razón 4, inicio en 5).

</details>

---

## Bloque 4: Las 10 Operaciones Fundamentales con Universales

### 1. 👁️ Ejemplo Modelo: $U = \{1 \dots 10\}$, $A=\{1,2,3,5,7\}$, $B=\{2,4,6,7,8\}$, $C=\{3,5,7,9,10\}$

1. **Unión:** $A \cup B = \{1, 2, 3, 4, 5, 6, 7, 8\}$
2. **Intersección:** $A \cap B = \{2, 7\}$
3. **Diferencia:** $A - B = \{1, 3, 5\}$
4. **Diferencia inversa:** $B - A = \{4, 6, 8\}$
5. **Complemento:** $A' = \{4, 6, 8, 9, 10\}$
6. **Diferencia simétrica:** $A \ \Delta \ B = \{1, 3, 4, 5, 6, 8\}$
7. **Compuesta:** $(A \cup B) \cap C = \{3, 5, 7\}$
8. **Compuesta:** $A - (B \cap C) = A - \{7\} = \{1, 2, 3, 5\}$
9. **De Morgan:** $(A \cap B)' = \{2, 7\}' = \{1, 3, 4, 5, 6, 8, 9, 10\}$
10. **Compuesta:** $(A - C) \cup (B - C) = \{1, 2\} \cup \{2, 4, 6, 8\} = \{1, 2, 4, 6, 8\}$

---

### 2. ✍️ Tu Turno: Ejercicio Espejo 4
Dado:
$$U = \{ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 \}$$
$$P = \{ 2, 3, 5, 7 \}, \quad Q = \{ 1, 3, 5, 7, 9 \}, \quad R = \{ 4, 5, 6, 7, 8 \}$$

Calcula las 10 operaciones:
1. $P \cup Q$
2. $P \cap Q$
3. $P - Q$
4. $Q - P$
5. $P'$
6. $P \ \Delta \ Q$
7. $(P \cup Q) \cap R$
8. $P - (Q \cap R)$
9. $(P \cap Q)'$
10. $(P - R) \cup (Q - R)$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 4</b></summary>

1. **$P \cup Q = \{ 1, 2, 3, 5, 7, 9 \}$**
2. **$P \cap Q = \{ 3, 5, 7 \}$**
3. **$P - Q = \{ 2 \}$**
4. **$Q - P = \{ 1, 9 \}$**
5. **$P' = \{ 1, 4, 6, 8, 9, 10 \}$**
6. **$P \ \Delta \ Q = \{ 1, 2, 9 \}$**
7. **$(P \cup Q) \cap R = \{ 5, 7 \}$** (Cruzamos $\{1, 2, 3, 5, 7, 9\}$ con $\{4, 5, 6, 7, 8\}$).
8. **$P - (Q \cap R) = \{ 2, 3 \}$** ($Q \cap R = \{5, 7\}$, los restamos de $P$).
9. **$(P \cap Q)' = \{ 1, 2, 4, 6, 8, 9, 10 \}$** (Todos menos $\{3, 5, 7\}$).
10. **$(P - R) \cup (Q - R) = \{ 2, 3 \} \cup \{ 1, 3, 9 \} = \{ 1, 2, 3, 9 \}$**

</details>
