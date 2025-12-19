# Tarea 8

## cBioPortal para analizar datos genómicos de cáncer

**Alumna: Ana Ramírez Rivas**

### Parte 1: *Selección del estudio*

1. Ingresa a [https://www.cbioportal.org](https://www.cbioportal.org/).
2. Explora el listado de estudios y selecciona **un tipo de cáncer sólido** (por ejemplo: *Lung adenocarcinoma*, *Pancreatic cancer*, *Breast cancer*, *Colorectal cancer*).
3. El estudio elegido debe tener **al menos 100 pacientes** y **datos genómicos y clínicos disponibles**.

**Completa la siguiente información:**

- **Nombre del estudio:**
  
  Pancreatic Adenocarcinoma (QCMG, Nature 2016).

- **Número total de pacientes:**
  
  456 pacientes.

- **Institución responsable:**
  
  Queensland Centre for Medical Genomics (QCMG), Institute for Molecular Bioscience, The University of Queensland, Australia.

### Parte 2: *Análisis genómico*

1. Ve a la pestaña **Summary** del estudio.
<img width="1331" height="607" alt="Summary global- Tarea 9" src="https://github.com/user-attachments/assets/e5a59c78-2dfc-4e9f-9b76-9ac4a6ca3a4c" />

2. Localiza la tabla **“Mutated Genes”**.

3. Identifica los **5 genes con mayor frecuencia de mutación**.

| #   | Gen    | N° de mutaciones | N° de pacientes (N° de muestras con 1 o más mutaciones) | Frecuencia (%) |
| --- | ------ | ---------------- | ------------------------------------------------------- | -------------- |
| 1   | KRAS   | 348              | 344/383                                                 | 89,8%          |
| 2   | TP53   | 256              | 253/383                                                 | 66,1%          |
| 3   | SMAD4  | 89               | 86/383                                                  | 22,5%          |
| 4   | CDKN2A | 75               | 71/383                                                  | 18,5%          |
| 5   | TTN    | 65               | 56/383                                                  | 14,6%          |

4. Selecciona **uno de esos genes** y filtra las muestras (→ **Select Samples**).  
   Observa cómo cambian los gráficos del resumen.
   
   Gen seleccionado *TP53*.
   
   <img width="1335" height="605" alt="Summary por gen- Tarea 9" src="https://github.com/user-attachments/assets/c0b2e4a7-b6d5-45e5-b07a-30320f193bd6" />
   
   **Responde:**
   
   - ¿Cuántos pacientes presentan esa mutación?
     
     253 pacientes.
   
   - ¿Qué tipo de mutación es más frecuente (missense, nonsense, frameshift)?
     
     Mutaciones missense.
     
    <img width="1279" height="124" alt="Tipo de mutación más frecuente- Tarea 9" src="https://github.com/user-attachments/assets/c53cffd3-f18f-49ee-8d06-083789675662" />
   
   - ¿Qué vías de señalización aparecen alteradas en la pestaña *Pathways*?
     
     * Vía de respuesta al daño al ADN (activada por estrés de replicación del ADN): En esta vía participan los genes ATM (alterado en un 3,7% de las muestras), CHEK2, RPS6KA3 y TP53 (alterado en un 66,1% de las muestras).
     
     * Vía de control de ciclo celular, proliferación y muerte celular: En esta vía participan los genes CDKN2A (alterado en un 18,5% de las muestras), MDM2 (alterado en < 0,5% de las muestras), MDM4 y TP53 (alterado en un 66,1% de las muestras).
     
     * Vía de estrés oncogénico: En esta vía participa el gen TP53 (alterado en un 66,1% de las muestras).
     
     <img width="647" height="352" alt="Vías de señalización alteradas- Tarea 9" src="https://github.com/user-attachments/assets/6f5749dd-bbfd-4e32-9f37-972fcbb4aa50" />

### Parte 3: *Análisis clínico*

1. Entra en la pestaña **Clinical Data**.
   
   <img width="1343" height="528" alt="Panel clinical data - Tarea 9" src="https://github.com/user-attachments/assets/7b651ee3-6bf6-43a5-af4b-8002ed58628c" />

2. Examina las variables demográficas:
   
   ***De acuerdo a los datos en general***
   
   - Distribución por sexo: El sexo masculino posee una mayor cantidad de pacientes afectados (239 muestras --> 52,4%) en relación al sexo femenino (198 muestras --> 43,4%); (NA: 19 muestras --> 4,2%).
   - Distribución por edad: El rango etario en el que se concentra la mayor cantidad de pacientes es de 60 a 80 años.
   - Distribución por raza (si está disponible): La raza más afectada es raza blanca/caucásica (336 muestras --> 73,7%), seguida de raza asiática (18 muestras --> 3,9%), raza negra/africana (6 muestras --> 1,3%), otras (3 muestras --> 0,6%); (NA: 93 muestra --> 20,4%).

3. Calcula:
   
   - **Rango de edad (edad máxima − edad mínima):** 90 - 33 años.
   
   - **Mediana de edad (usando “Compare Groups → Median”):** 67 años.

4. **Interpreta los resultados:**
   
   - ¿Existe una predominancia por sexo o edad?
     
     Existe predominancia tanto por sexo como por edad; los hombres se ven más afectados que las mujeres,  en relación a la edad, la mayoría de los casos se concentran en la población de adultos mayores, personas mayores a 60 años pero menores a 90 años.
   
   - ¿Qué implicancias podría tener esa distribución para el estudio del cáncer elegido?
     
     Los adultos mayores, especialmente aquellos de sexo masculino, son más propensos a sufrir adenocarcinoma pancreático.

### Parte 4: *Análisis interpretativo*

Redacta un breve comentario (5–10 líneas) respondiendo:

* ¿Qué relación observas entre las mutaciones más frecuentes y las características clínicas del grupo?.

* ¿Por qué podría ser relevante este gen como biomarcador o diana terapéutica?.

La mayoría de las mutaciones se concentran en genes asociados con el control de la proliferación y muerte celular (KRAS, TP53, SMD4, CDKN2A) por lo que se espera que el cáncer sea de rápida progresión y diseminación, no obstante, la mayor cantidad de muestras son de tumores primarios pobre o medianamente diferenciados, recolectados en pacientes que se encuentran mayormente en estadíos tempranos de la enfermedad (IIA-IIB); esta discordancia probablemente se debe a los métodos de pesquisa y diagnóstico temprano implementados en los países involucrados en el estudio, más que por los genes mutados presentes. Es coherente la edad media de diagnóstico de este cáncer debido a que a medida que aumenta la edad del paciente, aumenta el n° de mutaciones acumuladas durante la replicación del ADN, lo que hace más propensos a los adultos mayores a sufrir neoplasias.

El gen TP53 mutado es el supresor de tumores que se encuentra con mayor frecuencia en muchos tipos de cáncer, por lo que puede servir para predecir riesgo, pronóstico y respuesta a tratamiento; también, como participa en varias vías de señalización clave, puede servir como diana terapéutica en caso de fracaso de otros tratamientos dirigidos.


