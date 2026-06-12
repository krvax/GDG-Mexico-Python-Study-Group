# 📓 Clase: Cálculo Infinitesimal con Python

## Objetivo

Visualizar funciones, derivadas y antiderivadas mediante aproximaciones numéricas usando NumPy y Matplotlib.

---

# Derivación numérica

La derivada se aproximó usando diferencias finitas entre muestras consecutivas.

Idea:

```text
pendiente ≈ cambio en y / cambio en x
```

Observación:

* La derivada tiene una muestra menos que la función original.
* `np.diff()` reduce la longitud del arreglo.

---

# Integración numérica

La antiderivada se aproximó usando el método del trapecio.

Idea:

```text
área total
=
suma de áreas de trapecios
```

Implementación conceptual:

```text
trapecio + trapecio + trapecio + ...
```

mediante:

```python
np.cumsum(...)
```

---

# Mediana y constante de integración

Descubrimiento importante de la clase.

La antiderivada calculada numéricamente puede quedar desplazada verticalmente.

Se utilizó:

```python
np.median(...)
```

para recentrar la gráfica.

Observación:

```text
Restar la mediana NO cambia la forma.
Solo cambia la posición vertical.
```

Conexión matemática:

```text
∫f(x)dx = F(x) + C
```

La mediana actúa como una forma práctica de ajustar la constante de integración para visualizar mejor la curva.

---

# Aprender a observar

Idea repetida por el profesor.

Antes de aplicar fórmulas:

```text
Observar comportamiento.
Observar patrones.
Observar composición.
```

La gráfica puede revelar información antes que el álgebra.

---

# Regla de la cadena

Idea central:

```text
Derivar la función exterior.
Multiplicar por la derivada de la función interior.
```

Pregunta clave:

```text
¿Qué está afuera?
¿Qué está adentro?
```

---

# Composición de funciones

Ejemplo conceptual:

```text
entrada
↓
g(x)
↓
resultado
↓
f(...)
↓
resultado final
```

La notación:

```text
f(g(x))
```

puede implementarse directamente en código:

```python
f(g(x))
```

---

# Observaciones de funciones estudiadas

## x²

```text
Función      -> parábola
Derivada     -> recta
Antiderivada -> cúbica
```

Permite visualizar claramente el Teorema Fundamental del Cálculo.

---

## sin(x)

```text
Derivada     -> cos(x)
Antiderivada -> -cos(x) + C
```

La gráfica confirma visualmente ambas relaciones.

---

## sin²(x)

Observación:

```text
afuera = cuadrado
adentro = seno
```

Primer ejemplo claro de composición.

---

## sin(x²)

Observación:

```text
afuera = seno
adentro = cuadrado
```

No es la misma función que:

```text
sin²(x)
```

aunque visualmente se parezcan en la escritura.

---

# Serie de Taylor

Aparece porque algunas integrales no tienen una antiderivada elemental simple.

Observación importante:

```text
La computadora puede integrar numéricamente
aunque no exista una fórmula elemental sencilla.
```

---

# Visualización

Descubrimiento práctico de la sesión:

Graficar función, derivada y antiderivada juntas puede ocultar patrones.

Mejor estrategia:

```text
1 gráfica por comportamiento
```

Beneficios:

* Más claridad.
* Más observación.
* Menos dependencia del color.
* Más accesible (especialmente útil siendo daltónico).

---

# Frase de la clase

> "Tenemos que aprender a observar."

Y la evidencia fue clara:

```text
Cuando se separaron las gráficas,
los patrones aparecieron inmediatamente.
```

Ese último punto vale oro porque no es solamente cálculo; también es análisis de datos, ingeniería y observabilidad. 🚀
