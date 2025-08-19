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
  > <a name="fig1"></a>  
![Figura 1: Distribución de la evasión](https://raw.githubusercontent.com/d4vid2025/challenge2-data-science-LATAM/main/evasion_general.png)  

- Churn por género  
  > <a name="fig2"></a>  
![Churn por tipo de contrato](https://raw.githubusercontent.com/d4vid2025/challenge2-data-science-LATAM/refs/heads/main/churn_genero.png)

- Churn por tipo de servicio  
  > <a name="fig3"></a>  
![Churn por tipo de contrato](https://raw.githubusercontent.com/d4vid2025/challenge2-data-science-LATAM/refs/heads/main/churn_contrato.png)

<a name="fig4"></a>  
![Churn por tipo de contrato](https://raw.githubusercontent.com/d4vid2025/challenge2-data-science-LATAM/refs/heads/main/churn_metodo_pago.png)

- Distribución del total de cargos mensuales y totales  
  ><a name="fig6"></a>  
![Churn por tipo de contrato](https://raw.githubusercontent.com/d4vid2025/challenge2-data-science-LATAM/refs/heads/main/churn_cuentas_totales.png)

---

## Conclusiones e Insights

- Alrededor de 73% representa la cantidad de clientes que se ha quedado en el servicio, de acuerdo al gráfico de Distribución de churn en general [Ir a Figura 1](#fig1) .
- La distribución de cliente que permanece y no pertenece se dividen equitativamente frente al género (la mitad con varones, la mitad son mujeres)[Ir a Figura 2](#fig2).
- La mayoría de cliente son mes a mes, sin embargo de aqui también se puede ver la gran mayoría de clientes que se van. Y se puede ver que los otros tipos de contratos los clientes no se van (se puede explicar por el largo plazo de los contratos)[Ir a Figura 3](#fig3).
- Respecto al cruce entre métodos de pago versus los que permanecen y se van, podemos ver una gram mayoría de los que se van son de método electronic check [Ir a Figura 4](#fig4) .
- La mayoría de los clientes que permanecen generan la mayor parte de los ingresos [Ir a Figura 6](#fig5) .
- Existe una diferencia notable en la evasión según el tipo de contrato/métodos de pago [Ir a Figura 3](#fig3) [Ir a Figura 4](#fig4) .
- Por lo tanto los clientes con ciertos tipos de contrato o sin servicios adicionales tienen mayor probabilidad de churn [Ir a Figura 3](#fig3) .

---

## Recomendaciones

- Las campañas deben ser orientadas equitativamente.  
- Revisar la estructura de contratos y servicios adicionales para incentivar la permanencia.  
  - Enfocarse en los contratos de un año y dos años, donde la evasión es menor.  
- Revisar el método de pago de Electronic check, ya que concentra gran parte de la evasión.  
  - Posible acción: desincentivar su uso.  
- Los clientes que permanecen explican la gran mayoría de ingresos (≈80%).
