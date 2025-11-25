# Tarea 10.1

## Tarea del tutorial 1

### Filtro y alineamiento de lecturas

1. Realizar el alineamiento contra el genoma humano hg19 de las lecturas R1 y R2 del paciente seleccionado para la tarea de control de calidad de lecturas de secuencia.
   
   *Muestra*: S12
   
   Se utilizó el siguiente comando para el alineamiento de las lecturas contra el genoma de referencia: 
   
   `module load bwa`
   
   Para cargar el módulo correspondiente a BWA (Burrows-Wheeler Aligner -->  paquete de programas para mapear secuencias de ADN contra un gran genoma de referencia) en el environment. 
   
   Luego el comando en el que se especifica el genoma de referencia y las lecturas en estudio:
   
   ```
   bwa mem -t 4 -M /datos/reference/genomes/hg19_reference/hg19.fasta \
   S12_R1_filter3.fastq.gz \
   S12_R2_filter3.fastq.gz \
   > S12.sam
   ```

2. Utilizando una línea de comando, encuentre la primera lectura en el archivo SAM que contenga bases enmascaradas (secuencias suavizadas por soft-clipping).
   
   Se utilizó el comando: 
   
   `awk '$6 ~ /S/ && $1 !~ /^@/ {print; exit}' S12.sam`
   
   * `awk`: es una herramienta que sirve para procesar, filtrar y transformar texto estructurado, como lo son los archivos SAM o BAM.
   
   * `$6 ~ /S/`: para buscar en la columna 6 (CIGAR) si contiene la letra **S**.
   
   * `$1 !~ /^@/`: para evitar las líneas de encabezado.
   
   * `print`: para imprimr la primera lectura que contenga bases enmascardas. 
   
   * `exit`: para detener la acción de la función de `awk` luego de encontrar la primera lectura.

3. Muestre el registro de la lecturas en el archivo SAM e identifique y explique el código CIGAR de esa lectura.
   
   El código CIGAR es una sección que describe cómo una lectura se alinea a la secuencia de referencia en un archivo SAM o BAM. Cada letra tiene un significado.
   
   ![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-19-13-44-46-image.png)
   
   Secciones:
   
   * `M03564:2:000000000-D29D3:1:1101:11927:2145`: ID de la lectura.
   
   * `99`: Indica que la lectura fue correctamente mapeada.
   
   * `chr19`: Referencia, donde esta la secuencia leída.
   
   * `13049460`: Posición de la secuencia en el cromosoma, en este caso el 19.
   
   * `60`: Valor de MAPQ (calidad del alineamiento); el valor obtenido indica que el alineamiento es confiable.
   
   * `226M25S`: Código CIGAR. El 226M se refiere a que hay 226 bases alineadas (match/mismatch); el 25S se refiere a que hay 25 bases soft-clipped, es decir, las bases están presentes en la secuencia, pero no se alinearon, por lo que el aligner no las borra sino que las deja al inicio o al final de la secuencia. En este caso las bases soft-clipped estan al final.

4. Generar un reporte técnico de calidad del alineamiento con *qualimap*.

5. Seleccionar 4 figuras que a su juicio sean las más informativas sobre la calidad de los datos y del ensamble.

6. Incluir las figuras en la sección de Resultados de un reporte técnico. Describir cada figura con una leyenda descriptiva. Adicionalmente, en el texto de la sección, interpretar los resultados y citar cada figura. Debe referirse a la calidad de los datos y del alineamiento. Enfóquese especialmente en los posibles problemas con los datos o alineamientos. Comente potenciales razones que expliquen lo observado. Incluya una sección con las principales *Conclusiones* para la muestra.

7. Incluya el reporte completo generado con *qualimap* como anexo.

8. Comparta el informe en formato markdown a través de github para dar por completada esta tarea.

#### Reporte:

***Resultados***

Se realizó el alineamiento de las lecturas R1 y R2 de la muestra de un paciente (S12) con el genoma humano de referencia (hg19). Se realizaron 48.634 lecturas, de las cuales 48.603 (99,94%) fueron mapeadas y 31 (0,06%) quedaron sin mapear; de estas, 439 (0,9%) lecturas fueron enmascaradas, lo cual se puede apreciar mejor en el gráfico de la **figura 3**, esto sugiere buena calidad de secuenciación, buen trimming previo (en el caso que se haya realizado este proceso) y un alineamiento limpio y sin colas de adaptadores. 

En promedio, la cobertura de la secuenciación fue del 82,5, tal como se observa en el gráfico superior de la **figura 1**, allí se observa una cobertura variada, en la que la mayoría de las secuencias tienen una baja cobertura, esto podría indicar que el panel tiene mala eficiencia en ciertos amplicones. 

En relación al contenido ACTG, resultó en:

* A: 25,58%.

* C: 26,18%.

* T: 22,5%.

* G: 25,73%.

* G-C: 51,92%. Esto se observa en el gráfico inferior de la **figura 1**, se ve que hay regiones con bajo contenido G-C (con alrededor del 30-35%) y regiones con alto contenido G-C (con alrededor del 60-65%), este contenido irregular a lo largo de la lectura coincide con lo reflejado en el gráfico superior de esa figura, es decir, con el panel de cobertura irregular.

Se obtuvo un tamaño del inserto de, en promedio 251, 7pb; esto se puede ver de mejor manera en el gráfico de la **figura 2**. Se sabe que usualmente, en las librerías típicas de Illumina, el tamaño del inserto puede estar entre 150–350pb, dependiendo del protocolo del ensayo, es por esto que se considera que el tamaño de los fragmentos es estable, lo que implica que la librería esta bien hecha y no fue degradada y que no hay fragmentación excesiva.

De las lecturas mapeadas, al menos una es una inserción en un 1.47%, al menos una es una deleción en un 2.32%, y al menos una es un homopolymer indels (tipo de error que ocurre en regiones del ADN donde hay secuencias con muchas repeticiones consecutivas del mismo nucleótido, lo que hace que en la secuenciación y alineamiento existan dificultades para determinar con precisión cuántas bases hay realmente) en un 58.96%.

Finalmente, en cuanto a la calidad del mapeo, tal como se observa en la **figura 4**, en promedio esta es de 58.8, lo que indica aunque las lecturas mapeadas están dispersas en posiciones puntuales del genoma (en regiones de interés), todas ellas tienen buena calidad de mapeo; no hay evidencia de problemas de alineamiento, ni lecturas ambiguas.

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-21-06-56-08-genome_coverage_across_reference.png)

***Figura 1:*** *Coverage across reference* 
El gráfico se encuentra dividido en 2 paneles. El panel superior corresponde al panel de *Cobertura (X)*, en el eje Y se representa la cobertura de la secuenciación y en el eje X la posición según pares de bases; en este se observa un rango de cobertura heterogéneo, la mayoría de las secuencias tienen una cobertura baja, que va entre 0-60X aproximadamente, una minoría de las secuencias tienen una cobertura baja-media, que va entre 100-125X, finalmente, se observa un pico aislado en el que la cobertura supera los 600X. El panel inferior corresponde al *Contenido de G-C por posición (%)*  en el que los peaks (líneas de color negro) indican porcentaje G-C del fragmento asociado a cada punto de cobertura y las líneas rojas punteadas indican el promedio G-C del conjunto de regiones; en este se observan regiones con un contenido G-C bajo, de aproximadamente 30-35%, y regiones con alto contenido G-C más alto, de aproximadamente 60-65%.



![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-21-07-02-49-genome_insert_size_across_reference.png)

***Figura 2***: *Insert Size Across Reference*

El gráfico muestra el tamaño del inserto, es decir, la distancia entre el inicio del fragmento forward y el fin del fragmento reverse en un par de lecturas paired-end. Las líneas verdes corresponden a una región dentro del archivo BED, Las regiones aparecen distribuidas por el genoma, solo en las regiones en estudio; se observa que la mayoría de los insert size van desde las 240pb a las 265pb, aunque hay una que supera los 320pb. 



![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-21-07-07-08-genome_reads_clipping_profile.png)

***Figura 3***: *Mapped Reads Clipping Profile*

En este gráfico se analiza el porcentaje de bases que está siendo enmascarado (recortado) en cada posición a lo largo de las lecturas mapeadas. En el eje X se representa la posición dentro del read, que va de 0 a 260 pb; en el eje Y se muestra el porcentaje de bases a las que se les realizó clipping, que va de 0 a 100%. Se observa que en la mayor parte del read, hasta 225pb aproximadamente, el clipping es bajo, al pasar esa posición, el porcentaje de clipping aumenta levemente.



![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-21-06-58-54-genome_mapping_quality_across_reference.png)

***Figura 4***: *Mapping Quality Across Reference*

En el gráfico se representa la calidad de mapeo de las lecturas alineadas a lo largo del genoma de referencia.
Las líneas rojas verticales corresponden a una lectura o grupo de lecturas; en el eje X se representa la posición (pb) de la lectura; en el eje Y se representa la calidad del mapeo. Se observa que la mayoría de las regiones mapeadas tienen una calidad de 60.

***Conclusiones***

Se tiene un archivo de cobertura de secuenciación variable, en la que la mayor parte de la secuencias tiene baja cobertura, esto podría indicar que el panel tiene mala eficiencia en ciertos amplicones o es producto de un mal diseño de la libreria, sin embargo, por el tamaño del inserto, se demuestra que la libreria esta bien construida y no esta degradada; respecto al contenido irregular de G-C (en algunas secciones bajo contenido y en otras alto) es consistente con la cobertura variable de la secuenciación.

Pese a lo anterior, el porcentaje de secuencias enmascaradas (que se producen cuando hay problemas en los extremos de las lecturas o por contaminación por adaptadores) es bajo y la calidad del mapeo es aceptable.

# 
