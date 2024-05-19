# Análisis de Bonos

## Valoración de Bonos

Un bono es un instrumento de deuda emitido por una entidad (gobierno, corporación) que promete pagar un flujo de caja regular (cupones) y devolver el principal al vencimiento. La valoración de un bono implica calcular el valor presente de estos flujos de caja futuros.

### Elementos Clave de un Bono

1. **Cupón**: Es el interés periódico que paga el bono, generalmente expresado como un porcentaje del valor nominal.
2. **Tasa de Interés**: Es la tasa de cupón del bono.
3. **Vencimiento**: Es el período al final del cual el principal del bono se reembolsa.

### Fórmula de Valoración de un Bono

El valor de un bono (\( P \)) es la suma del valor presente de los pagos de cupón y el valor presente del principal reembolsado al vencimiento:

\[ P = \sum_{t=1}^{n} \frac{C}{(1 + r)^t} + \frac{F}{(1 + r)^n} \]

Donde:
- \( C \) es el pago del cupón (anual).
- \( r \) es la tasa de descuento (o rendimiento requerido).
- \( n \) es el número de períodos hasta el vencimiento.
- \( F \) es el valor nominal (o principal) del bono.

## Cálculo de Precios de Bonos y Rendimiento al Vencimiento (YTM - *Yield to Maturity*)

El rendimiento al vencimiento (YTM) es la tasa de retorno que un inversor obtendrá si mantiene el bono hasta su vencimiento, suponiendo que todos los pagos de cupón se reinvierten a la misma tasa.

### Fórmula del YTM

El YTM se calcula resolviendo la siguiente ecuación para \( r \):

\[ P = \sum_{t=1}^{n} \frac{C}{(1 + YTM)^t} + \frac{F}{(1 + YTM)^n} \]

El cálculo exacto del YTM requiere iteración y generalmente se realiza usando calculadoras financieras o software como Excel.

### Ejemplo en Excel

Considera un bono con:
- Valor nominal: $1,000
- Tasa de cupón: 5% anual (pagos de $50)
- Vencimiento: 10 años
- Precio de mercado: $950

Para calcular el YTM en Excel:

1. Introduce los flujos de caja en las celdas A1:A11 ($50 cada año por 10 años y $1,050 el año 10).
2. Usa la función `TIR`:

   ```excel
   =TIR(A1:A11)
   ```

Esto te dará el YTM del bono.

# Análisis de Acciones

## Valoración de Acciones (Modelo de Crecimiento Gordon)

El modelo de crecimiento Gordon, también conocido como el modelo de descuento de dividendos (DDM), valora una acción basada en los dividendos futuros que se espera que pague y la tasa de crecimiento de esos dividendos.

### Fórmula del Modelo de Crecimiento Gordon

\[ P_0 = \frac{D_0 (1 + g)}{r - g} = \frac{D_1}{r - g} \]

Donde:
- \( P_0 \) es el precio actual de la acción.
- \( D_0 \) es el dividendo más reciente.
- \( D_1 \) es el dividendo esperado en el próximo período (\( D_0 (1 + g) \)).
- \( r \) es la tasa de descuento (o rendimiento requerido).
- \( g \) es la tasa de crecimiento de los dividendos.

## Dividendos y Tasa de Descuento

1. **Dividendos**: Los pagos periódicos a los accionistas representan una porción de las ganancias de la empresa. Son fundamentales en el modelo de crecimiento Gordon.
2. **Tasa de Descuento**: Representa el rendimiento requerido por los inversores, basado en el riesgo percibido de la inversión. Se puede estimar usando el modelo de valoración de activos de capital (CAPM):

   \[ r = R_f + \beta (R_m - R_f) \]

   Donde:
   - \( R_f \) es la tasa libre de riesgo.
   - \( \beta \) es la beta de la acción.
   - \( R_m \) es el rendimiento esperado del mercado.

### Ejemplo de Valoración de Acciones

Supongamos que una empresa paga un dividendo actual (\( D_0 \)) de $2, se espera que los dividendos crezcan a una tasa del 3% anual, y el rendimiento requerido (\( r \)) es del 8%.

\[ P_0 = \frac{2 (1 + 0.03)}{0.08 - 0.03} = \frac{2.06}{0.05} = 41.2 \]

El precio de la acción sería $41.20.

# Conclusión

El análisis de bonos y acciones implica entender y aplicar varias fórmulas financieras para valorar estos instrumentos. La valoración de bonos se basa en el valor presente de los flujos de caja futuros, mientras que la valoración de acciones puede utilizar el modelo de crecimiento Gordon para estimar el precio basado en los dividendos esperados. La tasa de descuento juega un papel crucial en ambos casos, ya que refleja el costo de oportunidad y el riesgo asociado con la inversión. Excel es una herramienta poderosa que facilita estos cálculos y permite realizar análisis financieros detallados.