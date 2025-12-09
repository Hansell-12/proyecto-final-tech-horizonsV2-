# Circular Data Madrid
## *"Analizamos, optimizamos y reducimos impactos para una ciudad más limpia y resiliente".*

### ODS 9: Industria, innovación e infraestructura
### ODS 9 Objetivo:  
Industria, Innovación e Infraestructura busca construir infraestructuras resilientes, fomentar la industrialización sostenible y promover la innovación.


---

## Información del Equipo

|        Nombre       |       GitHub          |          Responsabilidades             |
|---------------------|-----------------------|----------------------------------------|
|   Sofia Acosta      |    @sofii0104         | Análisis exploratorio, presentación    |
|   Hellen Bonilla    |    @Hellen            | Limpieza y preparación de datos        |
|   Hansel Ramírez    |    @Hansell-12        | Repositorio de GitHub                  |
|   Rafael Mezua      |    @rafaelmezua       | Coordinación, presentación             |
|   Elias Arosemena   |                       | Análisis exploratorio, estadísticas    |
|   Alison Bonilla    |                       | Coordinación, presentación             |
|   Alexandra Barrios |    @ct24-alexabarrios | Coordinación, presentación             |
|   Brihanna          |                       | Modelado y proyecciones                |

---

## Problemática

### ¿Qué problema estamos resolviendo?
En la Comunidad de Madrid persisten importantes desafíos relacionados con la separación, recolección y valorización de residuos reciclables. A pesar de contar con un sistema de contenedores por fracción y diversas infraestructuras de tratamiento, su cobertura y accesibilidad no son homogéneas entre los distritos. Asimismo, se observan tasas significativas de impropios en las fracciones reciclables, lo que limita la eficiencia de los procesos de recuperación de materiales como plástico, vidrio, aluminio, papel y cartón.
Como consecuencia, una proporción considerable de los residuos generados continúa siendo destinada a infraestructuras como el Parque Tecnológico de Valdemingómez, lo que contribuye a la saturación del sistema, aumenta los costos operativos y genera impactos ambientales negativos. Esta situación evidencia una brecha entre la capacidad instalada y las necesidades reales de la población madrileña.


### ¿Por qué es importante?
La insuficiencia de infraestructura y la desigual participación ciudadana en los programas de reciclaje tienen repercusiones ambientales, económicas y sociales. Entre ellas destacan:

- **Incremento de la contaminación** del aire, suelo y recursos hídricos debido al manejo ineficiente de residuos y al aumento de desechos destinados a vertedero.

- **Presión creciente sobre las instalaciones de Valdemingómez**, cuya capacidad se encuentra al límite, afectando la sostenibilidad del sistema de gestión de residuos municipal.

- **Pérdida de oportunidades de desarrollo económico**, específicamente en la expansión de empleos verdes y en la recuperación de materiales con valor económico como PET, aluminio y cartón.

- **Limitaciones para avanzar hacia un modelo de economía circular**, debido al bajo aprovechamiento de los residuos y a la falta de datos precisos para optimizar su gestión.

- **Desigualdades territoriales** en el acceso a puntos limpios y contenedores especializados, lo que resulta en una menor participación de ciertos sectores de la población.

### ¿A quién afecta?
El problema impacta a múltiples actores del ecosistema urbano de Madrid:

- **Residentes de la ciudad**, quienes enfrentan dificultades para acceder a infraestructura adecuada de reciclaje y carecen, en algunos casos, de información suficiente para una correcta separación en origen.

- **Distritos socialmente vulnerables**, afectados de manera desproporcionada por la contaminación y por la falta de servicios de gestión ambiental adecuados.

- **El Ayuntamiento de Madrid**, que debe asumir costos crecientes de recolección, clasificación y disposición final, además de gestionar los riesgos asociados a la saturación del sistema.

- **Organizaciones ambientales y ONGs**, que requieren datos fiables para implementar intervenciones efectivas y orientar campañas de sensibilización.

- **Empresas recicladoras y del sector privado**, que ven limitadas sus oportunidades de recuperación de materiales y de expansión de la economía circular.

- **El entorno natural**, impactado por el aumento de desechos, las emisiones derivadas de su gestión y la pérdida de recursos potencialmente reutilizables.


### Alcance del Proyecto
- **Geográfico:** Local — El proyecto se centra en el municipio de Madrid, abarcando sus 21 distritos y las diferencias territoriales en la infraestructura y participación en el reciclaje.

- **Temporal:** El análisis cubre el período 2018–2025, correspondiente a los datos disponibles en el Portal de Datos Abiertos del Ayuntamiento de Madrid sobre la generación y recogida de residuos urbanos.

- **Población:** La población objetivo incluye:
  - **Los residentes del municipio de Madrid**, principales generadores de los residuos analizados.

  - **Distritos con características sociodemográficas diferenciadas**, lo que permite evaluar desigualdades en acceso a infraestructura de reciclaje.

  - **Actores institucionales** relacionados con la gestión de residuos (Ayuntamiento de Madrid, empresas gestoras y puntos limpios).


---

## Datos Utilizados

### Fuentes de Datos
| Dataset  | Fuente |     Descripción     |    Período    |
|----------|--------|---------------------|---------------|
| [Nombre] | [URL]  | [Descripción breve] | [Años/fechas] |
| [Nombre] | [URL]  | [Descripción breve] | [Años/fechas] |

---

## Tecnologías Utilizadas

- ![Python](https://img.shields.io/badge/-Python-blue?logo=python) **Python** - Lenguaje principal
- ![Pandas](https://img.shields.io/badge/-Pandas-green?logo=pandas) **Pandas** - Manipulación de datos
- ![Streamlit](https://img.shields.io/badge/-Streamlit-red?logo=streamlit) **Streamlit** - Dashboard interactivo
- ![Plotly](https://img.shields.io/badge/-Plotly-blue?logo=plotly) **Plotly** - Visualizaciones interactivas
- ![GitHub](https://img.shields.io/badge/-GitHub-black?logo=github) **GitHub** - Control de versiones

## Metodología

### Proceso de limpieza y análisis

**1. Carga del archivo**

  -  Se cargó el dataset usando pandas.read_csv(), especificando el separador correcto sep=';'.

**2. Revisión inicial**

  - Se analizaron:
  - Las primeras filas del dataset (df.head())

  - La estructura completa (df.info())

  - Estadísticas generales (df.describe())

  - Cantidad de valores nulos por columna (df.isnull().sum())

*Esto permitió comprender el estado del archivo.*

**3. Limpieza básica**

Se realizaron las siguientes acciones:

  - Eliminación de columnas irrelevantes.

  - Conversión de coordenadas X y Y a valores numéricos

  - Filtrado de filas vacías o incorrectas

  - Normalización ligera de algunos textos


**4. Análisis**

Se generaron conteos y agrupaciones:

  - Cantidad de contenedores por tipo

  - Conteo de contenedores por barrio

  - Preparación de datos para las gráficas

**Finalmente, se creó una figura con tres gráficos en un solo panel:** 

  1. Cantidad por tipo de contenedor

  2. Barrios con mayor cantidad de contenedores

  3. Distribución porcentual por tipo (gráfico de pastel)

-------------------------------------------

### Contribución a los ODS

- **Indicador 9.1.1 – Acceso a infraestructura sostenible**

  - **Definición ODS:** Proporción de la población que vive cerca de infraestructuras adecuadas.

**Aplicación en el proyecto:**

  - Distribución desigual de contenedores y puntos limpios entre los 21 distritos de Madrid.

  - Identificación de distritos con menor cobertura de infraestructura de reciclaje.


**Resultado:**
  - Se evidencia una brecha territorial en el acceso a infraestructura de reciclaje, afectando especialmente a distritos socialmente vulnerables, lo que limita la participación ciudadana y la eficiencia del sistema 

------------------------------------------------

- **Indicador 9.4.1 – Eficiencia en el uso de recursos**

  - **Definición ODS:** Fomento del uso de tecnología, investigación y datos para mejorar procesos.

**Aplicación en el proyecto:**

  - Uso de Python, Pandas y Plotly para análisis de grandes volúmenes de datos (2018–2025).

  - Desarrollo de un dashboard interactivo en Streamlit.

**Resultado:**
  - El proyecto demuestra que el uso de herramientas tecnológicas mejora la toma de decisiones basada en datos, permitiendo detectar ineficiencias, desigualdades territoriales y oportunidades de innovación en la gestión de residuos.
    
-------
- **Indicador 9.5.1 – Promoción de la innovación**

  - **Definición ODS:** Emisiones y eficiencia en procesos industriales e infraestructuras.

**Aplicación en el proyecto:**

  - Análisis de impropios en fracciones reciclables (plástico, vidrio, papel/cartón).

  - Evaluación del destino final de residuos hacia Valdemingómez.


**Resultado:**
  - Las altas tasas de impropios reducen la eficiencia del reciclaje y provocan un mayor envío de residuos a vertedero, aumentando costos operativos y el impacto ambiental del sistema

---
- **Indicador 9.b.1 – Desarrollo sostenible e industrial**

  - **Definición ODS:** Apoyo a industrias sostenibles y economía circular.

**Aplicación en el proyecto:**

  - Análisis del potencial de recuperación de materiales con valor económico (PET, aluminio, cartón).

  - Relación con empleos verdes y sector reciclador.

**Resultado:**
  - La baja valorización de residuos limita el crecimiento de la economía circular y la generación de empleos verdes, evidenciando la necesidad de fortalecer la infraestructura y la educación ambiental.

---

## Conclusión

- El análisis realizado evidencia que la gestión de residuos en la Comunidad de Madrid enfrenta importantes desafíos vinculados a la falta de infraestructura homogénea, la elevada presencia de impropios y la limitada participación ciudadana. Estas brechas generan presión sobre instalaciones como Valdemingómez, incrementan los costos operativos y reducen la eficiencia del reciclaje, afectando directamente los objetivos del ODS 9. El uso de tecnologías como Python, Pandas, Plotly y Streamlit permitió identificar desigualdades territoriales, zonas críticas y oportunidades de innovación que pueden fortalecer la economía circular. En conjunto, el proyecto demuestra que una gestión inteligente basada en datos es esencial para construir infraestructuras más resilientes, sostenibles y accesibles, promoviendo así una ciudad más eficiente, equitativa y comprometida con el desarrollo sostenible.


## Arquitectura del Proyecto

```
📁 proyecto-final/
│
├── data/
│   ├── Datosproyecto.csv                    # Datos originales sin procesar
│
├── notebooks/
│   ├── Proyecto.ipynb                       # Programación y análisis final de los datos
│
└── README.md                                # Este archivo
```

---

## Agradecimientos

- **Tech Horizons** por la oportunidad de aprender ciencia de datos
- **Portal de datos abiertos del Ayuntamiento de Madrid** por proporcionar datos abiertos
- **Comunidad open source** por las herramientas utilizadas.

---

**¡Gracias por revisar nuestro proyecto!**

*Hecho por el equipo Circular Madrid*
