# Tarea 6

## Genética de poblaciones 2

### Proyecto 1

***Do all present-day populations from Europe display the same 3-way admixture?*** 

Poblaciones involucradas:

- Mbuti.DG: Población Africana moderna.

- Basque.DG: Población Francesa moderna (WE).

- GBR.DG: Población de Reino Unido moderna (NE).

- Italy_Broion_CA.SG: Población Italiana antigua (SE).

- Luxembourg_Mesolithic.DG: Población de Luxemburgo antigua.

- Russia_Samara_EBA_Yamnaya.AG (EE): Población Rusa antigua.

- Turkey_Marmara_Barcin_N.AG: Población Turca antigua.

<u>*Estadístico Outgroup-F3*: Resultado </u>

<img width="582" height="213" alt="Tabla 1 (f3), Tarea 6" src="https://github.com/user-attachments/assets/3ba8ce12-3c31-4783-bd14-30388093b30a" />


**Interpretación:**

Medición de cuánta deriva genética comparten las poblaciones del target (A) y las poblaciones del source (B) desde que se separaron del outgroup.

* pop1: outgroup.

* pop2: población objetivo de estudio.

* pop3: población con la cual se compara el target.

Valor del estadístico: En este caso el valor del estadístico, para todas las comparaciones, es positivo y cercano a cero, lo que indica que las poblaciones objetivo no muestran evidencia de mezcla reciente al compararlas con las poblaciones del source.

Valor de Z: En este caso en todas las comparaciones el valor de Z es mayor a 3, lo que indica evento significativo estadísticamente.

**Conclusión:**

Los resultados evidencian una diferenciación clara de las poblaciones respecto a la población outgroup Mbuti.DG.

Las poblaciones (pares) con mayor valor de F3 (0,075) son aquellas con más deriva compartida:

* Tanto la población Basque.DG como la población GBR.DG comparte más ascendencia con la población Luxembourg_Mesolithic.DG.

* La población Italy_Broion_CA.SG, a diferencia de las anteriores, comparte más ascendencia con la población Turkey_Marmara_Barcin_N.AG.

Las poblaciones (pares) con menor valor de F3 (0,069) son aquellas con menos deriva compartida:

* La población Italy_Broion_CA.SG comparte menos ascendencia con la población Russia_Samara_EBA_Yamnaya.AG.

<u>*Estadístico F4*: Resultados</u>

<img width="704" height="43" alt="Tabla 2 (f4), Tarea 6" src="https://github.com/user-attachments/assets/6ff7c90a-c167-4e1b-83b5-cafdf3ce93e5" />


**Interpretación:**

Medida eficaz para distinguir la introgresión de la clasificación incompleta de linajes, basándose en las frecuencias alélicas de 4 poblaciones. Con las poblaciones A, B, C y D, asumiendo (A,B),(C,D), el estadístico se calcula como (frA -frB) x (frC-frD), donde fr son frecuencias alélicas.

- pop1: Población con la cual se compara el target.

- pop2: Población con la cual se compara el target.

- pop3: Población de interés.

- pop4: outgroup.

Valor del estadístico: En este caso el valor del estadístico es positivo, lo que indica que la población A comparte más deriva genética con C.

Valor de Z: En este caso en todas las comparaciones el valor de Z es mayor a 3, lo que indica evento significativo estadísticamente.

**Conclusión:** 

La población Basque.DG comparte más deriva genética con la población Turkey_Marmara_Barcin_N.AG que con la población Russia_Samara_EBA_Yamnaya.AG.

<u>*qp-wave*: Resultado</u>

<img width="714" height="455" alt="Tabla 3 (qp-wave), Tarea 6" src="https://github.com/user-attachments/assets/054861a4-4fba-4a48-b4a0-b342c825d5de" />

<img width="508" height="132" alt="Tabla 3 (qp-wave continuación), Tarea 6" src="https://github.com/user-attachments/assets/f13aa0db-1e42-4f59-a97c-fbafd0c3ff46" />


**Interpretación:**

Estimar el número mínimo de eventos de mezcla en una(s) población objetivo; en este tipo de prueba se intengran múltiples *f2, f3 y f4* de las poblaciones analizadas.

*Primera tabla*

Estadístico f4:

* pop1: Población target.

* pop2: Poblaciones de posible fuente de mestizaje.

* pop3: Right 1 (outgroup).

* pop4: Right 2 (outgroup).

*Segunda tabla*

f4rank: Corresponde al número de flujos génicos que se estan probando.

Valor de p: El valor de p debe ser mayor a 0,05 para aceptar la hipótesis nula (H0: son suficientes el mínimo de flujos génicos ocurridos). 

**Conclusión:**

De acuerdo al valor de p (0,966), son suficientes 3 flujos génicos para explicar la variación genética de las poblaciones testeadas. 

<u>*qp-Adm*: Resultado</u>

<img width="809" height="553" alt="Tabla 4 (qp-Adm1), Tarea 6" src="https://github.com/user-attachments/assets/eb742b0f-e6f9-426f-a51f-534e43431741" />

<img width="804" height="529" alt="Tabla 4 (qp-Adm2), Tarea 6" src="https://github.com/user-attachments/assets/dc2f70d4-cffd-486b-8a1e-6e7df7910965" />

<img width="807" height="212" alt="Tabla 4 (qp-Adm3), Tarea 6" src="https://github.com/user-attachments/assets/cede9b04-0903-4d72-ab5e-63294bc998f2" />

<img width="489" height="70" alt="Tabla 4 (qp-Adm continuación), Tarea 6" src="https://github.com/user-attachments/assets/7e513b89-ba2d-4c21-b49c-c3dbd66b902c" />

<img width="1006" height="91" alt="Tabla 4 (qp-Adm continuación 2), Tarea 6" src="https://github.com/user-attachments/assets/6a747185-81e2-4597-8be8-d6bc843378d3" />

<img width="436" height="73" alt="Tabla 4 (qp-Adm continuación 3), Tarea 6" src="https://github.com/user-attachments/assets/fb5ae44f-7a9d-4bad-8e96-1de6cfb3ad9b" />

**Interpretación:**

Estimar la proporción de mestizaje de cada fuente; en este tipo de prueba también se intengran múltiples *f2, f3 y f4* de las poblaciones analizadas. 

Una vez establecido un número de flujos migratorios (en el qp-wave) en las poblaciones testeadas, en esta etapa (qp-Adm) se busca evaluar la contribución de dichos flujos al target.

*Primera tabla*

Estadístico f4:

- pop1: Población target.

- pop2: Poblaciones de posible fuente de mestizaje.

- pop3: Right 1 (outgroup).

- pop4: Right 2 (outgroup).

*Segunda tabla*

f4rank: Corresponde al número de flujos génicos que se estan probando.

Valor de p: El valor de p debe ser mayor a 0,05 para aceptar la hipótesis nula (H0: son suficientes el mínimo de flujos génicos ocurridos).

*Tercera tabla*

Modelo 00: Se estan utilizando las 2 poblaciones como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

Modelo 01: Se esta utilizando el modelo con la 1era población como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

Modelo 10: Se esta utilizando el modelo con la ultima población como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

*Cuarta tabla*

Weight: Muestra para las poblaciones target y las poblaciones potenciales fuentes, cual es la contribución en términos de ancestría; sus valores deberían sumar 1.

**Conclusión**

El 44,4% de la contribución de flujo génico para la población Basque.DG viene dada por la población Turkey_Marmara_Barcin_N.AG y el 55,6% viene dada por Russia_Samara_EBA_Yamnaya.AG, y este modelo es posible (TRUE). Esto es un poco contradictorio a lo señalado en el f4, en el que se establecía que el mayor flujo génico para Basque.DG venía dado por Turkey_Marmara_Barcin_N.AG.

### Proyecto 2

***Steppe formation model***

Poblaciones involucradas:

- Mbuti.DG: Población Africana moderna.

*Estadístico Outgroup-F3*: Resultado

<img width="619" height="149" alt="Tabla 1 P2 (f3), Tarea 6" src="https://github.com/user-attachments/assets/74a157fd-dcd6-4c35-8173-367332c276ca" />

**Interpretación:**

Medición de cuánta deriva genética comparten las poblaciones del target (A) y las poblaciones del source (B) desde que se separaron del outgroup.

- pop1: outgroup.

- pop2: población objetivo de estudio.

- pop3: población con la cual se compara el target.

Valor del estadístico: En este caso el valor del estadístico, para todas las comparaciones, es positivo y cercano a cero, lo que indica que las poblaciones objetivo no muestran evidencia de mezcla reciente al compararlas con las poblaciones del source.

Valor de Z: En este caso en todas las comparaciones el valor de Z es mayor a 3, lo que indica evento significativo estadísticamente.

**Conclusión:**

Los resultados evidencian una diferenciación clara de las poblaciones respecto a la población outgroup Mbuti.DG.

Las poblaciones (pares) con mayor valor de F3 (0,075) son aquellas con más deriva compartida:

- La población Russia_LBA_Srubnaya_Alakul.SG,  comparte más ascendencia con la población Russia_Sidelkino_HG.SG.

Las poblaciones (pares) con menor valor de F3 (0,067) son aquellas con menos deriva compartida:

- La población Kazakhstan_Maitan_MLBA_Alakul.AG, Russia_LBA_Srubnaya_Alakul.SG y Russia_Sidelkino_HG.SG comparten menos ascendencia con la población Iran_GanjDareh_N.AG.

*Estadístico F4*: Resultados

<img width="751" height="53" alt="Tabla 2 P2 (f4), Tarea 6" src="https://github.com/user-attachments/assets/3028afd8-0881-4ecc-859c-0ab0bb88ba6e" />

**Interpretación:**

Medida eficaz para distinguir la introgresión de la clasificación incompleta de linajes, basándose en las frecuencias alélicas de 4 poblaciones. Con las poblaciones A, B, C y D, asumiendo (A,B),(C,D), el estadístico se calcula como (frA -frB) x (frC-frD), donde fr son frecuencias alélicas.

- pop1: Población de source1.

- pop2: Población de source1.

- pop3: Población de interés.

- pop4: outgroup.

Valor del estadístico: En este caso el valor del estadístico es negativo, lo que indica que la población B comparte más deriva genética con C.

Valor de Z: En este caso en todas las comparaciones el valor de Z (valor absoluto) es mayor a 3, lo que indica evento significativo estadísticamente.

**Conclusión:**

La población Kazakhstan_Maitan_MLBA_Alakul.AG comparte más deriva genética con la población Russia_Sidelkino_HG.SG que con la población Iran_GanjDareh_N.AG.

*qp-wave*: Resultado

![](C:\Users\cosit\Pictures\Tabla%203%20P2%20(qp-wave),%20Tarea%206.png)

![](C:\Users\cosit\Pictures\Tabla%203%20P2%20(qp-wave%20continuación),%20Tarea%206.png)

**Interpretación:**

Estimar el número mínimo de eventos de mezcla en una(s) población objetivo; en este tipo de prueba se intengran múltiples *f2, f3 y f4* de las poblaciones analizadas.

*Primera tabla*

Estadístico f4:

- pop1: Población target.

- pop2: Poblaciones de posible fuente de mestizaje.

- pop3: Right 1 (outgroup).

- pop4: Right 2 (outgroup).

*Segunda tabla*

f4rank: Corresponde al número de flujos génicos que se estan probando.

Valor de p: El valor de p debe ser mayor a 0,05 para aceptar la hipótesis nula (H0: son suficientes el mínimo de flujos génicos ocurridos).

**Conclusión:**

De acuerdo al valor de p (0,599), son suficientes 2 flujos génicos para explicar la variación genética de las poblaciones testeadas.

*qp-Adm*:Resultado

![](C:\Users\cosit\Pictures\Tabla%204%20P2%20(qp-Adm%204),%20Tarea%206.png)

![](C:\Users\cosit\Pictures\Tabla%204%20P2%20(qp-Adm%204%20continuación),%20Tarea%206.png)

![](C:\Users\cosit\Pictures\Tabla%204%20P2%20(qp-Adm%204%20continuación%202),%20Tarea%206.png)

![](C:\Users\cosit\Pictures\Tabla%204%20P2%20(qp-Adm1),%20Tarea%206.png)

![](C:\Users\cosit\Pictures\Tabla%204%20P2%20(qp-Adm2),%20Tarea%206.png)

![](C:\Users\cosit\Pictures\Tabla%204%20P2%20(qp-Adm3),%20Tarea%206.png)

**Interpretación:**

Estimar la proporción de mestizaje de cada fuente; en este tipo de prueba también se intengran múltiples *f2, f3 y f4* de las poblaciones analizadas.

Una vez establecido un número de flujos migratorios (en el qp-wave) en las poblaciones testeadas, en esta etapa (qp-Adm) se busca evaluar la contribución de dichos flujos al target.

*Primera tabla*

Estadístico f4:

- pop1: Población target.

- pop2: Poblaciones de posible fuente de mestizaje.

- pop3: Right 1 (outgroup).

- pop4: Right 2 (outgroup).

*Segunda tabla*

f4rank: Corresponde al número de flujos génicos que se estan probando.

Valor de p: El valor de p debe ser mayor a 0,05 para aceptar la hipótesis nula (H0: son suficientes el mínimo de flujos génicos ocurridos).

*Tercera tabla*

Modelo 00: Se estan utilizando las 2 poblaciones como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

Modelo 01: Se esta utilizando el modelo con la 1era población como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

Modelo 10: Se esta utilizando el modelo con la ultima población como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

*Cuarta tabla*

Weight: Muestra para las poblaciones target y las poblaciones potenciales fuentes, cual es la contribución en términos de ancestría; sus valores deberían sumar 1.

**Conclusión**

El 30,6% de la contribución de flujo génico para la población Russia_MLBA_Sintashta.AG viene dada por la población Iran_GanjDareh_N.AG y el 69,4% viene dada por Russia_Sidelkino_HG.SG, y este modelo es posible (TRUE). 

### Proyecto 4

***Medieval / Iberian admixture***

Poblaciones involucradas:

- Mbuti.DG: Población Africana moderna.

<u>*Estadístico Outgroup-F3*: Resultado</u>

<img width="626" height="345" alt="Tabla 1 P4 (f3), Tarea 6" src="https://github.com/user-attachments/assets/70e1d1c0-4c11-4dc2-b83f-3bd45feaba5a" />

**Interpretación:**

Medición de cuánta deriva genética comparten las poblaciones del target (A) y las poblaciones del source (B) desde que se separaron del outgroup.

- pop1: outgroup.

- pop2: población objetivo de estudio.

- pop3: población con la cual se compara el target.

Valor del estadístico: En este caso el valor del estadístico, para todas las comparaciones, es positivo y cercano a cero, lo que indica que las poblaciones objetivo no muestran evidencia de mezcla reciente al compararlas con las poblaciones del source.

Valor de Z: En este caso en todas las comparaciones el valor de Z es mayor a 3, lo que indica evento significativo estadísticamente.

**Conclusión:**

Los resultados evidencian una diferenciación clara de las poblaciones respecto a la población outgroup Mbuti.DG.

Las poblaciones (pares) con mayor valor de F3 (0,11) son aquellas con más deriva compartida:

- La población Spain_Islamic.AG, Spain_Islamic_Zira.AG, Spain_Medieval.AG, Spain_NazariPeriod_Muslim.AG y Spain_Visigoth_Granada.AG comparten más ascendencia con la población Spain_MLN.AG.

Las poblaciones (pares) con menor valor de F3 (0,076) son aquellas con menos deriva compartida:

- La población Spain_Islamic.AG, Spain_Islamic_Zira.AG, Spain_Medieval.AG, Spain_NazariPeriod_Muslim.AG y Spain_Visigoth_Granada.AG comparten menos ascendencia con la población Yoruba.DG.

<u>*Estadístico F4*: Resultados</u>

<img width="694" height="55" alt="Tabla 2 P4 (f4), Tarea 6" src="https://github.com/user-attachments/assets/ffefd191-206e-4b1e-abc6-8b0a42d1b155" />


**Interpretación:**

Medida eficaz para distinguir la introgresión de la clasificación incompleta de linajes, basándose en las frecuencias alélicas de 4 poblaciones. Con las poblaciones A, B, C y D, asumiendo (A,B),(C,D), el estadístico se calcula como (frA -frB) x (frC-frD), donde fr son frecuencias alélicas.

Valor del estadístico: En este caso el valor del estadístico es negativo, lo que indica que la población B comparte más deriva genética con C.

Valor de Z: En este caso en todas las comparaciones el valor de Z (valor absoluto) es mayor a 3, lo que indica evento significativo estadísticamente.

**Conclusión:**

La población Spain_NazariPeriod_Muslim.AG comparte más deriva genética con la población Spain_Medieval.AG que con la población Spain_Islamic.AG.

*qp-wave*: Resultado

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-14-50-58-image.png)

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-14-51-22-image.png)

**Interpretación:**

Estimar el número mínimo de eventos de mezcla en una(s) población objetivo; en este tipo de prueba se intengran múltiples *f2, f3 y f4* de las poblaciones analizadas.

*Primera tabla*

Estadístico f4:

- pop1: Población target.

- pop2: Poblaciones de posible fuente de mestizaje.

- pop3: Right 1 (outgroup).

- pop4: Right 2 (outgroup).

*Segunda tabla*

f4rank: Corresponde al número de flujos génicos que se estan probando.

Valor de p: El valor de p debe ser mayor a 0,05 para aceptar la hipótesis nula (H0: son suficientes el mínimo de flujos génicos ocurridos).

**Conclusión:**

De acuerdo al valor de p (< 0,05), se rechaza la hipótesis nula, hacen falta más de 2 flujos génicos para explicar la variación genética de las poblaciones testeadas.

*qp-Adm*:Resultado

![](C:\Users\cosit\Pictures\Tabla%204%20P4%20(qp-Adm%204),%20Tarea%206.png)

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-15-20-54-image.png)

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-15-21-16-image.png)

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-15-22-17-image.png)

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-15-32-07-image.png)

![](C:\Users\cosit\Pictures\Tabla%204%20P4%20(qp-Adm2),%20Tarea%206.png)

![](C:\Users\cosit\AppData\Roaming\marktext\images\2025-11-07-15-30-32-image.png)

**Interpretación:**

Estimar la proporción de mestizaje de cada fuente; en este tipo de prueba también se intengran múltiples *f2, f3 y f4* de las poblaciones analizadas.

Una vez establecido un número de flujos migratorios (en el qp-wave) en las poblaciones testeadas, en esta etapa (qp-Adm) se busca evaluar la contribución de dichos flujos al target.

*Primera tabla*

Estadístico f4:

- pop1: Población target.

- pop2: Poblaciones de posible fuente de mestizaje.

- pop3: Right 1 (outgroup).

- pop4: Right 2 (outgroup).

*Segunda tabla*

f4rank: Corresponde al número de flujos génicos que se estan probando.

Valor de p: El valor de p debe ser mayor a 0,05 para aceptar la hipótesis nula (H0: son suficientes el mínimo de flujos génicos ocurridos).

*Tercera tabla*

Modelo 00: Se estan utilizando las 2 poblaciones como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

Modelo 01: Se esta utilizando el modelo con la 1era población como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

Modelo 10: Se esta utilizando el modelo con la ultima población como fuente; entrega información del weight (contribución en términos de ancestría), si el modelo es o no posible (TRUE/FALSE).

*Cuarta tabla*

Weight: Muestra para las poblaciones target y las poblaciones potenciales fuentes, cual es la contribución en términos de ancestría; sus valores deberían sumar 1.

**Conclusión**

El 91,9% de la contribución de flujo génico para la población Spain_Islamic.AG viene dada por la población Spain_MLN.AG y el 8,1% viene dada por Morocco_EN.WGC.SG, y este modelo es posible (TRUE).


