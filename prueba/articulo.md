---
title: Análisis de Estructuras Complejas en Arch Linux
author: Tu Nombre
abstract: Este documento es una prueba de fuego. Se diseñó para forzar a la máquina a renderizar dos columnas, ecuaciones de alto nivel y tablas que normalmente romperían el sistema. Al superar estos errores de compilación, validamos que el flujo de trabajo es apto para entregas universitarias finales.
format:
  pdf:
    documentclass: article
    classoption:
      - twocolumn
    geometry: margin=1.5cm
    pdf-engine: xelatex
    include-in-header:
      - text: |
          \usepackage{booktabs}
          % EL PARCHE DEFINITIVO
          \makeatletter
          \AtBeginDocument{
            \let\longtable\tabular
            \let\endlongtable\endtabular
            \def\endhead{}
            \def\endfirsthead{}
            \def\endfoot{}
            \def\endlastfoot{}
          }
          \makeatother
      - text: |
          \usepackage{booktabs}
          % EL PARCHE DEFINITIVO
          \makeatletter
          \AtBeginDocument{
            \let\longtable\tabular
            \let\endlongtable\endtabular
            \def\endhead{}
            \def\endfirsthead{}
            \def\endfoot{}
            \def\endlastfoot{}
          }
          \makeatother
      - text: |
          \usepackage{booktabs}
          % EL PARCHE DEFINITIVO
          \makeatletter
          \AtBeginDocument{
            \let\longtable\tabular
            \let\endlongtable\endtabular
            \def\endhead{}
            \def\endfirsthead{}
            \def\endfoot{}
            \def\endlastfoot{}
          }
          \makeatother
bibliography: referencias.bib
csl: ieee.csl
---

# Introducción
La escritura académica suele ser un proceso lineal, pero la maquetación es un desafío técnico. Cuando usamos dos columnas, el espacio se reduce a la mitad, lo que obliga al motor de texto a tomar decisiones difíciles sobre dónde cortar las palabras y cómo posicionar los elementos visuales.

# Desarrollo del Marco Teórico
En esta sección exploramos cómo las matemáticas se integran en el diseño. Por ejemplo, una integral compleja se ve así en una columna:

$$ \int_{0}^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2} $$

Este tipo de fórmulas son las que hacen que LaTeX sea la herramienta estándar en ingeniería, a pesar de lo difícil que es configurarla al principio.

## Análisis de Datos (La Tabla)
Aquí es donde el sistema solía fallar. Esta tabla ahora se comporta como una tabla "estática" que cabe perfectamente en la columna izquierda:

| Parámetro | Valor Clásico | Valor Optimizado |
| :--- | :--- | :--- |
| Latencia | 150ms | 12ms |
| CPU Uso | 85% | 22% |
| Rendimiento | Estable | Máximo |

# Discusión Extensa
Para ver el efecto de las dos columnas, necesitamos que el texto fluya. Imagina que aquí estamos explicando por qué Arch Linux es la mejor base para este tipo de experimentos. La libertad de instalar solo los paquetes necesarios de TeX Live nos permite tener un sistema ligero, aunque nos obliga a conocer cada pieza del motor.

Si escribes suficiente texto, verás cómo al llegar al final de la página, el cursor salta automáticamente a la columna de la derecha en la parte superior. Esto es lo que le da el "look" de revista científica a tus trabajos.

# Conclusión
Si estás leyendo esto en un PDF de dos columnas, hemos vencido a los errores de `\noalign` y `\endhead`. Ahora tienes un sistema donde solo te preocupas por escribir en Markdown y la computadora hace el trabajo sucio.

---
# Referencias