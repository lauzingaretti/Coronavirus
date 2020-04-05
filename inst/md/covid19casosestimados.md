# ¿Qué dicen las matemáticas sobre el covid-19 en Argentina?

## ¿Cuántos casos de covid-19 hay en Argentina a día de hoy (5-4-2020)?

El gobierno argentino informa diariamente la evolución del covid-19 a través de la página web del ministerio de salud, https://www.argentina.gob.ar/coronavirus/informe-diario. En el informe matutino del día de hoy, reporta 1451 casos y 44 muertes. 


Sin embargo, el número de casos de covid-19 está subestimado en la mayoría de los países porque no se hacen suficientes exámenes y se sabe que muchos infectados son asintomáticos. Ante este contexto, cabe preguntarse si es posible saber aproximadamente cuál es el número real de infectados. La **matemática** puede ayudarnos.


## Distribución de muertes covid-19 en Argentina por edad 

La siguiente tabla, arroja el número de defunciones en Argentina por rango de edades. Cabe destacar que de estos muertos, el 68\% son hombres y el 32\% mujeres. 

|<30|30-39|40-49|50-59|60-69|70-80|>80|
|:----:|--|-----|-----|-----|-----|---|
|0  | 0   | 3  | 10   | 11  | 12  | 8 |

Un dato curioso es que en Argentina la cantidad de muertos entre 40 y 70 años es muy alta: asciendiendo al 55\% (son 24 personas). Esto es un indicio de que hay mucha más gente infectada en esta franja etárea y no está reportada, ¿por qué podemos decir esto? La proporción de defunciones en Corea del Sur puede darnos una pista. 

## Porcentaje de muertes en Corea por franja etárea 

La siguiente tabla, nos muestra el porcentaje de muertes en Corea del sur por franja etárea:

|<30|30-39|40-49|50-59|60-69|70-80|>80|
|:----:|--|-----|-----|-----|-----|---|
|0  | 0.11  | 0.09  | 0.37  | 1.51 | 5.34 |10.84 |

Esto significa que en Corea murieron el 10.84\% de las personas infectadas mayores a 80 años, o el 5.34\% de los infectados de entre 70 y 80 años, etc. Dado que en Corea del Sur se realizaron 5 cada 1000 habitantes (0.5\%), podemos considerar que estos datos son fiables para estimar incidencias en otros países. 

En el informe del ministerio de salud de la nación Argentina del día de hoy se reportan 1451 casos y 7888 descartes, lo que indica que se hicieron 9339 tests y que el porcentaje de positivos entre los test es del 15.53\% (alrededor de 1 de cada 6 test que se hacen da positivo). Estos datos nos permiten suponer que hay un claro sesgo en el número real de casos: se están haciendo test sólo a casos altamente sospechosos. Además, si nos detenemos en el número de test por habitantes, en Argentina se hicieron 2 test por 10000 habitantes a día de hoy, cuando en Corea fueron 50 por igual número de personas.

La estimación que haremos a continuación tiene un supuesto muy fuerte y es que la tasa de muerte por franja de edad es aproximadamente constante entre países. 


## ¿Cuál es la incidencia real del virus en argentina?

Usando los casos de defunciones a día de hoy y los números de Corea, podemos estimar estos casos: 


|<30|30-39|40-49|50-59|60-69|70-80|>80|
|:----:|--|-----|-----|-----|-----|---|
|0  | 0  | 3333 |2703  | 728 |  225 |74|

(Los números están redondeados)

Lo que da un total de 7063 casos. Sin embargo, estos no son infectados actuales, ¿por qué? la respuesta es muy simple: porque transcurre un tiempo entre que una persona se infecta hasta que se muere, este tiempo está estimado entre 2 y 4 semanas. Supongamos que son 21 días en promedio, es decir que este número puede corresponder a 21 días atrás (15 de marzo aproximadamente). 

La otra clave para saber los enfermos a día de hoy es el tiempo que tarda la enfermedad en duplicarse. Hay algunos trabajos científicos que establecen ese tiempo medio en 6.2 días sin medidas de confinamiento. Dado que en Argentina el confinamiento se aplicó desde hace ya casi 3 semanas, vamos suponer que ese tiempo medio sea 12, es decir que la enfermedad tarda 12 días en duplicarse. Entonces, para saber cuántos enfermos aproximados hay actualmente deberíamos multiplicar 7063 por


<img src="https://render.githubusercontent.com/render/math?math=2^\frac{21}{12}">

Lo que arroja un total de 23757 casos: más que 16 veces más que los casos actualmente reportados! 

Podemos jugar con la fórmula general, 

<img src="https://render.githubusercontent.com/render/math?math=2^\frac{days}{dup}\times7063=CasosActuales">

Dónde days indica el período medio de la enfermedad y dup el tiempo que tarda en duplicarse. 


Supongamos que el tiempo medio que transcurre entre que una persona se infecta y se muere son 14 días, entonces estos números corresponderían a 14 días atrás, y el número de infectados (reemplazandos days por 14 y dup por 12) hoy sería de $15855$ (sí, 10 veces más que los reportados actualmente!). 

Sin embargo, si miramos cuidadosamente los datos reportados como positivos en Argentina, la enfermedad se está duplicando cada 6 días aproximadamente. Es decir, podríamos utilizar perfectamente dup=6.2 reportados por algunos trabajos científicos y estimar los posibles casos a día de hoy usando days=14/21 y dup=6.2, lo que nos da un total de 33785 y 73893 casos respectivamente. 

Es decir, en el escenario más favorable (que la enfermedad se duplique cada 12 días y que el período infeccioso dure sólo 14 días), el número real de casos rondaría los *15000*, en tanto que en el escenario más desfavorable (que la enfermedad se duplique cada 6.2 días y la enfermedad tenga un período de duración de 21 días), el número de casos sería mayor a *70000*. Sin embargo, en base a las evidencias que disponemos, lo más razonable sería suponer un período medio de 14 días y una duplicación de entre 6.2  a 10 días, lo que arroja un total de entre *18639* y *33785* casos. 

Creo que tenemos ciertas evidencias para suponer que en Argentina la circulación comunitaria es un hecho y no sólo se trata de alrededor de 8\% de la población como establece el informe diario del ministerio. Si sólo se hacen test a personas sospechosas o con vinculación directa con viajes al extranjero, es obvio que se van a subestimar los casos de circulación comunitaria. 
