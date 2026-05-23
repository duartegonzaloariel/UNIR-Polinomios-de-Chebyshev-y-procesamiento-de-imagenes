## Requisitos

```bash
pip install numpy scipy pandas matplotlib seaborn
```

## Uso

Abrir y ejecutar el notebook `practica_2_grupo_9_v2.ipynb` en orden. Todas las celdas son autocontenidas y no requieren datos externos.

## Resultados principales

- Los nodos de Chebyshev reducen el error de los métodos polinómicos globales en factores superiores a 3000 en los casos más extremos (función de Runge con $n=21$).
- El spline cúbico es el método más robusto con nodos equiespaciados, evitando las oscilaciones del fenómeno de Runge.
- La cuadratura de Clenshaw-Curtis supera al trapecio compuesto en funciones suaves, pero el trapecio resulta más preciso para funciones muy concentradas en una región pequeña del intervalo.

## Autores

Grupo 9 — Máster Universitario en Ingeniería Matemática y Computación, UNIR.
Saúl González Bermejo
Joe Xavier Herrera Vallejo
Juan Castañón Pérez
Gonzalo Ariel Duarte
