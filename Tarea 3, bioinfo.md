# Tarea 3

## Manejo de R y Rstudio

### Ejercicio 1

Crear una variable con el logaritmo base 10 de 50 y sumarlo a otra variable cuyo valor sea igual a 5.

```
a <- log10(50)
b <- 5
a+b
```

<img width="835" height="160" alt="Ejercicio 1, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/62eae647-328f-4df5-a36e-8b9d75e9e251" />


### Ejercicio 2

a) Sumar el número 2 a todos los números entre 1 y 150.

* Crear el vector: 
  
  `vec.a <- 1:150`

* Crear variable para número a sumar:
  
  `num.sum <- 2`

* Para obtener el resultado, crear variable resultado donde se sume el vector y el número a sumar:
  
  `resultado <- vec.a + num.sum`

* Correr el resultado:
  
  `resultado`
  
<img width="797" height="274" alt="Ejercicio 2 a, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/d9feb1dc-7bba-4c4b-ae30-696a324f1deb" />


b) ¿Cuántos números son mayores a 20 en el vector -13432:234?

* Crear vector:
  
  `vec.b <- -13432:234`

* Preguntar a R sobre los números del vector mayores a 20:
  
  `vec.b[vec.b>20]`

* Pedirle a R que sume la cantidad de números del vector mayores a 20, para responder la pregunta:

* `sum(vec.b>20)`
  
<img width="1333" height="238" alt="Ejercicio 2 b, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/eda6cf80-526b-4bc6-bb1c-7b8292dfdf52" />


### Ejercicio 3

Carga en R el archivo `PracUni1Ses3/maices/meta/maizteocintle_SNP50k_meta_extended.txt` y ponlo en un objeto de R llamado meta_maiz.

* Cargar librerias:
  
  ```library(readr)
  library(rstatix)```
  ```

* Configurar R con el directorio de trabajo (aquel donde se encuentra el archivo descargado):
  
  `Session > Set Working Directory > Choose directory`

* Utilizar la función `read.delim` para abrir el archivo; colocarlo en un objeto de R llamado meta_maiz:

* ```
  meta_maiz <- read.delim("Maiz_U1S3.txt")
  meta_maiz
  ```
  
<img width="989" height="116" alt="Ejercicio 3, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/4af2ce12-82aa-4ead-97f4-a479bf2d7203" />


### Ejercicio 4

a) Escribe un for loop para que divida 35 entre 1:10 e imprima el resultado en la consola.

`for (i in 1:10) {print (paste (35/i))}`

<img width="177" height="146" alt="Ejercicio 4a, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/c3fd0cd2-f105-4753-af5e-3d08b0e83ff7" />


b) Modifica el loop anterior para que haga las divisiones solo para los números nones (con un comando, NO con `c(1,3,...)`). Pista: `next`.

* Crear un vector que contenga los números a evitar (impares):
  
  `none <- c(1, 3, 5, 7, 9)`

* Incluirlo en el comando al igual que la función `next`, la cual sirve como indicación para saltarse dichos números en la operación:

* ```
  for (i in 1:10) {
    if (i %in% none){
      next
    }
    print(paste(35/i))
  }
  ```
  
<img width="165" height="78" alt="Ejercicio 4b, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/2f665d21-c376-4af6-9455-ec017a841ddd" />


c) Modifica el loop anterior para que los resultados de correr todo el loop se guarden en una df de dos columnas, la primera debe tener el texto "resultado para x" (donde x es cada uno de los elementos del loop) y la segunda el resultado correspondiente a cada elemento del loop. Pista: el primer paso es crear un vector *fuera* del loop. 

* Crear un `data.frame` vacío:
  
  `df <- data.frame(resulti = NULL, result35_i= NULL)`

* Crear un `data.frame` auxiliar que contendrá los nombres/comandos de las variables interés de la operación:
  
  ```
  i <- 1:10
  c = paste0("El resultado para ", i, " es: ")
  d = 35/1:10
  soc <- data.frame(result_i = c,result_35_i = d)
  ```

* ***NOTA***: result_i contendrá los resultados para los valores que tomará i, result_35_i contendrá los valores que tomará el loop al realizar la operación 35/i.

* Utilizar la función `rbind` para unir ambos `data.frame` en la operación:
  
  ```
  for (i in 1:10) {
    df <- rbind (df,soc)
    }
  df
  ```
  
<img width="307" height="326" alt="Ejercicio 4c, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/15a7f70c-00f5-41a2-988a-e6d7cd765fd7" />


### Ejercicio 5

Abre en RStudio el script `PracUni1Ses3/mantel/bin/1.IBR_testing.r`. Este script realiza un análisis de [aislamiento por resistencia](http://www.bioone.org/doi/abs/10.1554/05-321.1) con Fst calculadas con ddRAD en *Berberis alpina*.

Lee el código del script y determina:

- ¿Qué hacen los dos for loops del script?
  
  Se busca hacer un Mantel test, el cual se emplea en ecología para evaluar la significancia de la relación (correlación) entre dos matrices de distancia calculadas entre pares de muestras; para esto se necesita:
  
  -El primer loop, que permite obtener la matriz de distancia efectiva (para comprobar la autocorrelación espacial) y la media de la matriz para cada trama.
  
  -El segundo loop, que permite realizar consecutivamente el Mantel test para cada condición de estudio.

- ¿Qué paquetes necesitas para correr el script?
  
  Se necesitan los paquetes ade4, sp y ggplot2.

- ¿Qué archivos necesitas para correr el script?
  
  Necesitaria 4 archivos:
  
  -surveyed_mountains.tsv
  
  -BerSS.sumstats.tsv
  
  -BerSS.fst_summary.tsv
  
  -Balpina_focalpoints.txt

### Ejercicio 6

Escribe una función llamada `calc.tetha` que te permita calcular tetha dados Ne y u como argumentos. Recuerda que tetha =4Neu.

* Primero se debe escribir el objeto en el cual estará la función:
  
  `calc.tetha <- function(Ne, u)`

* Luego dar las instrucciones e identificar partes de la función:
  
  ```
  ##Función que calcula tetha dado Ne y u
    ##Argumentos
    #Ne
    #u
    ##Función
    #Cálculo de tetha:
    calculo.tetha <- 4*Ne*u
    return(calculo.tetha)
  ```

* ***NOTA***: Recordar que hay que colocar `return` para que el resultado de la dunción vuelva al objeto asociado.

* Dar valores a los argumentos:
  
  `calc.tetha(Ne= 3, u=2)`
  
<img width="333" height="174" alt="Ejercicio 6, Tarea 3 bioinfo" src="https://github.com/user-attachments/assets/00962c21-c00b-424c-a566-f53205391433" />


