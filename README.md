# Practico 7



-----



Bruno Romero





-----





El	 objetivo	 del	 práctico	 es	 determinar	 si	 un	 grupo	 de	 proteínas	 pertenecientes	 a	 la	
familia	 de	 Glutation	 transferasa,	 evolucionaron	 mediante	 un	 proceso	 divergente	 o	
convergente,	 utilizando	 la	 información	 entregada	 por	 el	 pdb	 que	 está	 asociada	 a	 las	
estructuras	de	estas	proteínas.		
	
  
  
  
  
Instrucciones:	
	
  
  
  
  
1. Busque al menos 5 estructuras de proteínas que pertenezcan a la familia de Glutation.	
2. Descargue los archivos pdb.	
3. Demuestre y discuta brevemente si existe evolución convergente o divergente.






Primeramente, se descrgaron los archivos .pdb de las siguientes proteínas:

1. [1AQW](https://www.rcsb.org/pdb/explore/explore.do?structureId=1AQW)   Homo sapiens. Regula negativamente CDK5.

2. [1EOH](https://www.rcsb.org/pdb/explore/explore.do?structureId=1EOH)   Homo sapiens. Regula negativamente CDK5, previene neurodegeneracion.

3. [1GNW](https://www.rcsb.org/pdb/explore/explore.do?structureId=1GNW)   Arabidopsis thaliana. Se une a auxin, flavonoides endogenos y a camalexina fitoalexina.

4. [1KBN](https://www.rcsb.org/pdb/explore/explore.do?structureId=1KBN)   Homo sapiens. Realiza funciones similares a 1EOH. Es una mutante de la misma.

5. [1MTC](https://www.rcsb.org/pdb/explore/explore.do?structureId=1MTC)   Rattus norvegicus. Relacionada con el proceso de olfato.




NOTA: A pesar de que 1AQW, 1EOH y 1KBN se encuentran en la misma especie y además cumplen una funcion muy similar, sus pesos moleculares libres de moleculas de agua son muy distintos.




> Glutathione S-transferases (GSTs) are detoxification enzymes, found in all aerobic organisms, which catalyse the conjugation of glutathione with a wide range of hydrophobic electrophilic substrates, thereby protecting the cell from serious damage caused by electrophilic compounds.



Luego de cargar cada proteína (.pdb) en VMD, se procedió a curarlas con el comando "chain A and protein". Hecho esto con cada proteina, se procedió a cargarlas nuevamente en VMD y se seleccionó una región especifica en el alineamiento generado en la herramienta Multiseq. Esta region, que al colorear el alineamiento con la orden "sequence identity" poseia la mayor conservacion de aminoacidos identicos, fue la seleccionada (Figura 1). Posteriormente, se centraron las proteinas empleando stamp alignment, con los valores de 6 en scanscore (yo estimaba un alto valor para la identidad de las secuencias en la region seleccionada) y lo demas se dejo en default (Figura 2).




![Alineamientoregion](https://github.com/CapitanFlint/Pr-ctico-7/blob/master/alineamientoooo.png)




__Figura 1.__ Se detalla la region seleccionada en el alineamiento: Residuos 18 al 30 fueron escogidos para realizar el analisis de stamp alignment.




![ChainA](https://github.com/CapitanFlint/Pr-ctico-7/blob/master/alineamientochainA.png)




__Figura 2.__ Alineamiento de las cadenas A empleando stamp alignment: Se detallan las 5 cadenas A de cada proteina centrada y alineada en base a la region seleccionada anteriormente.




Posteriormente, decidi que para tener una mejor comparacion, lo mejor seria ir haciendo combinaciones. En primer lugar, solo deje a las proteinas provenientes de Homo sapiens, obteniendo un resultado esperado: El alineamiento estructural era casi perfecto, cada estructura secundaria encajaba muy bien (Figura 3) y las distancias eran mínimas (Figura X).




![Sinplantaniraton](https://github.com/CapitanFlint/Pr-ctico-7/blob/master/sin%20raton.png)




__Figura 3.__ Alineamiento estructural de las cadenas A de proteinas provenientes de Homo sapiens: En esta figura de eliminaron del alineamiento las cadenas provenientes de A. thaliana y R. norvegicus.



En la Figura 1., en el extremo inferior derecho vemos una secuencia de aminoacidos que no encaja con el resto y que probablemente deberia provenir de A. thaliana. Para comprobarlo elimine a la cadena A de la proteina proveniente de A. thaliana y efectivamente esa secuencia correspondia a ese organismo (Figura 4).




![sinplanta](https://github.com/CapitanFlint/Pr-ctico-7/blob/master/sinplanta.png)




__Figura 4.__ Alineamiento estructural de las cadenas A sin considerar a A. thaliana: Se detalla que la seccion aminoacidica que en la Figura 1 resaltaba del resto aqui se ve omitida.






Luego, teniendo con consideracion de que mi hipotesis era: Como las cadenas de Homo sapiens eran casi identicas, yo esperaria ver mas diferencias en las proteinas provenientes de raton y planta, siendo la de raton mas similar a las de humano(ambos mamiferos). Por esto, decidi calcular el RMSD de las cadenas A de las proteinas, obteniendo resultados interesantes y no esperados (Figura 5).



![RMSD](https://github.com/CapitanFlint/Pr-ctico-7/blob/master/gregeergrggr.png)




__Figura 5.__ Calculo de RMSD para las cadenas A de las proteinas: Se realizo el calculo en base a los residuos 18 al 30, que corresponde a la region del alineamiento estructural. Ademas, el programa utilizo a la proteina de raton como punto de comparacion (RMSD= 0,0).



Hecho el RMSD, me di cuenta de que las cadenas A de raton y planta eran las mas cercanas en cuanto a las distancias atomicas del _backbone_ en comparacion a las de humano. Esto podria significar que



En base a los resultados de RMSD, decidi realizar un alineamiento estructural de las cadenas A de las proteinas de R. norvegicus y A. thaliana (Figura 6).




![plantayraton](https://github.com/CapitanFlint/Pr-ctico-7/blob/master/raton%20y%20planta.png)




__Figura 6.__ Alineamiento estructural entre A. thaliana y R. norvegicus: Se detalla la similitud estructural entre estos dos organismos, comaprtiendo estructuras secundarias y manteniendo baja distancia RMSD.








