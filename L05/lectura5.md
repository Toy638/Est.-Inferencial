- Inferencia no parametrica con proporciones
  - No parametrico (Libres de distribución)
    - No hay parametro
    - No hacen suposición de la distribución de la población
    - Ventajas
      - Menos restrictivas
        - No siempre los datos siguen una distribución normal
      - ¿ Por que no usarlas siempre?
        - Entregan Menos información
          - "Las poblaciones muestran proporciones equivalentes"
          - "Las poblaciones muestran proporciones distintas"
          - No indican proporciones en realidad
        - Si se cumplen las condiciones para aplicar parametricas, no parametrico tiene menor poder estadistico
   
    - Chi Cuadrado de Pearson
    
      -  Permite inferir sobre proporciones 
    
      - Cuando aplicar:
        - 2 Variables categóricas y una es dicotómica

      - Condiciones:
        - Observaciones independientes entre sí
        - Al menos 5 observaciones esperadas en cada grupo (Formula).
  
       - 3 Tipos: 
          - Homogeneidad
            - Determinar si dos poblaciones(dicotomica) presentan las mismas proporciones en diferentes niveles de una variable categórica
            - Ejemplo programadores y programadoras
          - Bondad de ajuste
            - Comprobar si una distribuciónde frecuencias observada se asemeja a una distribución esperada. Usualmente se utiliza para comprobar si una muestra es representativa de la población.
          - Independencia
            - Permite determinar si 2 variables categoricas de una misma poblacion son estadisticamente independiente
            - Hongos
    - Pruebas para muestras pequeñas
      - Prueba exacta de fisher
        - Alternativa chi^2 cuando ambas variables son dicotomicas
        - Hipotesis
          - H0: Las variables son independientes
          - Ha: Las variables estan relacionadas
          - Ejemplo vampiros y vacunas
      - Prueba mcnemar
      - Prueba Q de cochran
        - Hipotesis
          - H0: La proporción de "exitos" es la misma para todos los grupos
          - Ha: La proporciónde "exitos" es distinta para al menos un grupo
        - Condiciones:
          - La variable de respuesta es dicotómica
          - La variable independiente es categórica
          - Observaciones independientes entre sí
          - Tamaño de la muestra suficiente mente grande. n*k >= 24, n >=4, numero de caos cuya respuestas no son unicamente E o Fracaso y k, la cantidad de niveles de la variable independiente
        - Omnibus
          - Post-hoc
            - Una vez que se verifican diferencias significativas
          - Correciones
            - Benferroni
              - Conservador 
              - Mantiene la probabilidad de cometer error tipo 1 Mas baja que el nivel de significacion establecido
            - Holm
              - \> Poder estadistico que benferroni 

--- 
Resources
https://www.youtube.com/watch?v=t_jfTOE44YQ

