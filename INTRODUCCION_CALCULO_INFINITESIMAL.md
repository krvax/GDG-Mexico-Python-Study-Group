# 📘 Hands-On: Introducción al Cálculo Infinitesimal con Python

## Objetivo

Aprender los conceptos fundamentales del cálculo diferencial e integral utilizando Python, NumPy y Matplotlib.

---

# ¿Qué es el cálculo infinitesimal?

El cálculo infinitesimal es una rama de las matemáticas que estudia el cambio continuo.

Se divide en dos áreas principales:

## Cálculo Diferencial

Estudia:

* Tasas de cambio
* Pendientes
* Velocidades
* Crecimiento y decrecimiento de funciones

Pregunta principal:

> ¿Qué tan rápido cambia una variable respecto a otra?

---

## Cálculo Integral

Estudia:

* Acumulación de cantidades
* Áreas bajo curvas
* Volúmenes
* Cantidades acumuladas

Pregunta principal:

> ¿Cuánto se ha acumulado a lo largo de un intervalo?

---

# Configuración Inicial

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(-10, 10, 1000)
```

Generamos:

* Rango de -10 a 10
* 1000 muestras
* Resolución suficiente para aproximaciones numéricas

---

# Derivación Numérica

```python
derivada = lambda y: np.diff(y) / np.diff(x)
```

La derivada se aproxima mediante:

Δy / Δx

donde:

```text
pendiente = cambio vertical / cambio horizontal
```

---

## Ejemplo

Para:

f(x) = x²

La derivada teórica es:

f'(x) = 2x

Cuando ejecutamos:

```python
derivada(x**2)
```

obtenemos una aproximación numérica muy cercana a:

```python
2*x
```

---

# Integración Numérica

```python
antiderivada = lambda y: np.cumsum(
    (y[1:] + y[:-1]) * np.diff(x) / 2
)
```

Esta implementación utiliza la Regla del Trapecio.

Cada par de puntos forma un trapecio cuya área se acumula progresivamente.

Visualmente:

```text
 ███
█████
███████
█████████
```

La integral representa el área acumulada bajo la curva.

---

# Función de Visualización

```python
def visualizacion(y, dy, sy):
    plt.plot(x, y, color='blue', label='Función')
    plt.plot(x[1:], dy, color='green', label='Derivada')
    plt.plot(x[1:], sy, color='purple', label='Antiderivada')

    plt.axhline(y=0, color='red')
    plt.axvline(x=0, color='red')

    plt.legend(loc='upper left')
    plt.grid()
    plt.show()
```

---

# Función Cuadrática

## Función

```python
def funcion_cuadrada(x):
    return x**2
```

## Cálculo

```python
f_cuadrada = funcion_cuadrada(x)
df_cuadrada = derivada(f_cuadrada)
sf_cuadrada = antiderivada(f_cuadrada)

plt.ylim(-100, 100)
visualizacion(
    f_cuadrada,
    df_cuadrada,
    sf_cuadrada
)
```

## Teoría

Función:

f(x) = x²

Derivada:

f'(x) = 2x

Integral:

∫x²dx = x³/3 + C

---

# Función Seno

## Función

```python
def funcion_seno(x):
    return np.sin(x)
```

## Cálculo

```python
f_seno = funcion_seno(x)
df_seno = derivada(f_seno)
sf_seno = antiderivada(f_seno)

visualizacion(
    f_seno,
    df_seno,
    sf_seno
)
```

## Teoría

Función:

sin(x)

Derivada:

cos(x)

Integral:

-cos(x) + C

---

# Función Lineal

## Función

```python
def funcion_lineal(x):
    return x
```

## Cálculo

```python
f_lineal = funcion_lineal(x)
df_lineal = derivada(f_lineal)
sf_lineal = antiderivada(f_lineal)

visualizacion(
    f_lineal,
    df_lineal,
    sf_lineal
)
```

## Teoría

Función:

f(x) = x

Derivada:

f'(x) = 1

Integral:

x²/2 + C

---

# Función Cúbica

## Función

```python
def funcion_cubica(x):
    return x**3
```

## Cálculo

```python
f_cubica = funcion_cubica(x)
df_cubica = derivada(f_cubica)
sf_cubica = antiderivada(f_cubica)

plt.ylim(-100, 100)

visualizacion(
    f_cubica,
    df_cubica,
    sf_cubica
)
```

## Teoría

Función:

f(x) = x³

Derivada:

f'(x) = 3x²

Integral:

x⁴/4 + C

---

# Función Coseno

## Función

```python
def funcion_coseno(x):
    return np.cos(x)
```

## Cálculo

```python
f_coseno = funcion_coseno(x)
df_coseno = derivada(f_coseno)
sf_coseno = antiderivada(f_coseno)

visualizacion(
    f_coseno,
    df_coseno,
    sf_coseno
)
```

## Teoría

Función:

cos(x)

Derivada:

-sin(x)

Integral:

sin(x) + C

---

# Función Tangente

## Función

```python
def funcion_tangente(x):
    return np.tan(x)
```

## Cálculo

```python
f_tangente = funcion_tangente(x)
df_tangente = derivada(f_tangente)
sf_tangente = antiderivada(f_tangente)

plt.ylim(-5, 5)

visualizacion(
    f_tangente,
    df_tangente,
    sf_tangente
)
```

## Teoría

Función:

tan(x)

Derivada:

sec²(x)

Observación:

La tangente tiende a infinito cerca de:

```text
π/2
3π/2
5π/2
...
```

Por eso es necesario limitar el eje Y.

---

# Composición de Funciones (Regla de la Cadena)

La regla de la cadena se utiliza cuando una función contiene otra función.

Ejemplo:

```python
np.sin(x**2)
```

Flujo:

```text
x
↓
x²
↓
sin()
```

---

## Ejemplo

```python
def funcion_compuesta(x):
    return np.sin(x**2)
```

```python
f_compuesta = funcion_compuesta(x)
df_compuesta = derivada(f_compuesta)
sf_compuesta = antiderivada(f_compuesta)

plt.ylim(-5, 5)

visualizacion(
    f_compuesta,
    df_compuesta,
    sf_compuesta
)
```

---

## Derivada Teórica

Si:

```text
f(x) = sin(x²)
```

Entonces:

```text
f'(x) = cos(x²) · 2x
```

La derivada de la función externa se multiplica por la derivada de la función interna.

---

# Conceptos Clave para Recordar

## Derivar

Significa medir qué tan rápido cambia algo.

Ejemplos:

* Velocidad
* Aceleración
* Crecimiento poblacional
* Temperatura

---

## Integrar

Significa acumular cantidades.

Ejemplos:

* Área bajo una curva
* Distancia recorrida
* Energía acumulada
* Volumen

---

## Regla de la Cadena

Se utiliza cuando existe una función dentro de otra función.

Ejemplo:

```python
sin(x²)
cos(3x)
exp(x²)
```

---

# Resumen Ejecutivo

Derivar:

```text
Cambio
Pendiente
Velocidad
```

Integrar:

```text
Acumulación
Área
Cantidad total
```

Regla de la cadena:

```text
Función dentro de función
```

Python nos permite aproximar estos conceptos usando:

```python
np.diff()
np.cumsum()
numpy
matplotlib
```

y visualizar gráficamente cómo se comportan las funciones, sus derivadas y sus integrales.
