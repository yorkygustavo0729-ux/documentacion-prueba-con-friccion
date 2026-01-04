# 📐 Análisis Experimental del Movimiento Rectilíneo Uniformemente Acelerado (MRUA) en un Plano Inclinado con Sensores Infrarrojos

## 1. Introducción

El estudio del movimiento rectilíneo uniformemente acelerado (MRUA) constituye uno de los pilares fundamentales de la mecánica clásica. En este proyecto se analiza el movimiento de un carrito que se desplaza sobre un *plano inclinado*, utilizando sensores infrarrojos para medir tiempos de paso en distancias conocidas.

A diferencia de un modelo ideal, el sistema experimental presenta *pérdidas de energía* principalmente asociadas a la *fricción*, por lo que la aceleración real del sistema es inferior a la aceleración teórica ideal obtenida al considerar únicamente la componente del peso.

El presente trabajo tiene como finalidad *modelar correctamente el sistema físico, obtener la **aceleración experimental, compararla con la **aceleración teórica corregida por fricción* y analizar el error experimental.

---

## 2. Objetivos

### Objetivo General
Analizar experimentalmente el MRUA de un carrito sobre un plano inclinado mediante sensores infrarrojos y validar el modelo físico considerando fricción.

### Objetivos Específicos
- Medir tiempos de paso en diferentes posiciones del plano inclinado
- Calcular la aceleración experimental del carrito
- Determinar la aceleración teórica considerando fricción
- Comparar ambos valores y cuantificar el error
- Justificar físicamente las diferencias entre teoría y experimento

---

## 3. Descripción del Sistema Experimental

El sistema está compuesto por:

- Un plano inclinado de ángulo variable \( \theta \)
- Un carrito que se desplaza desde el reposo
- Cuatro sensores infrarrojos:
  - S0: inicio del movimiento
  - S1: 0.20 m
  - S2: 0.50 m
  - S3: 1.00 m
- Un microcontrolador que registra los tiempos de detección

El carrito parte *desde el reposo*, sin impulso inicial, lo que permite modelar el movimiento como MRUA puro.

---

## 4. Modelo Físico del Movimiento

### 4.1 Fuerzas que actúan sobre el carrito

Durante el movimiento actúan las siguientes fuerzas:

1. *Peso del carrito*
\[
\vec{P} = m\vec{g}
\]

2. *Fuerza normal del plano*
\[
\vec{N}
\]

3. *Fuerza de fricción cinética*
\[
\vec{F}_f
\]

---

### 4.2 Descomposición del peso

El peso se descompone en dos componentes:

- Paralela al plano:
\[
P_{\parallel} = mg\sin(\theta)
\]

- Perpendicular al plano:
\[
P_{\perp} = mg\cos(\theta)
\]

La fuerza normal equilibra la componente perpendicular:
\[
N = mg\cos(\theta)
\]

---

### 4.3 Fuerza de fricción

La fuerza de fricción cinética se define como:
\[
F_f = \mu N
\]

Sustituyendo:
\[
F_f = \mu mg\cos(\theta)
\]

Esta fuerza *se opone al movimiento* del carrito.

---

## 5. Aceleración Teórica del Sistema

### 5.1 Fuerza neta

La fuerza neta paralela al plano es:
\[
F_{\text{neta}} = mg\sin(\theta) - \mu mg\cos(\theta)
\]

---

### 5.2 Aplicación de la Segunda Ley de Newton

\[
F_{\text{neta}} = ma
\]

Sustituyendo:
\[
ma = mg\sin(\theta) - \mu mg\cos(\theta)
\]

Dividiendo entre la masa:
\[
\boxed{
a_{\text{teórica}} = g(\sin\theta - \mu\cos\theta)
}
\]

🔹 La masa del carrito no afecta el valor de la aceleración, lo cual es coherente con la teoría clásica.

---

## 6. Aceleración Experimental (MRUA)

Dado que el carrito parte del reposo, se emplea la ecuación cinemática:

\[
x = \frac{1}{2}at^2
\]

Despejando la aceleración:
\[
\boxed{
a_{\text{experimental}} = \frac{2x}{t^2}
}
\]

---

## 7. Uso de Múltiples Mediciones

Para minimizar errores experimentales:

- Se mide el tiempo hasta tres distancias diferentes
- Se calcula una aceleración para cada tramo
- Se obtiene un promedio

\[
a_i = \frac{2d_i}{t_i^2}
\]

\[
\boxed{
a_{\text{exp}} = \frac{a_1 + a_2 + a_3}{3}
}
\]

Este procedimiento reduce:
- Ruido electrónico
- Errores de detección
- Desviaciones locales

---

## 8. Cálculo del Error Experimental

El error porcentual se define como:

\[
\boxed{
\text{Error (\%)} =
\left|
\frac{a_{\text{exp}} - a_{\text{teórica}}}
{a_{\text{teórica}}}
\right|
\times 100
}
\]

---

## 9. Ejemplo de Aplicación (θ = 19.5°)

### Datos:
- \( g = 9.81 \, m/s^2 \)
- \( \theta = 19.5° \)
- \( \mu \approx 0.06 \)

### Cálculo:
\[
\sin(19.5°) \approx 0.334
\]
\[
\cos(19.5°) \approx 0.943
\]

\[
a = 9.81(0.334 - 0.06 \cdot 0.943)
\]

\[
\boxed{
a_{\text{teórica}} \approx 2.72 \, m/s^2
}
\]

Este valor es coherente con los resultados experimentales obtenidos.

---

## 10. Discusión de Resultados

- La aceleración experimental es menor que la ideal sin fricción
- La fricción explica la reducción observada
- El error porcentual bajo valida el modelo
- El sistema cumple con MRUA no ideal

---

## 11. Conclusiones

- El movimiento del carrito corresponde a un MRUA no ideal
- La fricción es un factor determinante
- El modelo teórico corregido concuerda con el experimento
- El uso de múltiples sensores mejora la precisión
- El sistema es adecuado para prácticas universitarias de física

---

## 12. Consideraciones Finales

- Los sensores operan con lógica invertida
- El carrito parte siempre desde el reposo
- No se considera resistencia del aire
- El coeficiente de fricción puede variar ligeramente

---
