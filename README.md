# Polinomios de Chebyshev e Interpolación Numérica
Práctica de la asignatura **Programación Científica y HPC** del Máster Universitario en Ingeniería Matemática y Computación (UNIR).

## Descripción
Este repositorio implementa y compara distintos métodos de interpolación numérica sobre tres funciones con comportamientos diferenciados:
- $f_1(x) = \sin(x)$ en $[-2\pi, 2\pi]$
- $f_2(x) = 1/(1+25x^2)$ en $[-1, 1]$ (función de Runge)
- $f_3(x) = e^{-20x^2}$ en $[-1, 1]$

Para cada función se construyen nodos equiespaciados y nodos de Chebyshev con $n \in \{11, 21\}$, y se aplican cuatro métodos de interpolación. Se analiza el error absoluto máximo, la norma $L_2$ y los tiempos de construcción. Como extensión, se implementa cuadratura de Clenshaw-Curtis y se compara con el trapecio compuesto.

## Métodos implementados
- **Interpolación baricéntrica** — via `scipy.interpolate.BarycentricInterpolator`
- **Interpolación de Lagrange** — via `scipy.interpolate.lagrange`
- **Diferencias divididas de Newton** — implementación propia con esquema de Horner; se muestran los polinomios resultantes en forma estándar para cada función, tipo y número de nodos
- **Splines cúbicos** — via `scipy.interpolate.InterpolatedUnivariateSpline`
- **Cuadratura de Clenshaw-Curtis** — implementación propia

## Resultados principales
- Los nodos de Chebyshev reducen el error de los métodos polinómicos globales en factores superiores a 3000 en los casos más extremos (función de Runge con $n=21$).
- El spline cúbico es el método más robusto con nodos equiespaciados, evitando las oscilaciones del fenómeno de Runge.
- La cuadratura de Clenshaw-Curtis supera al trapecio compuesto en funciones suaves, pero el trapecio resulta más preciso para funciones muy concentradas en una región pequeña del intervalo.

## Autores
Grupo 9 — Máster Universitario en Ingeniería Matemática y Computación, UNIR.

- Saúl González Bermejo
- Joe Xavier Herrera Vallejo
- Juan Castañón Pérez
- Gonzalo Ariel Duarte

