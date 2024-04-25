# S7_featureEng_split_dataLeakage

## Material de Francisco

- Feature Engineering
- Split en distintos tipos de datasets
- Data Leakage
- Tratamiento de datos desbalanceados

## Webinar DS 7.2 - Métricas de evaluación de modelos

- Matriz de confusión.
- Sensibilidad.
- Especificidad.
- Otros derivados de la Matriz de Confusión.
- F_{beta=1}-Score.
- F_{beta}-Score.
- MCC
- Gain y Lift.
- ROC
- AUC

### Links relevantes

- https://machinelearningmastery.com/fbeta-measure-for-machine-learning/
- https://scikit-learn.org/stable/modules/generated/sklearn.metrics.fbeta_score.html
- https://www.cs.odu.edu/~mukka/cs795sum09dm/Lecturenotes/Day3/F-measure-YS-26Oct07.pdf
- https://stats.stackexchange.com/questions/221997/why-f-beta-score-define-beta-like-that
- https://en.wikipedia.org/wiki/Sensitivity_and_specificity
- https://en.wikipedia.org/wiki/F-score
- http://qwone.com/~jason/writing/fmeasure.pdf
- https://www.youtube.com/watch?v=PeYQIyOyKB8
- https://www.youtube.com/watch?v=LbX4X71-TFI
- https://en.wikipedia.org/wiki/Arithmetic_mean
- https://en.wikipedia.org/wiki/Geometric_mean
- https://en.wikipedia.org/wiki/Harmonic_mean
- https://www.gaussianos.com/demostracion-visual-de-la-relacion-entre-media-aritmetica-y-media-geometrica/
- https://en.wikipedia.org/wiki/Gini_coefficient
- https://towardsdatascience.com/using-the-gini-coefficient-to-evaluate-the-performance-of-credit-score-models-59fe13ef420
- https://developers.google.com/machine-learning/crash-course/classification/roc-and-auc?hl=es-419
- https://howtolearnmachinelearning.com/articles/the-lift-curve-in-machine-learning/

## Webinar DS 8.1 - Tratamiento de datos desbalanceados

- Por qué es importante balancear los datos
- Comparación entre modelo
	  - Sin tratamiento de desbalance
	  - Con balance de clases
	  - Con sobre-muestreo aleatorio
	  - Con sub-muestreo
	  - Con sobre-muestreo SMOTE.
- Intuición de KNN

### Links relevantes

- https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html
- https://en.wikipedia.org/wiki/F-score
- https://machinelearningmastery.com/smote-oversampling-for-imbalanced-classification/
- https://www.analyticsvidhya.com/blog/2020/11/handling-imbalanced-data-machine-learning-computer-vision-and-nlp/
- https://www.analyticsvidhya.com/blog/2018/03/introduction-k-neighbours-algorithm-clustering/
- https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_classification.html

## Webinar DS.9.1 - Bootstrapping, data leakage, crossvalidation, Data Centric vs Model Centric AI


- Qué es Bootstrapping
	  - Método de resampling con repetición
- Qué es Data Leakage
	  - Problema con missing values
	  - Problemas con series de tiempo
	  - Problemas con normalización
	  - Ejemplo con upsampling
- Qué es Crossvalidation
	  - Importancia de hacer cross validation solo en nuestro dataset de entrenamiento

### Links relevantes

- https://www.mastersindatascience.org/learning/machine-learning-algorithms/bootstrapping/
- https://www.youtube.com/watch?v=STGGniMV0jg&ab_channel=ChristinaKnudson
- https://www.youtube.com/watch?v=Xz0x-8-cgaQ&ab_channel=StatQuestwithJoshStarmer
- https://www.youtube.com/watch?v=fE_25esn-5U&ab_channel=CynthiaRudin
- https://www.youtube.com/watch?v=y8qaI5mpJeA&ab_channel=DataRobot
- https://www.youtube.com/watch?v=n9jz7G68pVg&ab_channel=KrishNaik
- https://www.youtube.com/watch?v=TIgfjmp-4BA&ab_channel=Udacity
- https://www.youtube.com/watch?v=EBJBgyzLGvI&ab_channel=Weights%26Biases
- https://dcai.csail.mit.edu/

## # Webinar DS 12.1 - Feature Engineering y correlación entre variables

- Feature engineering
	- Binning
	- Log Transform
	- One-Hot Encoding
	- Grouping Operations
	- Feature Split
	- Scaling
	- Extracting Date
- Cómo lidiar con datasets con muchas variables y cómo elegir con cuales quedarse
- Diferencia entre correlación y correlación lineal
- Por qué los árboles hacen cortes lineales unidimensionales y cómo eso limita al algoritmo
	- Ejemplo de cómo el Random Forest predice bien un tablero de ajedrez pero el árbol no

### Links relevantes:

- https://towardsdatascience.com/feature-engineering-for-machine-learning-3a5e293a5114#199b
- https://www.freecodecamp.org/news/how-machines-make-predictions-finding-correlations-in-complex-data-dfd9f0d87889/
- https://medium.com/data-science-in-your-pocket/calculating-non-linear-correlation-using-distance-correlation-with-examples-83f6a8cf2473
- https://www.youtube.com/watch?v=gTu_Li7AY7I&ab_channel=GarethTribello
- https://www.youtube.com/watch?v=xZ_z8KWkhXE&ab_channel=StatQuestwithJoshStarmer
- https://www.youtube.com/watch?v=3I-mXOoSY-o&ab_channel=DataScienceinyourpocket

## Webinar DS 14.1 - Intro a NLP

- Representación de una palabra en forma de vector
- Espacios vectoriales de dimensión infinita y su aproximación por espacios vectoriales de dimensión finita.

### Links relevantes:

- https://en.wikipedia.org/wiki/Embedding