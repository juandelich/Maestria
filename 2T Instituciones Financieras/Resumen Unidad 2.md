## Unidad 2

Como se vio en la clase 1: El trade off de un seguro de depositos es la aparición de fenomenos como riesgo moral y selección adversa en los agentes.

## Como corregir los incetivos al riesgo 
### Aumentar la disiplina de los inversores
En este caso queremos entender y tomar medidas que obliguen a los inversores de las instituciones financieras a aumentar su control sobre las mismas. La opción teorica sería implementar seguros de depositos ajustados por el riesgo de cada banco. Aunque el optimo es inalcansable, existen opciones. 

En estados unidos, desde el año 1993, el seguro federal de depositos (FDCI) implementa una matrix con la cual evalua a las entidades y definen los premiums sobre sus contribuciones. Sin embargo, las diferencias entre categorias era relativamente pequeña en terminos de costos. Esto llevo a que no hubiera un efecto grande en los participantes de mercado. 

Pero en 1997 esto fue modificado, haciendo más grande la diferencia de las primas y de los bancos. Pero aun con estos cambios la mayoria de los bancos estaban aun lejos de las primas y sus pagos en concepto de castigos eran bajos o nulos. Fue en 2007 donde se tomo una postura más agresiva y todos los bancos pagarian premiums positivas.

### Aumentar la disiplina del depositante 
La implementación del seguro de deposito tiene otro efecto interesante que es la caida de las tasas de intereses sobre los depositos. Al caer el riesgo del depositante, la tasa que puede demandar es menor. Esto se ve reflejado tambien en las tasas que los bancos enfrentan en su deuda corporativa, ya que su riesgo percibido es menor. 

En la practica, y como esta en la clase 1,  la mayoria de los depositos se ven protegidos por la percepción de TBTF. Esto hace que los individuos no crean intertemporalmente la posibilidad de que el gobierno no rescate a las entidades financieras. 

En total tanto el seguro de depositos como el efecto TBTF dejan pocos incentivos a que el depositante monitoree a los bancos. 

### Aumentar la disiplina del regulador
Los reguladores tienen la capacidad de emitir leyes, decretos o normas que le permitan aumentar la responsabilidad de las instituciones. Esto los pone en una posición de enorme responsabilidad. 

Una de las medidas más comunes es la de obligar a las instituciones a tener encajes o niveles minimos de capital. Esto no solo es una reserva frente a posibles perdida, sino que actua tambien como una señal de confianza a los depositantes o como un contra balance del riesgo moral.

Tambien se puede implementar sistemas de ajuste por riesgo, donde los bancos paguen más si su cartera es más reisgosa. Tambien se ataca el problema de riesgo moral. 

## Riesgos de liquidez
El riesgo de liquidez es la posibilidad de una repentina demanda de fondos por parte de los depositantes, lo que podria obligar a las instituciones financieras a liquidar gran parte de los activos en el corto plazo y debajo de su valor de mercado. 

Puede darse desde los pasivos cuando, por ejemplo los depositantes transaccionales, demandan sus pagos. Desde los acctios, cuando se activan las lineas de credito o los prestamos entregados.

| Activos               | Pasivos y Patrimonio                    |
| --------------- | --------- |
| Treasuries |Liquidez disponible|
| Prestamos|Depositos|
||Patrimonio neto|


Los riesgo de liquidez pueden manejarse **Comprando liquidez** o **utilizando liquides existente**

### Comprando liquidez
Las entidades financieras pueden comprar liquidez mediante diversas funetes en el mercado:
- Mercado federal de fondos (federal fund market)
- Repurchase Agreement Markets (Repo)
- Issue fixed-maturity certificates of deposit

===Las desventajas de esto===

**Compra de liquidez por aumento de extracción de depositos**:

| Activos               | Pasivos y Patrimonio                    |
| --------------- | --------- |
| Treasuries |Liquidez comprada $\uparrow$|
| Prestamos|Depositos$\downarrow$|
||Patrimonio neto|

**Compra de liquidez por aumento en los pedidos de lineas de prestamo**:
| Activos               | Pasivos y Patrimonio                    |
| --------------- | --------- |
| Treasuries |Liquidez comprada $\uparrow$|
| Prestamos $\uparrow$||Depositos|
||Patrimonio neto|


### Liquidez de reserva
En este caso el banco liquida activos para afrontar la demanda de los depositantes. El problema de esto es que hace caer la hoja de balance del banco y le obligara a vender primero sus activos de mayor retorno o mayor tasa. 

**Liquiedez mediante venta de titulos**:

| Activos               | Pasivos y Patrimonio                    |
| --------------- | --------- |
| Treasuries$\downarrow$ |Liquidez comprada|
| Prestamos|Depositos$\downarrow$|
||Patrimonio neto|

**Liquiedez mediante venta uso de titulos**:

| Activos               | Pasivos y Patrimonio                    |
| --------------- | --------- |
| Treasuries$\downarrow$ |Liquidez comprada|
| Prestamos$\uparrow$|Depositos|
||Patrimonio neto|

En este caso la demanda de liquidez viene por parte de los tenedores de linea de credito no ejecutadas. 


## Liquidez y COVID-19

Como medir el risgo de liquidez:
- *Unused Commitments*: La suma de la lineas de credito aseguradas por firmas, hogares y otros. Esto es sin importar el tipo de activo, siempre y cuando de derecho de retiro de liquidez en el corto plazo. 
- Wholesale funding: Depositos a la vista, repos, deuda subordinada y otros 
- Liquidity: La suma de efectuvo, titulos del tesoro, reverse repos y algunas selectas seguridades.

$$
\text{Liquidity Risk}= \frac{\text{Unused commitments + Wholesale funding -Liquidity}}{Total Assets}
$$
