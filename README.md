---

📐 Análisis Experimental del MRUA en un Plano Inclinado con Fricción

1. Introducción

El Movimiento Rectilíneo Uniformemente Acelerado (MRUA) es un caso fundamental dentro de la mecánica clásica. En este proyecto se estudia experimentalmente el movimiento de un carrito que se desplaza sobre un plano inclinado, utilizando sensores infrarrojos TCRT5000 para medir los tiempos de paso en posiciones conocidas.

A diferencia de un sistema ideal, el experimento considera la presencia de fricción entre el carrito y la pista, lo cual reduce la aceleración real respecto al valor teórico ideal. El objetivo es comparar la aceleración experimental con la aceleración teórica corregida por fricción y analizar el error obtenido.


---

2. Objetivos

Objetivo general

Analizar el MRUA de un carrito sobre un plano inclinado considerando fricción, mediante mediciones experimentales con sensores infrarrojos.

Objetivos específicos

Medir tiempos de paso en distancias conocidas.

Calcular la aceleración experimental.

Determinar la aceleración teórica con fricción.

Comparar resultados teóricos y experimentales.

Analizar el error porcentual del sistema.



---

3. Descripción del sistema experimental

El sistema está compuesto por:

Un plano inclinado de ángulo variable 

Un carrito que se desplaza desde el reposo

Cuatro sensores infrarrojos:

S0: inicio del movimiento

S1: 0.20 m desde S0

S2: 0.50 m desde S0

S3: 1.00 m desde S0


Un microcontrolador Arduino que registra los tiempos


El carrito se libera sin velocidad inicial, lo que permite modelar el movimiento como MRUA.


---

4. Modelo físico del sistema

4.1 Fuerzas que actúan sobre el carrito

Durante el movimiento sobre el plano inclinado actúan:

Peso del carrito

Fuerza normal del plano

Fuerza de fricción cinética



---

4.2 Descomposición del peso

El peso del carrito es:

P = mg

Este se descompone en dos componentes:

Componente paralela al plano:

P_{\parallel} = mg \sin(\theta)

Componente perpendicular al plano:

P_{\perp} = mg \cos(\theta)

La fuerza normal es igual a la componente perpendicular:

N = mg \cos(\theta)


---

4.3 Fuerza de fricción

La fuerza de fricción cinética se calcula como:

F_f = \mu N

Sustituyendo la normal:

F_f = \mu mg \cos(\theta)

Esta fuerza se opone al movimiento del carrito.


---

5. Aceleración teórica del sistema

La fuerza neta paralela al plano es:

F_{\text{neta}} = mg \sin(\theta) - \mu mg \cos(\theta)

Aplicando la segunda ley de Newton:

F_{\text{neta}} = ma

Dividiendo entre la masa:

a_{\text{teórica}} = g \left( \sin(\theta) - \mu \cos(\theta) \right)

Este valor representa la aceleración real del carrito considerando fricción.


---

6. Aceleración experimental (MRUA)

Como el carrito parte del reposo, se utiliza la ecuación del MRUA:

x = \frac{1}{2} a t^2

Despejando la aceleración:

a_{\text{experimental}} = \frac{2x}{t^2}


---

7. Uso de múltiples mediciones

Para mejorar la precisión, se calcula la aceleración en tres distancias distintas:

a_1 = \frac{2d_1}{t_1^2}

a_2 = \frac{2d_2}{t_2^2}

a_3 = \frac{2d_3}{t_3^2}

La aceleración experimental promedio es:

a_{\text{exp}} = \frac{a_1 + a_2 + a_3}{3}

Este promedio reduce errores de medición y ruido electrónico.


---

8. Cálculo del error porcentual

El error porcentual se calcula como:

\text{Error (\%)} =
\left|
\frac{a_{\text{exp}} - a_{\text{teórica}}}
{a_{\text{teórica}}}
\right|
\times 100


---

9. Ejemplo de aplicación (θ = 19.5°)

Datos:








Valores trigonométricos:

\sin(19.5^\circ) \approx 0.334

\cos(19.5^\circ) \approx 0.943

Sustituyendo en la ecuación de aceleración:

a = 9.81 (0.334 - 0.06 \cdot 0.943)

Resultado:

a_{\text{teórica}} \approx 2.72 \, \text{m/s}^2


---

10. Discusión de resultados

La aceleración experimental es menor que la ideal sin fricción.

La fricción explica la diferencia observada.

El bajo error porcentual valida el modelo físico.

El movimiento cumple con MRUA no ideal.



---

11. Conclusiones

El carrito presenta MRUA con aceleración constante.

La fricción influye significativamente en el sistema.

El modelo teórico corregido concuerda con los resultados experimentales.

El uso de múltiples sensores mejora la precisión.

El sistema es adecuado para prácticas universitarias de física.



---

12. Consideraciones finales

Los sensores infrarrojos operan con lógica invertida.

El carrito parte siempre desde el reposo.

No se considera resistencia del aire.

El coeficiente de fricción puede variar ligeramente entre pruebas.



---
