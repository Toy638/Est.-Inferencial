- Métodos más contemporaneos para enfrentar datos problemáticos
    - Metodos Robustos
        - Ejemplo problemáticas
          - T Student (Media)
            - Incumplimiento supuesto normalidad
              - Resultados sesgados
              - Intervalos de confianza calculados de manera inadecuada
              - Reducción del poder estadístico de la prueba
      - Alternativas robustas (WRS2)
        - Mediana
        - Media truncada
          - Descarta un determinado porcentaje en ambos extremos (colas)
          -  ```mean(, trim) ```
          - Puede causar problemas si se descartan muchos datos
        - Media windsorizada
          - En lugar de descartar los valores extremos, se reemplazan por los valores extremos 
          - ``` winmean(x,tr) ```
        - Prueba de yuen
          - Utiliza Medias truncadas y windsorizadas
          - No se recomienda usar esta prueba si las muestras se truncan cerca del nivel de medianas $ \gamma \approx 0.5$ 
            - ??? 
          - Alternativa a t student muestras independientes 
            - Varianzas son muy diferentes
            - Tamaños de muestras muy dispares
            - yuen(formula, data, tr)
              - formula: variable dependiente ~ variable independiiente
                - Variable independiente debe tener dos niveles
              - data: matriz de datos
              - tr: parametro $ \gamma $ de la poda
            - pb2gen
              - Remuestreo bootstrapping
              -  ```  pb2gen(formula, data, est, nboot) ```
            - Script 11.1
            - Script 11.2
        - Prueba de yuen para dos muestras pareadas
          - Usa medias truncadas
          - ``` yuend ```
          - Script 11.3
        - Comparaciones de una vía para multiples grupos independientes
          - Ejemplos de cuando usar
            - Cuando los tamaños muestrales son muy diferentes
            - Cuando no se cumple la condición de homocedasticidad
          - ```t1way(formula, data, tr, alpha)```
            - Procedimiento Similar a ANOVA usamdo medias truncadas
            - Post-Hoc
              - ```  lincon(formula, data, tr, alpha) ```
          - ```t1waybt(formula, data, tr, nboot)```
            - Análogo al interior solo que además realiza bootstrapping
            - Post-Hoc
              - ```  lincon(formula, data, tr, alpha) ```
          - ```med1way(formula, data, iter)```
            - EL paquete no ofrece Post-Hoc
          - Script 11.4
        - Comparaciones de una via para multiples grupos correlacionados
          - Cuando los datos violan la condición de esfericidad
          - ``` rmanova(y,groups,block,tr) ```
            - Similar a anova usando medias truncadas
            - Post-hoc
              - ``` rmmcp(y,groups,blocks,tr,nboot) ```
          - ``` rmanovab(y,groups,block,tr, nboot) ```
            - Post-hoc
              - ``` pairdepb(y,groups,blocks,tr,nboot) ```  
          - Script 11.5 
          - ```  ```  
      - Remuestreo
        - Bootstrapping (boot, bootES)
          - Procedimiento general
            - Generar B muestras con reposición del mismo tamaño.
            - Calcular estadístico en cada muestra. Obteniendo distribucion bootstrap
            - Usar distribución bootstrap para analizar estadístico de interés.
            - Puede aplicarse para casi cualquier estadístico
          - Bootstrapping para una muestra
            - Script 11.6: construcción de un intervalo de confianza para la media poblacional mediante bootstrapping.
            - Script 11.7: inferencia sobre la media de una muestra con bootstrapping.