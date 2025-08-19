# 📄 Informe Final

## Introducción
El objetivo de este análisis es entender el comportamiento de evasión (churn) de los clientes de TelecomX, identificando patrones y factores que influyen en la decisión de los clientes de abandonar la empresa. Esto permitirá tomar decisiones estratégicas para reducir la evasión y mejorar la fidelización.

---

## Limpieza y Tratamiento de Datos
Se realizaron los siguientes pasos:

- Importación de los datos desde un archivo JSON en GitHub.
- Expansión de columnas anidadas (por ejemplo, información del cliente, servicios de internet y teléfono, cuenta).
- Conversión de columnas numéricas a tipo float64.
- Identificación y manejo de valores faltantes o inconsistentes (NaN o strings vacíos).
- Normalización de nombres de columnas para facilitar su manipulación.
- Transformación de variables categóricas como Yes/No a valores numéricos (1/0).

```
datos_limpio.sample(5)
```

### Se exploraron las siguientes dimensiones:

- Distribución de Churn  
  > Figura 1: distribución de la evasión de clientes.

- Churn por género  
  > Figura 2

- Churn por tipo de servicio  
  > Figura 3

- Distribución del total de cargos mensuales y totales  
  > Figura 6

---

## Conclusiones e Insights

- Alrededor de 73% representa la cantidad de clientes que se ha quedado en el servicio (Figura 1).  
- La distribución de clientes que permanecen y se van se divide equitativamente según género (Figura 2).  
- La mayoría de clientes son mes a mes, y en este grupo se observa la mayor tasa de evasión. En contraste, los contratos a un año o dos años tienen menor churn (Figura 3).  
- En el cruce entre métodos de pago y churn, se observa que la mayoría de los clientes que se van usan electronic check (Figura 4).  
- Los clientes que permanecen generan la mayor parte de los ingresos (~80%) (Figura 6).  
- Existe una diferencia notable en la evasión según tipo de contrato y métodos de pago (Figuras 3 y 4).  
- Los clientes con ciertos tipos de contrato o sin servicios adicionales tienen mayor probabilidad de churn (Figura 3).

---

## Recomendaciones

- Las campañas deben ser orientadas equitativamente.  
- Revisar la estructura de contratos y servicios adicionales para incentivar la permanencia.  
  - Enfocarse en los contratos de un año y dos años, donde la evasión es menor.  
- Revisar el método de pago de Electronic check, ya que concentra gran parte de la evasión.  
  - Posible acción: desincentivar su uso.  
- Los clientes que permanecen explican la gran mayoría de ingresos (≈80%).
