# 📓 Cálculo Infinitesimal — Notas de clase

## Primera revelación

La derivada y la integral no son magia.

La derivada es:

```text
¿qué tan rápido cambia?
```

La integral es:

```text
¿cuánta área llevo acumulada?
```

---

## Método del trapecio

La computadora integra así:

```text
trapecio
+
trapecio
+
trapecio
+
...
```

hasta aproximar la integral.

Momento importante:

> "Ah, por eso existe `np.cumsum()`"

---

## ¿Por qué restamos la mediana?

Confusión inicial:

```text
¿Qué demonios tiene que ver estadística con cálculo?
```

Descubrimiento:

```text
No corrige la integral.
Corrige la visualización.
```

Más precisamente:

```text
ajusta la constante de integración
```

para que la gráfica quede centrada.

Momento de iluminación:

> "¡¡¡Ya entendí por qué usan la mediana!!!"

---

## Frase del sensei

> "Tenemos que aprender a observar."

---

## Observación vs memorización

Antes:

```text
Quiero la fórmula.
```

Después:

```text
¿Qué estoy viendo?
```

---

## Regla de la cadena

La pregunta no es:

```text
¿Cómo derivo?
```

La pregunta es:

```text
¿Quién está afuera?
¿Quién está adentro?
```

---

### Caso 1

```text
sin²(x)
```

Observación:

```text
afuera = cuadrado
adentro = seno
```

---

### Caso 2

```text
sin(x²)
```

Observación:

```text
afuera = seno
adentro = cuadrado
```

---

## Momento "a la madre"

Descubrimiento:

```text
sin²(x)
```

y

```text
sin(x²)
```

NO son la misma función.

---

## Serie de Taylor

Reacción oficial:

> "¿Qué demonios acaba de pasar?"

Aprendizaje:

```text
Hay funciones cuya integral
no tiene una fórmula elemental simple.
```

Entonces aparecen:

```text
Series infinitas
Taylor
Fresnel
Brujería matemática
```

---

## Graficar por separado

Petición oficial del alumno:

> "Sensei, pase el código para verlas separadas."

Resultado:

### Función

Observación:

```text
La frecuencia aumenta.
```

---

### Derivada

Observación:

```text
Parece un embudo.
```

porque aparece:

```text
2x
```

---

### Antiderivada

Observación:

```text
Oscila y parece estabilizarse.
```

---

## Momento ingeniería

Pregunta espontánea:

> "¿Eso parece un filtro pasa banda?"

Respuesta:

```text
No exactamente.
```

Pero sí se parece a una señal tipo:

```text
chirp
```

donde la frecuencia aumenta con el tiempo.

---

## Descubrimiento inesperado

Separar las gráficas fue más útil que verlas juntas.

Regla para recordar:

```text
Si una gráfica es confusa,
haz varias gráficas simples.
```

---

## Nota personal

Soy daltónico.

Ver:

```text
función
+
derivada
+
antiderivada
```

en una sola gráfica es una experiencia religiosa no necesariamente agradable.

---

## Conclusión de la clase

La mejor frase no fue una fórmula.

Fue:

> "Aprender a observar."

Porque las respuestas empezaron a aparecer cuando dejamos de perseguir fórmulas y empezamos a mirar qué estaba haciendo cada curva. 🚀📈😄
