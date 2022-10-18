# Resumen Instituciones Financieras
## Clase 1 - Intermediarios financieros

En la primera clase se discute el rol del los agentes de liquidez en la economia. Esto abarca la creación de liquidez así como la posibilidad de mover intertemporalmente riqueza por parte de los agentes. Se presenta un modelo simple de dos periodos, el mismo apunta a entender posibles elementos de corridas bancarias y estabilidad financiera. Por ultimo se ve evidencia empirica del fenomeno *Too big to Fail*

### Que son las instituciones y los intermediarios finacieros

En los modelos clasicos o introductorios de macroeconomia solemos simplificar la relación entre los hogares y las firmas. En este sentido los hogares financian directamente a las firmas mediante sus ahorros, y las mismas retribuyen pagando un interes igual a la tasa marginal de capital.

$$
\frac{Hogares}{\text{ Ahorradores Netos}} \Longleftrightarrow \frac{Firmas}{\text{ Acreedores netos}}
$$
Obviamente los modelos son simplificaciones o suponen que los agentes se comportaran *como si* (*as if*), pero vale la pena señalar cuales serian los problemas de un mundo así

- **Selección Adversa**: En este caso, todos los hogares deberían evaluar a todas las firmas para lograr identificar a aquellas que merecen recibir capital. Esto requiere grandes cantidades de trabajo, que a su vez es repetido por todos y los costos de este exceso absorbidos por todos. 
- **Moral Hazard**: Las familias no solo deberían evaluar a los hogares antes de prestar el dinero, sino que tambien deberian hacer un monitoreo de las mismas. Ya que de no hacerlo las firmas tendrian incentivos a no cumplir con sus promesas. 
- **Problemas de liquidez y plazos**: Las firmas y los agentes pueden tener horizontes de inversión y retorno distitnos. En una economia pueden convivir multiples generaciones que en distintos momentos invierten en distintas firmas.

En resumen tenemos una situación donde hay altos costos de información y por lo tanto menores fondos. Las instituciones financieras pueden ser un vehiculo que resuelva ambos problemas. 

````mermaid
graph LR

A{{Households}} --> |Efectivo| B(Instituciones financiaeras)

B{{Instituciones financiaeras}} --> |Depositos|A

B -->|Efectivo|C[Firmas]

C{{Firmas}} -->|Bonos y Acciones| B

````

[![](https://mermaid.ink/img/pako:eNp1kM1qwzAMx1_F6LRB-wI5DJK0g0FP23HeQdjKIrbYwVYGxcm7T8EtO00nffwk_aUCLnqCBj4TzqO5vNpg1NpS-jFxlgnztpnj8cms54Gc8E9cTffwErKwLI5joGwGDhgcIyXMj3VAV8r_zH3iieaYWWJe21vXnv9b1L8_c1IFH7Xal1Lj2r92McRsrqZ1dYcK20E4wESKsdezyp6xICNNZKFR12P6smDDptwyexQ6e9WQoBnwO9MBcJH4dg0OGkkL3aETo75oulHbL-3Ya8w)](https://mermaid-js.github.io/mermaid-live-editor/edit#pako:eNp1kM1qwzAMx1_F6LRB-wI5DJK0g0FP23HeQdjKIrbYwVYGxcm7T8EtO00nffwk_aUCLnqCBj4TzqO5vNpg1NpS-jFxlgnztpnj8cms54Gc8E9cTffwErKwLI5joGwGDhgcIyXMj3VAV8r_zH3iieaYWWJe21vXnv9b1L8_c1IFH7Xal1Lj2r92McRsrqZ1dYcK20E4wESKsdezyp6xICNNZKFR12P6smDDptwyexQ6e9WQoBnwO9MBcJH4dg0OGkkL3aETo75oulHbL-3Ya8w)

#### Tipos de instituciones financieras
- **Brokers puros**: Estas entindades cumplen simplemente el rol de intermediarios entre las firmas y los hogares. Toman los instrumentos creados por las firmas y el efectivo de los hogares, para hacer un match entre ellos. A su vez, puede reducir los costos de screening para los activos que las firmas emiten.
- **Tranformadores de activos**: Este agente tiene multiples caracteristicas, pero centralmente es creador de liquidez y de mercado. Esto es en contraposición con aquellos que solo intermedian entre los agentes. Estas instituciones pueden tomar activos iliquidos y transformarlos en activos liquidos, como los prestamos hipotecarios en bonos respaldados. A su vez pueden tomar gran cantidad de riesgo de agentes y diversificarlo, como cuando se ofrece un estructurado. De la misma manera puede hacer un *match* entre las necesidades de duración de los agentes.

**Regulación**: La relavancia que estas instituciones han tomado, sumado a la sensibilidad, lleva a que esten alramente reguladas. Los hacedores de politica intentan a toda cosa **disuadir a las firmas de tomar riesgo excesivo** (*Requrimientos minimos de capital*) e intentar promover la diversificación(*Limitaciones al peso de cierto prestamista*).


### Modelo de creación de liquidez y corrida bancaria

#### Moralejas

- Monopolies price following the inverse elasticity of demand: $L = \frac{1}{\eta}$. Prices (markup) are higher in inelastic markets
- In the monopoly model, setting price or setting quantity leads to the same results.

#### Intuiciones

- Lorem ipsum dolor sit amet.

- Consectetur adipiscing elit.

#### Setting - Supuestos importantes a mencionar

- En este modelo los agentes invierten en un banco debido a una preferencia de liquidez. El banco permite hacer un puente entre ambos periodos con la posibilidad de obtener liquidez en cualquiera de ellos. La demanda de liquidez esta determinada por la posible incertidumbre de consumo de los agentes y por el plazo que desean sostener un activo. 
- Los agente s
-  Este modelo presenta un activo cuya tasa de retorno es distinta para cada periodo. La tasa del periodo dos es superior al del primero ($r(1)<r(2)$), mientra que la liquidez del activo se mide como la tasa entre los retornos ($\frac{r(1)}{r(2)}$). Si el coeficiente se acerca a uno es que el activo es completamente liquido, entre más cercanoa cero más iliquido.

#### Resolución 

> Notar, no hay una parte de "conclusiones", porque la idea es que estén en **Moralejas.** La idea es después poder *llegar hasta ellas.*

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas sit amet nunc ut ligula imperdiet venenatis ut id urna. Donec eu quam eget purus ultricies volutpat. Quisque eleifend leo in massa congue consectetur. Duis quis tempor dui. Fusce vitae dolor nulla. Suspendisse varius quam dui, sed imperdiet arcu venenatis a. Ut sed ex mauris. Morbi ac venenatis magna, nec gravida ante. Proin varius nisi leo. Ut mollis tortor eget efficitur iaculis. Morbi rhoncus ipsum erat, eu condimentum leo posuere ultricies. Phasellus non risus vitae augue sollicitudin fermentum. Etiam vel auctor elit. Aliquam at enim ipsum. Mauris eu consequat velit.


==Modelo no terminado==


## Garantias implicitas, explicitas y riesgo moral
Una manera de frenar las corridas es establecer mecanismos explicitos o implicitos con los cuales garantizar que las personas confien en el sistema bancario. Los explicitos funcionan meidante regulaciones y los implicitos mediante expectativas.

### Seguro de depositos (Explicitos)
Una opción para evitar los panicos relacionados a corridas bancarias es la creción de de seguros de depositos. El seguro de depositos esta garantizado por el gobierno con los depositantes y no con los bancos. Obviamente hay un factor de credibilidad donde los depositantes tienen que confiar en que el gobierno cumplira la promesa. 

### *Too Big To Fail(TBTF)*
Algunas instituciones puede tornarnes extremadamente grandes en termino de balances sobre el sistema financiero, lo cual hace su rol fundamental en la economia. Siguiendo esto los agentes pueden derivar que los gobiernos tienen demasiados incentivos para rescatarlos en caso de colapso, tambien pueden hacerlo los mismos bancos. Aunque esto puede generar garantias, esto tambien genera problemas de riesgo moral. 

### Riesgo moral
La idea de que los depositos esten asegurados, o de que existan garantias, lleva a que los bancos tengan más incentivos para correr o tomar más riesgos. Llamamos a esto problemas de riesgo moral. Esto puede manifestarse como tomando más prestamos subprime o tomando más activos riesgosos de otro tipo. 


## Caso empirico 1: TBTF bond premiums USA 90's

### Motivación 
En los estuados unidos en los 90 hubo una ola de fusiónes en los bancos privados, lo que llevo a que algunos bancos crecieran. 
### Hipotesis 
Los bancos grandes tienen un premium en el valor de su deuda por su status percibido de TBTF. Es decir que hay una suerte de garantia implicita, donde los agentes percibirian a algunos bancos como más seguros. Esto sería porque los gobiernos impedirian su caida

### Resultados 
La evidencia muestra que hay retornos abnormales luego de las fechas de los anuncios de fusión, donde los bonos tienen saltos en los rendimientos. Pero estos saltos solo suceden en la fusión de los bancos medios que superaban la vara de los 100 mil millones y pasaban entonces a ser TBTF. Por otro lado, los bancos que ya eran TBTF, no vieron una ganancia en terminos de su spread pos fusión

### Implicaciones 
De esto podemos ver que el mercado incorpora en el precio de que un banco es TBTF, lo que podría reducir la disciplina de mercado. Esto es ya que no es creible la amenza de no rescate de los policy makers y por lo tanto el mercado castiga menos la toma de riesgos 

## Caso empirico 2: Garantias explicitas en bolivia 

### Motivación 
Bolivia tuvo una incorporación tardía del seguro de depositos, lo que permite intentar verificar si una garantia explicita aumenta los riesgos a los que se expone la institución.

### Hipotesis 
En este caso se observo la cartera de prestamos de la institución y se la compara antes y despues de la medida. Si aumentara el incentivo a tomar riesgos se vería un aumento de los prestamos Sub-prime sobre el portafolio total. 
### Resultados 
Los primeros resultados mostraron un aumento en los depositos subprime de 6,8%, mientras que los bancos no compesaron esta subida requiriendo más colateral o acortando las duraciones.


El paper mostro que los seguros de depositos reducen las corridas bancarias pero a su vez quitan incentivos a la disciplina de mercado. 