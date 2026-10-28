# Módulo 2: Regla de Cramer y Determinantes — Entrenamiento de Dominio Acelerado

> **Metodología de Aprendizaje Acelerado (4 Pasos):**
> 1. 🧠 **Algoritmo Mental:** El proceso de cálculo sistemático paso a paso.
> 2. 👁️ **Ejemplo Modelo:** Demostración con cada diagonal y signo explicitado.
> 3. ✍️ **Tu Turno (Ejercicio Espejo):** Sistema completo para resolver por tu cuenta con trampa de variable faltante.
> 4. 🔍 **Solución y Checkpoint:** Despliega la solución completa con comprobación en 30 segundos.

---

## Bloque 1: Cálculo de Determinantes $3 \times 3$ (Método de Sarrus)

### 1. 🧠 Algoritmo Mental de Sarrus en 4 Pasos

Sea el determinante:
$$\Delta = \begin{vmatrix} a & b & c \\ d & e & f \\ g & h & i \end{vmatrix}$$

- **Paso 1 (Duplicación):** Escribe las dos primeras filas exactamente iguales debajo de la tercera fila:
  $$\begin{matrix} a & b & c \\ d & e & f \\ g & h & i \\ \hline a & b & c \\ d & e & f \end{matrix}$$
- **Paso 2 (Diagonales Principales $\searrow$):** Calcula los 3 productos hacia abajo a la derecha y súmalos:
  $$P = (a \cdot e \cdot i) + (d \cdot h \cdot c) + (g \cdot b \cdot f)$$
- **Paso 3 (Diagonales Secundarias $\swarrow$):** Calcula los 3 productos hacia abajo a la izquierda y súmalos:
  $$S = (c \cdot e \cdot g) + (f \cdot h \cdot a) + (i \cdot b \cdot d)$$
- **Paso 4 (Resta y Regla de Signos):**
  $$\Delta = P - (S)$$
  > ⚠️ **ALERTA MÁXIMA:** El signo menos delante de $(S)$ le cambia el signo a toda la suma secundaria. Si $S = -6$, entonces $-(-6) = +6$.

---

### 2. 👁️ Ejemplo Modelo: Determinante con Signos Mixtos
Calcular:
$$\Delta = \begin{vmatrix} 1 & 2 & -2 \\ 4 & -1 & 1 \\ -2 & 1 & 1 \end{vmatrix}$$

- **Paso 1:** Duplicamos las filas 1 y 2:
  $$\begin{matrix} 1 & 2 & -2 \\ 4 & -1 & 1 \\ -2 & 1 & 1 \\ \hline 1 & 2 & -2 \\ 4 & -1 & 1 \end{matrix}$$
- **Paso 2 (Principales $\searrow$):**
  - $D_1 = 1 \cdot (-1) \cdot 1 = -1$
  - $D_2 = 4 \cdot 1 \cdot (-2) = -8$
  - $D_3 = (-2) \cdot 2 \cdot 1 = -4$
  - $P = (-1) + (-8) + (-4) = -13$
- **Paso 3 (Secundarias $\swarrow$):**
  - $D_4 = (-2) \cdot (-1) \cdot (-2) = -4$ *(tres negativos dan negativo)*
  - $D_5 = 1 \cdot 1 \cdot 1 = 1$
  - $D_6 = 1 \cdot 2 \cdot 4 = 8$
  - $S = (-4) + 1 + 8 = 5$
- **Paso 4:** $\Delta = P - (S) = -13 - (5) = \mathbf{-18}$

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 1
Calcula el siguiente determinante $3 \times 3$ aplicando Sarrus:
$$\Delta_M = \begin{vmatrix} 2 & -1 & 3 \\ 1 & 0 & 2 \\ -1 & 4 & 1 \end{vmatrix}$$

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 1</b></summary>

- **Duplicamos filas:**
  $$\begin{matrix} 2 & -1 & 3 \\ 1 & 0 & 2 \\ -1 & 4 & 1 \\ \hline 2 & -1 & 3 \\ 1 & 0 & 2 \end{matrix}$$
- **Principales ($\searrow$):**
  - $2 \cdot 0 \cdot 1 = 0$
  - $1 \cdot 4 \cdot 3 = 12$
  - $(-1) \cdot (-1) \cdot 2 = 2$
  - $P = 0 + 12 + 2 = 14$
- **Secundarias ($\swarrow$):**
  - $3 \cdot 0 \cdot (-1) = 0$
  - $2 \cdot 4 \cdot 2 = 16$
  - $1 \cdot (-1) \cdot 1 = -1$
  - $S = 0 + 16 - 1 = 15$
- **Resultado:**
  $$\Delta_M = P - S = 14 - (15) = \mathbf{-1}$$

</details>

---

## Bloque 2: Resolución Completa de Sistemas $3 \times 3$ por Cramer

### 1. 🧠 Algoritmo de Cramer en 5 Fases

Dado el sistema en forma canónica:
$$\begin{cases} a_1 x + b_1 y + c_1 z = d_1 \\ a_2 x + b_2 y + c_2 z = d_2 \\ a_3 x + b_3 y + c_3 z = d_3 \end{cases}$$

- **Fase 1 (Calcular $\Delta$):** Determinante con los coeficientes de $x, y, z$.
  - Si $\Delta = 0$ $\rightarrow$ **Detente:** El sistema no tiene solución única.
- **Fase 2 (Calcular $\Delta_x$):** Reemplaza la columna de las $x$ por los términos independientes $(d_1, d_2, d_3)$.
- **Fase 3 (Calcular $\Delta_y$):** Reemplaza la columna de las $y$ por los términos independientes $(d_1, d_2, d_3)$.
- **Fase 4 (Calcular $\Delta_z$):** Reemplaza la columna de las $z$ por los términos independientes $(d_1, d_2, d_3)$.
- **Fase 5 (Cocientes Finales):**
  $$x = \frac{\Delta_x}{\Delta}, \quad y = \frac{\Delta_y}{\Delta}, \quad z = \frac{\Delta_z}{\Delta}$$
- **Fase 6 (El Seguro de Vida - Comprobación en 30 s):** Reemplaza $(x, y, z)$ en la primera ecuación original. Si coincide con $d_1$, tienes el ejercicio 100% correcto.

---

### 2. 👁️ Ejemplo Modelo Completo Paso a Paso

Resolver el sistema:
$$\begin{cases} x + 2y - 2z = 10 \\ 4x - y + z = 4 \\ -2x + y + z = -2 \end{cases}$$
Términos independientes: $(10, 4, -2)$.

#### Paso 1: Determinante del Sistema ($\Delta$)
Calculado en el Bloque 1: $\mathbf{\Delta = -18} \ne 0$ (solución única garantizada).

#### Paso 2: Determinante $\Delta_x$
Columna $x$ reemplazada por $(10, 4, -2)$:
$$\Delta_x = \begin{vmatrix} 10 & 2 & -2 \\ 4 & -1 & 1 \\ -2 & 1 & 1 \end{vmatrix}$$
- Principales: $10(-1)(1) + 4(1)(-2) + (-2)(2)(1) = -10 - 8 - 4 = -22$
- Secundarias: $(-2)(-1)(-2) + 1(1)(10) + 1(2)(4) = -4 + 10 + 8 = 14$
- $\Delta_x = -22 - (14) = \mathbf{-36}$

#### Paso 3: Determinante $\Delta_y$
Columna $y$ reemplazada por $(10, 4, -2)$:
$$\Delta_y = \begin{vmatrix} 1 & 10 & -2 \\ 4 & 4 & 1 \\ -2 & -2 & 1 \end{vmatrix}$$
- Principales: $1(4)(1) + 4(-2)(-2) + (-2)(10)(1) = 4 + 16 - 20 = 0$
- Secundarias: $(-2)(4)(-2) + 1(-2)(1) + 1(10)(4) = 16 - 2 + 40 = 54$
- $\Delta_y = 0 - (54) = \mathbf{-54}$

#### Paso 4: Determinante $\Delta_z$
Columna $z$ reemplazada por $(10, 4, -2)$:
$$\Delta_z = \begin{vmatrix} 1 & 2 & 10 \\ 4 & -1 & 4 \\ -2 & 1 & -2 \end{vmatrix}$$
- Principales: $1(-1)(-2) + 4(1)(10) + (-2)(2)(4) = 2 + 40 - 16 = 26$
- Secundarias: $10(-1)(-2) + 4(1)(1) + (-2)(2)(4) = 20 + 4 - 16 = 8$
- $\Delta_z = 26 - (8) = \mathbf{18}$

#### Paso 5: Soluciones Finales
$$x = \frac{-36}{-18} = \mathbf{2}, \quad y = \frac{-54}{-18} = \mathbf{3}, \quad z = \frac{18}{-18} = \mathbf{-1}$$

#### Paso 6: Comprobación
Reemplazamos en Ecuación 1:
$$x + 2y - 2z = 2 + 2(3) - 2(-1) = 2 + 6 + 2 = \mathbf{10} \quad \checkmark$$

---

### 3. ✍️ Tu Turno: Ejercicio Espejo 2 (¡Alerta: Variable Faltante!)
Resuelve el siguiente sistema aplicando el algoritmo de 5 fases:
$$\begin{cases} x + y + z = 6 \\ 2y - z = 1 \\ 3x - y + z = 4 \end{cases}$$

> 💡 **Pista:** En la segunda ecuación no hay $x$. Su coeficiente es obligatoriamente **$0$** ($0x + 2y - z = 1$).

<details>
<summary>🔍 <b>Desplegar Solución y Checkpoint del Ejercicio Espejo 2</b></summary>

#### Matriz ordenada:
$$\begin{pmatrix} 1 & 1 & 1 & \mid & 6 \\ 0 & 2 & -1 & \mid & 1 \\ 3 & -1 & 1 & \mid & 4 \end{pmatrix}$$

#### 1. Cálculo de $\Delta$:
- Principales: $1(2)(1) + 0(-1)(1) + 3(1)(-1) = 2 + 0 - 3 = -1$
- Secundarias: $1(2)(3) + (-1)(-1)(1) + 1(1)(0) = 6 + 1 + 0 = 7$
- $\Delta = -1 - (7) = \mathbf{-8}$

#### 2. Cálculo de $\Delta_x$:
$$\begin{vmatrix} 6 & 1 & 1 \\ 1 & 2 & -1 \\ 4 & -1 & 1 \end{vmatrix}$$
- Principales: $6(2)(1) + 1(-1)(1) + 4(1)(-1) = 12 - 1 - 4 = 7$
- Secundarias: $1(2)(4) + (-1)(-1)(6) + 1(1)(1) = 8 + 6 + 1 = 15$
- $\Delta_x = 7 - (15) = \mathbf{-8}$

#### 3. Cálculo de $\Delta_y$:
$$\begin{vmatrix} 1 & 6 & 1 \\ 0 & 1 & -1 \\ 3 & 4 & 1 \end{vmatrix}$$
- Principales: $1(1)(1) + 0(4)(1) + 3(6)(-1) = 1 + 0 - 18 = -17$
- Secundarias: $1(1)(3) + (-1)(4)(1) + 1(6)(0) = 3 - 4 + 0 = -1$
- $\Delta_y = -17 - (-1) = \mathbf{-16}$

#### 4. Cálculo de $\Delta_z$:
$$\begin{vmatrix} 1 & 1 & 6 \\ 0 & 2 & 1 \\ 3 & -1 & 4 \end{vmatrix}$$
- Principales: $1(2)(4) + 0(-1)(6) + 3(1)(1) = 8 + 0 + 3 = 11$
- Secundarias: $6(2)(3) + 1(-1)(1) + 4(1)(0) = 36 - 1 + 0 = 35$
- $\Delta_z = 11 - (35) = \mathbf{-24}$

#### 5. Valores finales:
$$x = \frac{-8}{-8} = \mathbf{1}, \quad y = \frac{-16}{-8} = \mathbf{2}, \quad z = \frac{-24}{-8} = \mathbf{3}$$

#### 6. Comprobación rápida:
- Ec 1: $1 + 2 + 3 = 6 \quad \checkmark$
- Ec 2: $2(2) - 3 = 1 \quad \checkmark$
- Ec 3: $3(1) - 2 + 3 = 4 \quad \checkmark$

</details>

---

## Bloque 3: Protocolo ante las 3 Trampas Mortales de Parcial

1. **Trampa de Variable Faltante:** Si una ecuación tiene solo dos incógnitas (ej: $2y - z = 1$), la variable ausente lleva coeficiente **0**. Nunca omitas ni corras las columnas.
2. **Trampa de Ecuación Desordenada:** Si te entregan $3z - x + 2y = 5$, **reordena a orden alfabético antes de escribir la matriz**: $-x + 2y + 3z = 5$.
3. **Trampa de $\Delta = 0$:** Si el determinante principal da cero, **no dividas entre cero**. Escribe: *"El sistema no es compatible determinado; la Regla de Cramer no es aplicable para hallar solución única"*.
