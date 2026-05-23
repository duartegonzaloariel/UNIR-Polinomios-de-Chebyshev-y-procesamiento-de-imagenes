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
- **Diferencias divididas de Newton** — implementación propia con esquema de Horner
- **Splines cúbicos** — via `scipy.interpolate.InterpolatedUnivariateSpline`
- **Cuadratura de Clenshaw-Curtis** — implementación propia

## Estructura
