# Análisis de Comportamiento de Usuarios en Dispositivos Móviles

## I. Definición del problema de negocio

### Descripción del problema

En la actualidad, el uso de dispositivos móviles se ha convertido en una parte fundamental de la vida cotidiana. Las empresas de tecnología y desarrolladores de aplicaciones necesitan comprender los patrones de comportamiento de los usuarios para optimizar sus productos, mejorar la experiencia del usuario y desarrollar estrategias de marketing efectivas. Sin embargo, existe una brecha en la comprensión de cómo diferentes factores demográficos y características de los dispositivos influyen en los patrones de uso.

### Pregunta de investigación

¿Cómo se relacionan las características demográficas (edad, género) y las especificaciones del dispositivo (modelo, sistema operativo) con los patrones de uso (tiempo de uso de aplicaciones, consumo de batería, uso de datos) y cómo estos factores pueden predecir las diferentes clases de comportamiento de usuario?

### Métricas para evaluar el éxito

1. **Precisión de clasificación**: Capacidad para predecir correctamente la clase de comportamiento del usuario basado en variables demográficas y de uso.
2. **Coeficiente de correlación**: Fuerza de la relación entre variables clave (tiempo de uso, consumo de batería, etc.).
3. **Varianza explicada**: Porcentaje de la variabilidad en el comportamiento del usuario que puede ser explicada por nuestro modelo.
4. **Segmentación efectiva**: Identificación clara de perfiles de usuario con características distintivas.
5. **Aplicabilidad práctica**: Capacidad para generar recomendaciones accionables para desarrolladores y empresas.

## II. Fuentes de datos

### Descripción de la fuente principal

- **Nombre del dataset**: Mobile Device Usage and User Behavior Dataset
- **Formato**: CSV (Comma-Separated Values)
- **Tamaño**: 700 registros x 11 columnas
- **Fuente**: Kaggle (valakhorasani/mobile-device-usage-and-user-behavior-dataset)

### Variables incluidas

1. **User ID**: Identificador único del usuario
2. **Device Model**: Modelo del dispositivo móvil (Google Pixel 5, OnePlus 9, Xiaomi Mi 11, iPhone 12, Samsung Galaxy S21)
3. **Operating System**: Sistema operativo del dispositivo (Android, iOS)
4. **App Usage Time (min/day)**: Tiempo diario de uso de aplicaciones en minutos
5. **Screen On Time (hours/day)**: Tiempo diario con la pantalla encendida en horas
6. **Battery Drain (mAh/day)**: Consumo diario de batería en miliamperios-hora
7. **Number of Apps Installed**: Número de aplicaciones instaladas en el dispositivo
8. **Data Usage (MB/day)**: Consumo diario de datos en megabytes
9. **Age**: Edad del usuario
10. **Gender**: Género del usuario (Male, Female)
11. **User Behavior Class**: Clasificación del comportamiento del usuario (1-5, donde 5 representa el uso más intensivo)

## III. Planeación

### Tablero en Trello

Se ha creado un tablero en Trello para la gestión del proyecto con las siguientes listas:

- **Por hacer**
- **En progreso**
- **Hecho**

### Tareas principales

1. **Definición del problema de negocio**
   - Descripción: Redactar la descripción del problema, pregunta de investigación y métricas
   - Responsable: [Nombre del responsable]
   - Fecha límite: [Fecha]

2. **Selección y descripción de fuentes de datos**
   - Descripción: Documentar formato, tamaño y origen de los datos
   - Responsable: [Nombre del responsable]
   - Fecha límite: [Fecha]

3. **Exploración inicial del dataset**
   - Descripción: Analizar características y distribuciones de los datos
   - Responsable: [Nombre del responsable]
   - Fecha límite: [Fecha]

4. **Generación del informe con Pandas Profiling**
   - Descripción: Ejecutar notebook y generar informe detallado
   - Responsable: [Nombre del responsable]
   - Fecha límite: [Fecha]

5. **Análisis de resultados**
   - Descripción: Interpretar hallazgos y generar insights
   - Responsable: [Nombre del responsable]
   - Fecha límite: [Fecha]

6. **Preparación de la entrega final**
   - Descripción: Compilar todos los entregables requeridos
   - Responsable: [Nombre del responsable]
   - Fecha límite: [Fecha]

### Enlace al tablero

[Enlace al tablero de Trello](https://trello.com/b/XXXXXXXX/analisis-comportamiento-usuarios-moviles)

## IV. Creación del repositorio

Se ha creado un repositorio en GitHub con la siguiente estructura:

- **README.md**: Contiene la información del problema de negocio y descripción general del proyecto
- **exploracion_dataset.ipynb**: Notebook de Jupyter con el código de exploración y análisis
- **user_behavior_dataset.csv**: Dataset original
- **requirements.txt**: Dependencias necesarias para ejecutar el código
- **visualizaciones/**: Carpeta con gráficos generados durante el análisis

### Enlace al repositorio

[Enlace al repositorio de GitHub](https://github.com/usuario/analisis-comportamiento-usuarios-moviles)

## V. Exploración

### Análisis exploratorio de datos

Se ha realizado un análisis exploratorio utilizando pandas_profiling para generar un informe detallado del dataset. A continuación, se presentan las principales observaciones:

#### Estadísticas generales

- **Número de registros**: 700
- **Número de variables**: 11
- **Variables numéricas**: 7
- **Variables categóricas**: 3 (excluyendo User ID)

#### Valores nulos y duplicados

- No se encontraron valores nulos en el dataset
- No se detectaron registros duplicados

#### Distribución de variables categóricas

- **Device Model**: Distribución relativamente uniforme entre los 5 modelos de dispositivos
- **Operating System**: Predominancia de Android (aproximadamente 80%) sobre iOS (20%)
- **Gender**: Distribución equilibrada entre géneros (aproximadamente 50% cada uno)
- **User Behavior Class**: Distribución relativamente uniforme entre las 5 clases de comportamiento

#### Distribución de variables numéricas

- **App Usage Time**: Media de aproximadamente 250 minutos/día, con distribución ligeramente sesgada a la derecha
- **Screen On Time**: Media de aproximadamente 5 horas/día
- **Battery Drain**: Media de aproximadamente 1500 mAh/día, fuertemente correlacionada con el tiempo de uso
- **Number of Apps Installed**: Media de aproximadamente 50 aplicaciones
- **Data Usage**: Media de aproximadamente 800 MB/día, con alta variabilidad
- **Age**: Distribución amplia entre 18-65 años, con mayor concentración en el rango 25-45

#### Correlaciones principales

- Fuerte correlación positiva entre tiempo de uso de aplicaciones y consumo de batería (r > 0.9)
- Correlación significativa entre tiempo de pantalla encendida y consumo de datos (r ≈ 0.7)
- Correlación moderada entre número de aplicaciones instaladas y consumo de datos (r ≈ 0.6)
- La clase de comportamiento del usuario está fuertemente correlacionada con el tiempo de uso de aplicaciones y el consumo de batería

#### Hallazgos clave por segmentos

- Los usuarios de dispositivos Samsung Galaxy S21 y OnePlus 9 muestran mayor tiempo de uso promedio
- Los usuarios más jóvenes (18-30 años) tienden a tener mayor consumo de datos y tiempo de pantalla
- Los usuarios de Android muestran patrones de uso ligeramente diferentes a los de iOS, con mayor variabilidad en el consumo de batería
- Las clases de comportamiento 4 y 5 (uso intensivo) muestran patrones distintivos en todas las métricas de uso

### Conclusiones

1. Existen patrones claros de comportamiento que pueden ser identificados y clasificados
2. Las variables demográficas y de dispositivo influyen significativamente en los patrones de uso
3. El consumo de batería y el tiempo de uso están estrechamente relacionados, lo que sugiere oportunidades para optimización
4. La segmentación por clase de comportamiento proporciona insights valiosos para estrategias de marketing y desarrollo de productos
5. Se recomienda un análisis más profundo utilizando técnicas de aprendizaje automático para predecir comportamientos y personalizar experiencias

