

## CAPÍTULO 11: Métodos Más Contemporáneos para Enfrentar Datos Problemáticos
- **Introducción**
  - Importancia de enfrentar datos que no cumplen con ciertas propiedades.
  - Métodos clásicos como alternativas.
  - Aumento en el acceso y poder de cómputo.
  - Estrategias para analizar datos problemáticos.

### 11.1 MÉTODOS ROBUSTOS
- **Pruebas estadísticas clásicas y requisitos**.
  - **Problemas con el incumplimiento del supuesto de normalidad**.
    - Resultados Sesgados
    - Intervalos de confianza calculados de manera inadecuada
    - Reducción del poder estadístico de la prueba
- **Estimadores robustos y su utilidad**.
- **Alternativas robustas en R**.
  - WRS2

#### 11.1.1 Alternativas robustas para la media
- **Mediana como alternativa robusta**.
- **Media truncada**.
  - Valores extremos atípicos
  - 
- **Media Winsorizada**.
  - Casos en los que se pierde demasiada información
  - winmean(x,tr=0.2)

#### 11.1.2 Prueba de Yuen para dos muestras independientes
- **Alternativa a la prueba t de Student**.
- **Uso de medias truncadas y Winsorizadas**.
- **Implementación en R**.

## Referencias bibliográficas
- (Aquí puedes agregar las referencias bibliográficas específicas del documento).
