Más idiomas: <kbd>[<img title="Leer en inglés" alt="Leer en inglés" src="https://cdn.staticaly.com/gh/hjnilsson/country-flags/master/svg/gb.svg" height="15">](translations/README.en.md)</kbd>  &emsp;
Seguime en <kbd>[<img title="Mi perfil en LinkedIn" alt="Mi perfil en LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" height="15">](https://www.linkedin.com/in/martinezjesusfl/)</kbd>

# Proyecto GDELT (Global Database of Events, Language, and Tone)
**Tecnologías usadas:**  
<img title="Python" alt="Python" src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue" height="20"> &emsp;
<img title="Terraform" alt="Terraform" src="https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" height="20"> &emsp;
<img title="DBT" alt="DBT" src="https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white
" height="20"> &emsp;
<img title="Prefect" alt="Prefect" src="https://img.shields.io/badge/Prefect-5772b0?style=for-the-badge&logo=?logoColor=white" height="20"> &emsp; 
<img title="Google Cloud" alt="Google Cloud" src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white
" height="20"> &emsp;

## Index
- [Introducción](#introducción)
- [Contexto](#contexto)
- [Contenidos](#contenidos)
- [Instrucciones](#instrucciones)

## Introducción
Este proyecto de ELT (Extract, Load, Transform) toma los datasets de [GDELT](https://www.gdeltproject.org/), los almacena en Google Cloud Storage y los procesa en Google BigQuery transformánodolos con DBT Cloud para que puedan ser analizados a través de Looker Studio.  
Para conocer más sobre los fundamentos de las herramientas usadas están disponibles el [Data Engineering Zoompcamp](https://youtube.com/playlist?list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb), y mis notas personales de cada módulo en el repositorio [Data Engineering Bootcamp](https://github.com/Jebushdd/Data-Engineering-Bootcamp).

## Contexto
GDELT (Global Database of Events, Language, and Tone) es una base de datos global de eventos y noticias que se actualiza constantemente. GDELT monitorea noticias y eventos en todo el mundo y los recopila en una base de datos accesible al público. La base de datos contiene información sobre eventos, personas, lugares y organizaciones, y utiliza técnicas de procesamiento del lenguaje natural (NLP) para analizar el tono y la emoción de los artículos de noticias. GDELT es utilizado por investigadores, periodistas y organizaciones en todo el mundo para analizar patrones y tendencias en noticias y eventos globales.

## Contenidos
- ```0_environment_setup``` La carpeta con los comandos para crear nuestro ambiente de trabajo e instalar los requerimientos necesarios.
- ```1_infrastucture``` La carpeta con un script de Terraform y los comandos para crear nuestra infraestructura en Google Cloud.
- ```2_pipeline``` La carpeta con el script para crear y correr el pipeline de Extracción y Carga de datos usando Prefect.
- ```3_transformation``` La carpeta con el procedimiento para transformar los datos usando DBT y dejarlos listos para su análisis.
- ```4_dashboard_connection``` La carpeta con el procedimiento para conectar la base de datos a Looker Studio.

## Instrucciones