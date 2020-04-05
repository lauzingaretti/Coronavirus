### El Delfos del Siglo XXI y la epidemia del coronavirus: ¿qué sabemos ahora mismo?
Este es un repositorio dónde pondré algunos análisis de los datos de coronavirus. 
Los datos que utilizo fueron descargados desde el siguiente enlace: 

https://github.com/CSSEGISandData/COVID-19. 

Los análisis están disponibles en https://lauzingaretti.github.io/Coronavirus/ 

### Modelo logístico para modelar la evolución de COVID19 

Los siguientes scripts de python contienen un sencillo modelo logístico que permiten modelar aproximadamente la evolución del coronavirus. El script se puede ejecutar para cualquier país con sólo cambiar el código de país. Las varianzas estimadas son muy grandes porque es un proceso de gran incertidumbre. Estos números sólo son orientativos, hay que tener en cuenta que si los datos son sesgados, los modelos no son buenos.  
En el caso argentino, por ejemplo, se estiman muy pocos casos de covid19 y el número de casos finales está posiblemmente muy subestimado. Sin embargo, se notan las medidas de confinamiento aplicadas en un estadío muy temprano. 
El caso Chino es conocido por todos, sin embargo -y a la luz de los datos de otros países- podríamos pensar que no son datos fiables. 

- [1. Estimación de la evolución de casos en Argentina](https://github.com/lauzingaretti/Coronavirus/blob/master/inst/md/Argentina_pred.md)
- [2. Estimación de la evolución de casos en España](https://github.com/lauzingaretti/Coronavirus/blob/master/inst/md/Spain_pred.md)
- [3. Estimación de la evolución de casos en USA](https://github.com/lauzingaretti/Coronavirus/blob/master/inst/md/USA.md)
- [4. Estimación de la evolución de casos en China](https://github.com/lauzingaretti/Coronavirus/blob/master/inst/md/China.md)

El siguiente enlace contiene un pequeño informe que nos ayuda a pensar sobre el número total de casos de Covid-19 en Argentina a día de hoy.

- [5. Estimación de los casos no reportados de covid-19 en Argentina]
(https://github.com/lauzingaretti/Coronavirus/blob/master/inst/md/covid19casosestimados.md)





