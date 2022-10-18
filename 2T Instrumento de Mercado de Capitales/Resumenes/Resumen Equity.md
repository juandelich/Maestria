# Resumen de Equity


## Analisis tecnico 

## Valuación de activos
El analsisi fundamental se centra en en entender cual es el valor intrinseco de una compañia y se esta esta por arriba o por debajo del mismo. Exista dos aproximaciones a la valuación de empresas: 
- **Relativa**:  buscamos una compañía comparable que ya este en el mercado, y comparamos “características”. Generalmente esto toma la forma de valuación por multiplos. 
- **Absoluta**: Descontamos cash flows futuros de la firma, así tratamos de obtener una valuación de cuanto genera la misma. Descontamos cash flows futuros.

### Relativa
En el caso de la valuación relativa, miramos algunos multiplos derivados del análsis de los balances de la firma.

#### Indicadores de Solvencia 
- **Asset/Equity**:
- **Liability/Equity**:
- **Financial Debt/Equity**: Es la suma de la linea de prestamos 
- **Net Financial Debt/Equity**: A la Financial debt se le resta las tenencias en efectivo e Inversiones financieras. 

#### Indicadores de Liquidez
- **Ratio Corriente**: Activo corriente/Pasivo corriente
- **Test ácido**: (Efectivo + inversiones financieras + deudores por ventas)/ Pasivo corriente
- **Cash Test**: Toma solamente la liquidez controlada por la compañia = (efectivo e inversiones financiras)/ Pasivo corriente 


#### Indicadores de rentabilidad
- **ROA**: EBIT/ Assets
- **ROE**: Net Income/ Equity
- **ROIC**: EBIT/(Net Debt+Equity)

### Absoluta
#### Dividend Discount (Modelo de Gordon)
Este punto intenta enfocarse en la valuación de una manera similar a renta fija, donde tratamos de ver un flujo de cashflows futuros con los dividendos como pagos. Tambien suponemos un crecimiento sucesivo de los dividendos en linea con el crecimiento de la empresa, y descontamos esos futuros rendimientos con la misma tasa de descuento. Esto solo converge si la tasa de descuento es mayor a la tasa de crecimiento de los dividendos, de forma que se da:

$$
V_0 = \frac{D_0(1+g)}{k-g}

$$
En este caso $g$ represetna el crecimiento de los dividendos y $k$ el factor de descuento. 

Pero que pasa si la empresa no reparte dividendos? Vale menos? No necesariamente, la reinversión de dividendos a una tasa de retornos  mayor a la de descuento genera un mayor valor.  Esta posibilidad de retorno se mide con el *Return on Equity (ROE)*, entonces suvecede cuando el ROE es mayor a la tasa de descuento K

El $V_0$ que mostramos arriba puede pensarse tambien como un valor terminal de las firmas, visto en [[Caso 1.pdf]] de finanzas corporativas. En este caso lo llamaremos *Present Value of Growth Opportunities (PVGO)*. La idea es que el precio presente debe ser igual a la suma de los activos de una empresa y su PVGO. 

$$
\begin {aligned}

P_0 =\frac{E_1}{k}+PVGO

\\

\frac{P_0}{E_1} = \frac{1}{k}(1+\frac{PVGO}{E/k})

\\

𝑃_0 = \frac{𝐸_1(1 − 𝑏)}{ 𝑘 − 𝑅𝑂𝐸 ∗ b}
\end {aligned}
$$
Con lo que P/E captura la expectativa de crecimiento en PVGO. En el modelo con crecimiento constante de los dividendos, con $D=E(1-b)$, $g=ROE . b$. Y por ende P/E se incrementa con el ROE. Cuando el ROE es mayor a k, los inversores prefieren que la firma re-invierta. Cuando es menor, que pague dividendos.

#### * Model (FCFF)* 
En algunos casos las compañías no pagan dividendos durante un tiempo, y la valuación por Modelo de Gordon no es posible. Pero se puede mirar el ***free cash flow of the firm (FCFF)*** descontado al promedio ponderado del costo promedio de fondeo (***weighted average cost of funding)(“WACC”)*** para obtener el valor de la firma, y luego restarle la deuda. Alternativamente, se puede mirar desde el principio el ***free cash flow a los equity holders (FCFE)***. Miremos esas dos posibilidades. 

$$
FCFF = EBIT (1 -t) + Depreciación − Capex - \text{Variación ev NWC}
$$
Donde $t$ reprensenta el corporate tax rate y $NWC$ es el net working capital.  A partir de esto tambien se puede sacar el *enterprise value (EV)*. Esto lo hacemos descontando nuestro FCFF por nuestra WACC. La WACC reprensenta el costo ponderado del financiamiento, considerando que la empresa puede obtener tanto equity como deuda (A la cual se le descuenta sus beneficios impositivos). 
$$
FCFE = FCFF - \text{Gastos de interes} * (1-t)+\text{Variación neta de deuda} 
$$
$$
\begin {aligned}

\text{Firm Value}= \sum_{t=1}^T{\frac{{FCFF}_t}{(1+WACC)^t}+\frac{P_T}{(1+WACC)^T}}

\\

P_t=\frac{FCFF_{T+1}}{WACC-g}

\end {aligned}
$$
$P_T$ es un valor terminal para el FCFF, descontado a la eternidad. En esa ultima parte se suele usar el modelo de Gordon, asumiendo un crecimiento constante del FCFF.

Alternativamente, podemos descontar free cash flows to equity (FCFE), al costo $k_E$
$$\begin {aligned}

\text{Market Value of Equity}= \sum_{t=1}^T{\frac{{FCFE}_t}{(1+k_E)^t}+\frac{P_T}{(1+k_E)^T}}

\\

P_t=\frac{FCFE_{T+1}}{K_e-g}

\end {aligned}$$
