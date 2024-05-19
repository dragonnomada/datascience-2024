# Sistemas de Amortización de Préstamos

Existen varios sistemas de amortización, entre los más comunes se encuentran:

1. **Amortización Francesa (Cuotas Constantes)**
2. **Amortización Alemana (Cuotas Decrecientes)**
3. **Amortización Americana (Interés Simple)**
4. **Amortización Italiana (Capital Fijo)**

# Amortización Francesa (Cuotas Constantes)

En este sistema, el pago periódico es constante a lo largo de la vida del préstamo. Cada pago incluye una parte de intereses y una parte de capital.

## Fórmula de la Cuota Constante

\[ A = \frac{P \times r(1 + r)^n}{(1 + r)^n - 1} \]

Donde:
- \( A \) es el pago periódico.
- \( P \) es el monto del préstamo.
- \( r \) es la tasa de interés por período.
- \( n \) es el número total de pagos.

## Ejemplo

Si tienes un préstamo de $10,000 a una tasa de interés anual del 6% (0.5% mensual) por 5 años (60 meses), el pago mensual sería:

\[ A = \frac{10000 \times 0.005(1 + 0.005)^{60}}{(1 + 0.005)^{60} - 1} \approx 193.33 \]

# Amortización Alemana (Cuotas Decrecientes)

En este sistema, los pagos de intereses se calculan sobre el saldo pendiente, mientras que el capital se amortiza en partes iguales en cada período. Esto resulta en pagos totales decrecientes a lo largo del tiempo.

## Fórmula del Pago de Capital Fijo

\[ C = \frac{P}{n} \]

Donde:
- \( C \) es la parte de capital pagada en cada período.
- \( P \) es el monto del préstamo.
- \( n \) es el número total de pagos.

El interés se calcula sobre el saldo pendiente de cada período:

\[ I_t = P_t \times r \]

Donde:
- \( I_t \) es el interés del período \( t \).
- \( P_t \) es el saldo pendiente al inicio del período \( t \).

El pago total en el período \( t \) sería:

\[ A_t = C + I_t \]

## Ejemplo

Para un préstamo de $10,000 a una tasa de interés anual del 6% (0.5% mensual) por 5 años (60 meses):

\[ C = \frac{10000}{60} \approx 166.67 \]

El primer pago mensual sería:

\[ I_1 = 10000 \times 0.005 = 50 \]

\[ A_1 = 166.67 + 50 = 216.67 \]

El segundo pago mensual sería:

\[ P_2 = 10000 - 166.67 = 9833.33 \]

\[ I_2 = 9833.33 \times 0.005 \approx 49.17 \]

\[ A_2 = 166.67 + 49.17 \approx 215.84 \]

# Amortización Americana (Interés Simple)

En este sistema, solo se pagan los intereses periódicamente y el capital se paga al final del período del préstamo. Este sistema es menos común para préstamos personales y más común en inversiones a corto plazo.

## Fórmula del Interés Simple

\[ I = P \times r \times t \]

Donde:
- \( I \) es el interés total.
- \( P \) es el monto del préstamo.
- \( r \) es la tasa de interés por período.
- \( t \) es el tiempo total del préstamo.

## Ejemplo

Para un préstamo de $10,000 a una tasa de interés anual del 6% por 5 años:

\[ I = 10000 \times 0.06 \times 5 = 3000 \]

Los intereses anuales serían $600, y el capital de $10,000 se pagaría al final de los 5 años.

# Amortización Italiana (Capital Fijo)

En este sistema, el pago del capital es constante en cada período, pero el pago de intereses disminuye a medida que se reduce el saldo pendiente.

## Fórmula del Pago de Capital Fijo

\[ C = \frac{P}{n} \]

El interés se calcula sobre el saldo pendiente de cada período:

\[ I_t = P_t \times r \]

El pago total en el período \( t \) sería:

\[ A_t = C + I_t \]

## Ejemplo

Para un préstamo de $10,000 a una tasa de interés anual del 6% por 5 años (60 meses):

\[ C = \frac{10000}{60} \approx 166.67 \]

El primer pago mensual sería:

\[ I_1 = 10000 \times 0.005 = 50 \]

\[ A_1 = 166.67 + 50 = 216.67 \]

El segundo pago mensual sería:

\[ P_2 = 10000 - 166.67 = 9833.33 \]

\[ I_2 = 9833.33 \times 0.005 \approx 49.17 \]

\[ A_2 = 166.67 + 49.17 \approx 215.84 \]

# Creación de Tablas de Amortización en Excel

Una tabla de amortización en Excel puede ayudar a visualizar cómo se dividen los pagos entre el capital y los intereses a lo largo del tiempo. Aquí te dejo los pasos para crear una tabla de amortización francesa (cuotas constantes):

1. **Encabezados de las Columnas**: Periodo, Pago, Intereses, Capital, Saldo.
2. **Fórmulas**:
   - Pago: Usa la función `=PAGO(tasa, nper, va)`.
   - Intereses: `=saldo_inicial * tasa`.
   - Capital: `=pago - intereses`.
   - Saldo: `=saldo_inicial - capital`.