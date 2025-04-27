## 👨🏽‍💻 ECONOMIST / BUSINESS INTELLIGENCE / BUSINESS DATA ANALYST  

¡Hola! Soy Emilio Quimis 👋, Economista proactivo, estudiante del Bootcamp Business Data Analyst de la ESPOL, con experiencia en datos en entidades públicas como privadas, con buenas propuestas de innovación y sostenibilidad que se pueden adaptar a cualquier necesidad. De aprendizaje rápido y constante, responsable y dedicado con el trabajo. Con enfoque en los datos y la importancia de estos en cualquier ámbito social o económico que exista, lo que posibilita que mis trabajos sean integrales y orientados a mantener el bienestar de las personas.

## 💼 Habilidades y Herramientas
🚀 Trabajo con las siguientes tecnologías:  
<img  alt="python" src ="https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white"/>
<img alt="Power BI" src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=Microsoft%20Power%20BI&logoColor=black"/>
<img alt="Excel" src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=Microsoft%20Excel&logoColor=white"/>
<img alt="MySQL" src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white"/>
<img alt="SPSS" src="https://img.shields.io/badge/SPSS-007ACC?style=for-the-badge&logo=IBM&logoColor=white"/>

## 👨🏽‍💼 Trabajos
<div align="center">
  <img href="https://github.com/EmilioQuimisM/-Coding-Bootcamps-ESPOL" height="300"  src="https://github.com/EmilioQuimisM/-Coding-Bootcamps-ESPOL/blob/main/Doordash.png" alt="Card header"/> 
</div>

## 🪪 Curriculum Vitae
<div align="center">
  <img height="200"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Codigo%20QR.png" alt="Card header"/> 
</div>
<h3 align="center">
  <a href="https://drive.google.com/file/d/1Z3rexKRv6hgbh8CIEu1GZM8r7v9TXhbC/view?usp=drive_link" download>
    <img alt="Descargar" src="https://img.shields.io/badge/Descargar-007ACC?style=for-the-badge&logo=download&logoColor=white"/>
  </a>
</h3>



## 🌍 Conectemos    
<a href="mailto:emilioqm89@gmail.com" target="_blank"><img height="28" src = "https://img.shields.io/badge/gmail-c14438?&style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/emilio-andres-quimis-muentes-569565196" target="_blank"> <img height="28" src = "https://img.shields.io/badge/-LinkedIn-0e76a8?style=for-the-badge&logo=Linkedin&logoColor=white"></a>

---

⭐ ¡Gracias por visitar mi perfil! No dudes en conectar conmigo para compartir ideas sobre análisis de datos e inteligencia de negocios. 🚀


##  👨🏽‍💼 Transformando sospechas en decisiones con Machine Learning 👩🏽‍💼
Predicción de fraude en reclamos de seguros

En el año 2023, una aseguradora de Colombia registró más de 24.000 fraudes, sumando pérdidas de más de 62 millones de dólares. Si pensamos que cada fraude costó más de $2.500 en promedio
<div align="center"> ¿Cómo podemos anticiparnos a estos eventos antes de que ocurran? </div>

<div align="center">
  <img height="420"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/que%20hace%20el%20modelo.png" alt="Card header"/> 
</div>

## Metodología - Análisis Exploratorio
El dataset consta de 15,420 registros y 33 columnas, con una mayoría de variables de tipo categórico.
La mayoría de las variables son categóricas (25) y el resto numéricas (8)
Hallazgo Relevante 1 (Desbalance de Clases): La variable objetivo FraudFound presenta un fuerte desbalance, con solo un 6% de los casos etiquetados como fraude. Esto implica la necesidad de técnicas específicas para el modelado.
Hallazgo Relevante 2 (Valores Inválidos): Se identificaron valores inválidos como "0" en columnas de fecha (DayOfWeekClaimed, MonthClaimed), los cuales requerirán limpieza.
Hallazgo Relevante 3 (Baja Variabilidad): Variables como WitnessPresent,AgentType, AddressChange-Claim y NumberOfCars mostraron baja variabilidad, lo que sugiere un potencial bajo poder predictivo (aunque se mantuvieron para evaluación con SHAP).
Algunas variables categóricas (Make, Fault, VehiclePrice, etc.) muestran diferencias visuales claras entre clases, lo que indica potencial valor predictivo.

<div align="center">
  <img height="320"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Metodolog%C3%ADa%20-%20An%C3%A1lisis%20Exploratorio.png" alt="Card header"/> 
</div>

## Metodología - Procesamiento de Datos

Se identificaron 320 registros con un valor de "0" en la variable Age. Para preservar la información de estos registros, en lugar de eliminarlos, se optó por la imputación utilizando la mediana de la edad dentro del grupo correspondiente de AgeOfPolicyHolder
Manejo de Valores Inválidos: Se eliminaron los registros con valores "0" en DayOfWeekClaimed y MonthClaimed ya que no representan datos válidos.
Eliminación de Columnas: Se eliminaron PolicyNumber (ID único sin valor predictivo), Year (baja variabilidad), Month, Age, RepNumber, y PolicyType (siguiendo indicaciones del tutor).
Manejo de Duplicados: Se eliminó una fila duplicada para asegurar la integridad de los datos.
Corrección de Inconsistencias: Se unificaron entradas inconsistentes en la columna Make (ej., 'Accura' a 'Acura').
Feature Engineering: Se crearon nuevas variables como ClaimLag, HighRiskProfile, IsSingleYoung, ExpensiveVehicle, WeekendClaim para extraer información potencialmente predictiva.
Codificación de Variables Categóricas: Las variables categóricas se transformaron a un formato numérico utilizando la técnica de one-hot encoding (pd.get_dummies).

<div align="center">
  <img height="320"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Metodolog%C3%ADa%20-%20Procesamiento%20de%20Datos.png" alt="Card header"/> 
</div>

## Metodología - Entrenamiento y Tuneo de Hiperparámetros

El dataset se dividió en conjuntos de entrenamiento (60%), validación (20%) y prueba (20%) manteniendo la proporción de la clase objetivo (estratificación).
El dataset presenta un desequilibrio considerable en la variable objetivo, donde los casos de fraude comprenden menos del 7% del total de las instancias. Esta distribución desigual de clases, que calificamos como un desequilibrio severo.
Se probaron varios algoritmos de clasificación: CatBoost, XGBoost, LightGBM, RandomForest y BalancedBagging.
Si bien el AUC obtenido con class_weight (0.794) y undersampling (0.811) es aceptable dada la baja proporción de fraudes (6%), el AUC excesivamente alto de SMOTE (0.995) apunta a un probable sobreajuste o una posible fuga de información durante la validación cruzada.
Se aplicó submuestreo aleatorio (RandomUnderSampler) en el conjunto de entrenamiento para mitigar el desbalance de clases.
Se realizó una búsqueda aleatoria (RandomizedSearchCV) con validación cruzada estratificada (5 folds) para encontrar los hiperparámetros óptimos para cada modelo, utilizando la métrica F1-score como principal criterio de optimización debido al desbalance de clases y la necesidad de un equilibrio entre precisión y recall. Sin embargo, dada la prioridad de no dejar pasar fraudes, se prestó especial atención al recall.

<div align="center">
  <img height="320"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Metodolog%C3%ADa%20-%20Entrenamiento%20y%20Tuneo%20de%20Hiperpar%C3%A1metros.png" alt="Card header"/> 
</div>

## Metodología - Interpretabilidad/Explicabilidad del Modelo

Se utilizó la librería SHAP (SHapley Additive exPlanations) para comprender la importancia de las variables en las predicciones de los 3 modelos XGBoost, LightGBM y CatBoost(el de mejor rendimiento).
Se generaron gráficos de resumen (summary plots) para visualizar tanto la importancia de las features como la dirección de su impacto en la predicción de fraude.
El alto valor predictivo de variables como Fault_Third Party y BasePolicy_Liability sugiere que el fraude puede estar más relacionado con la naturaleza del contrato y no tanto con el perfil personal.
Ejemplo de Insight: La variable Fault_Third Party mostró ser una de las más importantes, con valores altos (cuando la culpa es del tercero) empujando la predicción hacia fraude, lo cual tiene sentido de negocio.
Pruebas Fallidas: Se exploraron diferentes técnicas de sobremuestreo (SMOTE) para el desbalance de clases, pero los resultados sugirieron un posible sobreajuste, por lo que se optó por el submuestreo aleatorio.
la probabilidad de fraude predicha por CatBoost estuvo considerablemente más alejada del punto de decisión (el umbral) en la dirección de "no fraude" que las predicciones de XGBoost y LightGBM. Esto sugiere que CatBoost encontró características en esta reclamación que lo llevaron a una conclusión más firme de que no se trataba de un caso fraudulento.

<div align="center">
  <img height="320"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Metodolog%C3%ADa%20-%20Interpretabilidad%20Explicabilidad%20del%20Modelo.png" alt="Card header"/> 
</div>

## Resultados - Rendimiento

Finalmente, se procede a re-entrenar y evaluar los modelos CatBoost, XGBoost y LightGBM utilizando únicamente las 14 variables más importantes identificadas mediante el análisis de interpretabilidad SHAP.
Se re-entrena el modelo utilizando el conjunto de entrenamiento reducido (X_train_reduced) y las etiquetas de entrenamiento balanceadas (y_resampled).
Se realizan predicciones sobre el conjunto de prueba reducido (X_test_reduced).
Se calculan y se imprimen el área bajo la curva ROC (ROC AUC) y el informe de clasificación (classification_report), que incluye precisión, recall, F1-score y soporte para cada clase (no fraude y fraude).

El modelo CatBoost original (entrenado con todas las variables) fue finalmente seleccionado como el mejor debido a su mejor ROC AUC(0.8066) en test set, manteniendo un recall alto (96.2%) que el resto sin una pérdida significativa en el F1-score en comparación con los modelos entrenados solo con las variables importantes.

<div align="center">
  <img height="320"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Resultados%20-%20Rendimiento.png" alt="Card header"/> 
</div>


## Implementación en el Negocio
<div align="center"> Propuesta  </div>
El modelo CatBoost se integraría en el sistema de gestión de reclamaciones de la aseguradora. Cada nueva reclamación sería evaluada por el modelo en tiempo real o por lotes periódicos.

<div align="center"> Justificación </div>

<div align="center"> Eficiencia, Reducción de Pérdidas y Prácticas Similares
</div>

<div align="center">
  <img height="320"  src="https://github.com/EmilioQuimisM/EmilioQuimisM/blob/main/Implementaci%C3%B3n%20en%20el%20Negocio.png" alt="Card header"/> 
</div>


## Conclusiones y Recomendaciones
<p align="center"> <div align="center"> Conclusión </div> </p>
 El proyecto demostró la viabilidad de utilizar un modelo de machine learning (CatBoost) para la detección de fraudes en seguros de autos, logrando un alto recall en la identificación de casos fraudulentos y un potencial impacto económico positivo significativo.
<p align="center"> <div align="center"> Recomendaciones </div> </p>
Explorar técnicas más avanzadas para el manejo de desbalance de clases (ej., algoritmos sensibles al costo, generación de datos sintéticos más sofisticada).
Investigar la incorporación de otras fuentes de datos relevantes que puedan mejorar la capacidad predictiva del modelo.
Experimentar con arquitecturas de modelos más complejas o ensambles de modelos que puedan mejorar el equilibrio entre precisión y recall.
Invertir en la recopilación y el almacenamiento de datos más detallados y diversos sobre los asegurados y las reclamaciones.
Establecer un proceso claro para la revisión y retroalimentación de los casos clasificados como de alto riesgo para mejorar continuamente el modelo y comprender mejor los patrones de fraude.
Evaluar el costo-beneficio de ajustar el umbral de clasificación para equilibrar la detección de fraudes con el costo de los falsos positivos. </div> </p>

## 🌍 Conectemos  
# Miguel Briones👨🏽‍💻
<a href="mailto:emilioqm89@gmail.com" target="_blank"><img height="28" src = "https://img.shields.io/badge/gmail-c14438?&style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/emilio-andres-quimis-muentes-569565196" target="_blank"> <img height="28" src = "https://img.shields.io/badge/-LinkedIn-0e76a8?style=for-the-badge&logo=Linkedin&logoColor=white"></a>
# Jemima Moreira 👩🏽‍💻
<a href="mailto:jhemy321@hotmail.com" target="_blank"><img height="28" src = "https://img.shields.io/badge/gmail-c14438?&style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/jemimamoreiraguzman/" target="_blank"> <img height="28" src = "https://img.shields.io/badge/-LinkedIn-0e76a8?style=for-the-badge&logo=Linkedin&logoColor=white"></a>
# Emilio Quimis 👨🏽‍💻
<a href="mailto:emilioqm89@gmail.com" target="_blank"><img height="28" src = "https://img.shields.io/badge/gmail-c14438?&style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/emilio-andres-quimis-muentes-569565196" target="_blank"> <img height="28" src = "https://img.shields.io/badge/-LinkedIn-0e76a8?style=for-the-badge&logo=Linkedin&logoColor=white"></a>
# Juan Palacios 👨🏽‍💻
<a href="mailto:juanpadani05@gmail.com" target="_blank"><img height="28" src = "https://img.shields.io/badge/gmail-c14438?&style=for-the-badge&logo=gmail&logoColor=white"></a>
<a href="https://www.linkedin.com/in/juan-carlos-palacios-sachez-6a748240/" target="_blank"> <img height="28" src = "https://img.shields.io/badge/-LinkedIn-0e76a8?style=for-the-badge&logo=Linkedin&logoColor=white"></a>

