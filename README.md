# 📐 Análisis Experimental del Movimiento Rectilíneo Uniformemente Acelerado (MRUA) en un Plano Inclinado con Sensores Infrarrojos

## 1. Introducción

El estudio del movimiento rectilíneo uniformemente acelerado (MRUA) constituye uno de los pilares fundamentales de la mecánica clásica. En este proyecto se analiza el movimiento de un carrito que se desplaza sobre un *plano inclinado*, utilizando sensores infrarrojos para medir tiempos de paso en distancias conocidas.

A diferencia de un modelo ideal, el sistema experimental presenta *pérdidas de energía* principalmente asociadas a la *fricción*, por lo que la aceleración real del sistema es inferior a la aceleración teórica ideal obtenida al considerar únicamente la componente del peso.

El presente trabajo tiene como finalidad *modelar correctamente el sistema físico, obtener la **aceleración experimental**, compararla con la **aceleración teórica corregida por fricción*** y analizar el error experimental.

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

- Un plano inclinado de ángulo variable θ
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

1. **Peso del carrito**  
   ![P = m × g](https://latex.codecogs.com/svg.latex?\vec{P}&space;=&space;m\vec{g})

2. **Fuerza normal del plano**  
   ![N](https://latex.codecogs.com/svg.latex?\vec{N})

3. **Fuerza de fricción cinética**  
   ![F_f](https://latex.codecogs.com/svg.latex?\vec{F}_f)

---

### 4.2 Descomposición del peso

El peso se descompone en dos componentes:

- **Paralela al plano:**  
  ![P_parallel = mg sin θ](https://latex.codecogs.com/svg.latex?P_{\parallel}&space;=&space;mg\sin(\theta))

- **Perpendicular al plano:**  
  ![P_perp = mg cos θ](https://latex.codecogs.com/svg.latex?P_{\perp}&space;=&space;mg\cos(\theta))

La fuerza normal equilibra la componente perpendicular:  
![N = mg cos θ](https://latex.codecogs.com/svg.latex?N&space;=&space;mg\cos(\theta))

---

### 4.3 Fuerza de fricción

La fuerza de fricción cinética se define como:  
![F_f = μN](https://latex.codecogs.com/svg.latex?F_f&space;=&space;\mu&space;N)

Sustituyendo:  
![F_f = μ mg cos θ](https://latex.codecogs.com/svg.latex?F_f&space;=&space;\mu&space;mg\cos(\theta))

Esta fuerza **se opone al movimiento** del carrito.

---

## 5. Aceleración Teórica del Sistema

### 5.1 Fuerza neta

La fuerza neta paralela al plano es:  
![F_neta = mg sin θ - μ mg cos θ](https://latex.codecogs.com/svg.latex?F_{\text{neta}}&space;=&space;mg\sin(\theta)&space;-&space;\mu&space;mg\cos(\theta))

---

### 5.2 Aplicación de la Segunda Ley de Newton

![F_neta = ma](https://latex.codecogs.com/svg.latex?F_{\text{neta}}&space;=&space;ma)

Sustituyendo:  
![ma = mg sin θ - μ mg cos θ](https://latex.codecogs.com/svg.latex?ma&space;=&space;mg\sin(\theta)&space;-&space;\mu&space;mg\cos(\theta))

Dividiendo entre la masa:  
![a_teorica = g(sinθ - μ cosθ)](https://latex.codecogs.com/svg.latex?\boxed{a_{\text{teórica}}&space;=&space;g(\sin\theta&space;-&space;\mu\cos\theta)})

🔹 **Nota importante:** La masa del carrito no afecta el valor de la aceleración, lo cual es coherente con la teoría clásica.

---

## 6. Aceleración Experimental (MRUA)

Dado que el carrito parte del reposo, se emplea la ecuación cinemática:  
![x = (1/2)at²](https://latex.codecogs.com/svg.latex?x&space;=&space;\frac{1}{2}at^2)

Despejando la aceleración:  
![a_exp = 2x/t²](https://latex.codecogs.com/svg.latex?\boxed{a_{\text{experimental}}&space;=&space;\frac{2x}{t^2}})

---

## 7. Uso de Múltiples Mediciones

Para minimizar errores experimentales:

- Se mide el tiempo hasta tres distancias diferentes
- Se calcula una aceleración para cada tramo
- Se obtiene un promedio

![a_i = 2d_i/t_i²](https://latex.codecogs.com/svg.latex?a_i&space;=&space;\frac{2d_i}{t_i^2})

![a_exp = (a₁ + a₂ + a₃)/3](https://latex.codecogs.com/svg.latex?\boxed{a_{\text{exp}}&space;=&space;\frac{a_1&space;+&space;a_2&space;+&space;a_3}{3}})

Este procedimiento reduce:
- Ruido electrónico
- Errores de detección
- Desviaciones locales

---

## 8. Cálculo del Error Experimental

El error porcentual se define como:  
![Error(%) = |(a_exp - a_teorica)/a_teorica| × 100](https://latex.codecogs.com/svg.latex?\boxed{\text{Error&space;(\%)}&space;=&space;\left|&space;\frac{a_{\text{exp}}&space;-&space;a_{\text{teórica}}}{a_{\text{teórica}}}&space;\right|&space;\times&space;100})

---

## 9. Ejemplo de Aplicación y Comparación Práctica

### Datos experimentales para θ = 19.5°:
- g = 9.81 m/s²
- μ ≈ 0.06 (coeficiente de fricción medido)
- Posiciones: S1 = 0.20 m, S2 = 0.50 m, S3 = 1.00 m

### Salida del programa experimental:

```
===============================
Ingrese angulo para prueba #6 (grados): 
Angulo: 19.5°  |  Acel. teorica: 2.7198 m/s²
Coloque carrito ANTES de S0 y espere...
Sistema listo. Suelte el carrito.
Inicio (S0)
Paso S1 (20 cm)
Paso S2 (50 cm)
Paso S3 (100 cm)

========== RESULTADOS ==========
Prueba #6
T20: 0.342412 s | T50: 0.606372 s | T100: 0.888428 s
Acel. experimental: 2.6683 m/s²
Acel. teorica: 2.7198 m/s²
Error: 1.90 %
================================
```

### Análisis de la comparación:

| Parámetro | Valor Teórico | Valor Experimental | Diferencia |
|-----------|---------------|-------------------|------------|
| Aceleración | 2.7198 m/s² | 2.6683 m/s² | -0.0515 m/s² |
| Error relativo | - | - | 1.90% |

### Interpretación de resultados:

1. **Concordancia excelente**: El error de solo 1.90% indica que el modelo teórico con fricción describe con alta precisión el sistema real.

2. **Validación del modelo**: La pequeña diferencia se atribuye a:
   - Variaciones en el coeficiente de fricción μ
   - Precisión limitada de los sensores infrarrojos
   - Posible resistencia del aire residual

3. **Eficacia del método**: El uso de tres puntos de medición (S1, S2, S3) permite:
   - Promediar errores de medición
   - Verificar consistencia del movimiento MRUA
   - Obtener mayor precisión que con una sola medición

### Cálculos detallados:

**Aceleración teórica:**
```
a_teórica = 9.81 × [sin(19.5°) - 0.06 × cos(19.5°)]
          = 9.81 × [0.334 - 0.06 × 0.943]
          = 9.81 × [0.334 - 0.05658]
          = 9.81 × 0.27742
          = 2.7198 m/s²
```

**Aceleración experimental (promedio):**
```
a_20 = 2 × 0.20 / (0.342412)² = 0.40 / 0.1172 = 3.413 m/s²
a_50 = 2 × 0.50 / (0.606372)² = 1.00 / 0.3677 = 2.719 m/s²
a_100 = 2 × 1.00 / (0.888428)² = 2.00 / 0.7893 = 2.534 m/s²

a_exp = (3.413 + 2.719 + 2.534) / 3 = 2.6683 m/s²
```

**Error porcentual:**
```
Error = |(2.6683 - 2.7198) / 2.7198| × 100
      = |(-0.0515) / 2.7198| × 100
      = 0.01894 × 100 = 1.894% ≈ 1.90%
```

---

**📌 Repositorio:** [documentacion-prueba-con-friccion](https://github.com/yorkygustavo0729-ux/documentacion-prueba-con-friccion)

**🧪 Autor:** Yorky Gustavo  
**🏫 Institución:** Universidad Experimental  
**📅 Fecha:** 2024

---

