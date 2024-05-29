# proyecto_biblo

# RED DE BIBLIOTECAS: UNA APUESTA A LA CONEXIÓN

Gutiérrez Verano Katherin Alexandra, Castillo López Gonzalo, Poveda Girata Hugo Steven, Silva Piracoca Edwin Leonardo

{kagutierrez, g.castillol, H.Poveda, e.silva}@javeriana.edu.co

Pontificia Universidad Javeriana

Bogotá D.C.

---

## Introducción

### Resumen
Acceder a las fuentes de conocimiento ofrecidas por las bibliotecas en Bogotá puede representar un desafío, dado que no siempre se dispone de información precisa sobre la existencia de un libro o documento en una biblioteca específica, ni sobre su ubicación geoespacial. Para abordar esta necesidad, el presente documento propone una solución tecnológica que, mediante la integración de datos en diferentes formatos, permite ubicar geo-espacialmente las bibliotecas más cercanas al usuario. Esto brinda la oportunidad de identificar fácilmente la biblioteca más próxima o la que más convenga según su ubicación actual.

### Palabras claves
BD Geoespacial, BD Vectoriales, BD Relacional, Docker.

### Contexto y Alcance
La innovación tecnológica beneficiada por ecosistemas de datos abiertos ha permitido la creación de soluciones y productos que responden a necesidades públicas. Estas soluciones han integrado datos de diversos formatos y, dependiendo de los casos de negocio, han utilizado diferentes bases de datos, basados en la consistencia y disponibilidad de los datos. La iteración entre datos heterogéneos con bases de datos de diferentes fuentes ha permitido el desarrollo de proyectos de integración de datos, iniciando con la comprensión de la información almacenada, con una posterior definición de mecanismos que permitan el flujo de datos entre sistemas y la implementación de cambios de estructuras. De este proceso se obtiene información transformada para formar parte de una fuente de información, como un DWH, o presentada al usuario final como resultado de una consulta.

En este entorno de datos y ecosistemas de aplicaciones, tenemos APIS que permiten extraer datos públicos, o aplicaciones APP diseñadas para solucionar necesidades de usuarios en el comercio, educación, salud o sector financiero, con la oportunidad permanente de crear nuevas soluciones que permitan atender necesidades públicas. Este documento presenta una solución que brinda la posibilidad a los usuarios de bibliotecas de ubicar geoespacialmente la más cercana a su ubicación.

El acceso a las bibliotecas es fundamental para el uso cotidiano y su utilización como espacios de encuentro social y convivencia ciudadana. Son la unidad de información más cercana a la comunidad. En el presente proyecto se presentan los datos no solo de bibliotecas públicas de la ciudad de Bogotá, sino también bibliotecas comunitarias, BibloRed, Manzanas del Cuidado, BibloEstación y Hemerotecas de la ciudad, como espacios que tienen desafíos a la accesibilidad por el desconocimiento del público de su ubicación o de la información que en ellas se puede encontrar.

Las bibliotecas tienen servicios de búsqueda de libros digitales y físicos, consulta de tesis y proyectos de investigación, y ofrecen servicios de educación continua que involucran a estudiantes y a la comunidad. Por ello, son centros de oportunidad para el aprendizaje y de avance para personas interesadas en lectura e investigación que no pueden comprar todas las publicaciones buscadas.

En el presente proyecto se busca conectar las bibliotecas en una aplicación tecnológica a través de los datos públicos ofrecidos por la página de Datos Abiertos de Bogotá, con las herramientas de bases de datos relacionales como PostgreSQL y bases de datos geoespaciales como PostGIS. Se busca analizar la relación entre los datos de las diferentes bibliotecas, la accesibilidad geográfica, la cobertura de libros manejados, y la información de contacto que brindan, por medio de Docker Compose.


## Objetivos

### Objetivos Generales
- **Desarrollar una solución tecnológica integral** que permita a los usuarios localizar geo-espacialmente las bibliotecas más cercanas en la ciudad de Bogotá, mejorando el acceso a la información bibliográfica y geoespacial mediante el uso de datos abiertos y diversas herramientas tecnológicas.

### Objetivos Específicos

1. **Recopilación y Almacenaje de Datos**
   - Recopilar y procesar datos de diversas fuentes públicas. Estos datos serán gestionados y almacenados utilizando MinIO. Adicionalmente, se configurarán bases de datos relacionales, geoespaciales y vectoriales, ejecutadas y orquestadas dentro de Docker Compose para asegurar una ejecución coordinada y eficiente de los componentes del sistema.

2. **Desarrollo e Implementación Tecnológica**
   - Desarrollar e implementar la tecnología necesaria para la explotación de los datos. Se crearán APIs utilizando FastAPI para exponer los datos de manera eficiente y segura, y se implementará una interfaz de usuario con Streamlit que permitirá la visualización intuitiva de la información geoespacial. Se llevarán a cabo pruebas de integración y funcionamiento para asegurar la eficiencia y efectividad del sistema.

3. **Facilitación del Acceso a Información Bibliotecaria**
   - Facilitar el acceso a la información bibliotecaria, permitiendo a los usuarios consultar la ubicación de las bibliotecas más cercanas, incluyendo bibliotecas públicas, comunitarias, Biblored y Manzanas del Cuidado. Se proveerá una herramienta que facilite el acceso y el conocimiento público sobre los servicios bibliotecarios disponibles en Bogotá, mejorando así la accesibilidad y promoviendo la utilización de estos recursos valiosos para la comunidad.

## Atributos de Calidad

La calidad es fundamental en el desarrollo exitoso del aplicativo, garantizando una experiencia de usuario óptima, segura y confiable.

### Escalabilidad

- **Escalabilidad Horizontal**: La aplicación está diseñada para manejar un incremento en la cantidad de usuarios y datos distribuyendo la carga en múltiples servidores. Para manejar un aumento en la carga de trabajo, se utilizarán servicios en la nube para almacenar y procesar datos, permitiendo escalar horizontalmente agregando más instancias de servidores según sea necesario.

### Rendimiento

El tiempo de respuesta de la aplicación es crucial para proporcionar una experiencia fluida y eficiente al localizar las bibliotecas cercanas rápidamente. Como estrategias, se plantea:

- Utilización de técnicas de cacheo para almacenar temporalmente datos frecuentemente accedidos, reduciendo el tiempo de acceso.
- Optimización de consultas a la base de datos relacional para mejorar la rapidez en la recuperación de información.

### Disponibilidad

La aplicación estará disponible y operativa la mayor parte del tiempo, con mínimos tiempos de inactividad. Se implementará:

- Monitoreo continuo y alertas para detectar y resolver problemas rápidamente.

### Seguridad

Para garantizar la seguridad de los datos y la aplicación:

- No se almacenarán datos sensibles del usuario.
- Se usarán protocolos que permitan la autenticación segura y protejan las API de acceso a datos.
- Se implementará HTTPS para todas las comunicaciones entre el cliente y el servidor.

### Mantenibilidad

El código de la aplicación estará estructurado de manera que sea fácil de entender y modificar. Se incluirá:

- Documentación clara y detallada para facilitar futuras modificaciones y actualizaciones.
- La aplicación estará dividida en componentes pequeños y reutilizables, facilitando las actualizaciones y el mantenimiento.

### Confiabilidad

Se asegurará que los datos presentados sean correctos y coherentes, sin errores ni duplicados. Para ello:

- Se realizarán pruebas unitarias y de integración para garantizar que nuevas actualizaciones no introduzcan errores.
- Se mantendrán bases de datos replicadas y backups automáticos para prevenir pérdida de datos.


## Descripción de la Arquitectura

La arquitectura del sistema está diseñada para permitir a los usuarios localizar geo-espacialmente las bibliotecas más cercanas en Bogotá, integrando diversas fuentes de datos y utilizando herramientas tecnológicas avanzadas. Los datos son recolectados desde fuentes públicas en múltiples formatos (Esri REST, WMS, WFS, GPKG, GeoJSON, SHP, KML, DXF) y gestionados mediante MinIO. Estos datos se almacenan en bases de datos relacionales, geoespaciales y vectoriales, que son orquestadas y gestionadas con Docker Compose. La capa de presentación incluye APIs desarrolladas con FastAPI y una interfaz de usuario intuitiva creada con Streamlit, complementada con búsqueda semántica en bases de datos documentales.

### Diagrama de Arquitectura

El diagrama de arquitectura muestra la estructura del ecosistema, destacando los componentes principales y su interconexión.

![Arquitectura.png](imagenes/Arquitectura.png)

### Componentes

#### Fuentes de Datos y Bibliotecas (ETL - Ingesta)
- **MinIO**: Un sistema de almacenamiento distribuido utilizado para gestionar y almacenar grandes volúmenes de datos recolectados. Almacena archivos en formatos Esri REST, WMS, WFS, GPKG, GeoJSON, SHP, KML, DXF, los cuales son diferentes formatos de datos geoespaciales y bibliográficos recolectados desde diversas fuentes públicas.

#### Sistema de Almacenaje de Información
- **BD Relacional**: PostgreSQL almacena datos estructurados en un formato relacional, proporcionando una base sólida y robusta para la gestión de datos en libros y bibliotecas.
- **BD Geoespacial**: PostGIS, como extensión de PostgreSQL, maneja datos geoespaciales necesarios para la localización precisa de las bibliotecas, permitiendo consultas y análisis espaciales avanzados.
- **BD Vectorial**: PostgreSQL también almacena datos vectoriales utilizados para representar objetos en un espacio geográfico, facilitando el manejo y análisis de datos vectoriales.
- **BD Documental**: MongoDB, una base de datos de documentos que ofrece gran escalabilidad y flexibilidad, y un modelo de consultas e indexación avanzado. Como ejercicio académico y complemento en el desarrollo del proyecto, el aplicativo se conecta a MongoDB para búsquedas semánticas.
- **Docker Compose**: Orquestador de contenedores utilizado para desplegar y gestionar los distintos componentes del sistema, asegurando su ejecución coordinada y eficiente.

#### Presentación
- **FastAPI**: Utilizado para desarrollar APIs que exponen los datos de manera eficiente y segura, facilitando la interacción con los datos almacenados y proporcionando un acceso rápido y estructurado a la información.
- **React**: Librerías de JavaScript utilizada en el desarrollo de la aplicación. 


### Flujo de Datos

El diagrama de flujo muestra el movimiento de datos desde las fuentes hasta la presentación final al usuario.

![Flujo.jpg](imagenes/Flujo.jpg)

## Tecnologías Utilizadas

- **MinIO**: Utilizado para gestionar y almacenar grandes volúmenes de datos en diversos formatos.

- **PostgreSQL**: Base de datos relacional utilizada para almacenar datos estructurados.

- **PostGIS**: Extensión de PostgreSQL para manejar datos geoespaciales.

- **Docker Compose**: Orquestador de contenedores utilizado para la implementación y gestión coordinada de los componentes.

- **FastAPI**: Framework para el desarrollo de APIs eficientes y seguras.

- **React**: Biblioteca de JavaScript para desarrollar interfaces de usuario intuitivas y dinámicas.

- **MongoDB**: Base de datos documental de fácil y rápida indexación, muy eficiente en procesos de búsquedas semánticas. Como valor agregado al proyecto, se realiza a través del front una búsqueda de palabras existentes en la base de datos de MongoDB.

- **Python**: Lenguaje de programación utilizado para el desarrollo del backend y procesamiento de datos.

- **Java**: Lenguaje de programación utilizado para la implementación de algunos servicios backend.

- **SQL**: Lenguaje de consulta utilizado para interactuar con bases de datos relacionales.

- **NoSQL**: Modelo de base de datos utilizado para almacenar datos no estructurados y de fácil escalabilidad.

## Configuración e Instalación

### MinIO

1. **Instalar Docker**:
   - Asegúrate de tener Docker instalado en el sistema. Puedes instalar Docker desde [Docker Hub](https://hub.docker.com/) o manejarlo mediante Visual Studio Code.

2. **Descargar la imagen de MinIO**:
   - Usa el siguiente comando para descargar la imagen de MinIO:
     ```bash
     docker pull minio/minio
     ```

3. **Configurar y ejecutar MinIO**:
   - Configura MinIO con credenciales personalizadas y ejecuta el contenedor:
     ```bash
     docker run -p 9000:9000 --name minio \
       -e "MINIO_ACCESS_KEY=youraccesskey" \
       -e "MINIO_SECRET_KEY=yoursecretkey" \
       minio/minio server /data
     ```

### PostgreSQL con PostGIS

1. **Descargar la imagen de PostgreSQL con PostGIS**:
   - Usa el siguiente comando para descargar la imagen de PostgreSQL con PostGIS:
     ```bash
     docker pull postgis/postgis
     ```

2. **Configurar y ejecutar PostgreSQL con PostGIS**:
   - Configura PostgreSQL con credenciales personalizadas y ejecuta el contenedor:
     ```bash
     docker run -p 5432:5432 --name postgis \
       -e POSTGRES_USER=yourusername \
       -e POSTGRES_PASSWORD=yourpassword \
       postgis/postgis
     ```

3. **Acceder a PostgreSQL con PostGIS**:
   - Utiliza un cliente o herramienta gráfica como pgAdmin para acceder a PostgreSQL con PostGIS.

### Docker Compose

1. **Crear un archivo `docker-compose.yml`**:
   - Crea un archivo `docker-compose.yml` con la configuración de los servicios necesarios:
     ```yaml
     version: '3.8'
     services:
       minio:
         image: minio/minio
         ports:
           - "9000:9000"
         environment:
           MINIO_ACCESS_KEY: youraccesskey
           MINIO_SECRET_KEY: yoursecretkey
         command: server /data

       postgis:
         image: postgis/postgis
         ports:
           - "5432:5432"
         environment:
           POSTGRES_USER: yourusername
           POSTGRES_PASSWORD: yourpassword
     ```

2. **Ejecutar Docker Compose**:
   - Ejecuta el siguiente comando en la terminal para iniciar los servicios definidos en `docker-compose.yml`:
     ```bash
     docker-compose up -d
     ```

### FastAPI

1. **Instalar FastAPI**:
   - Usa pip para instalar FastAPI y Uvicorn:
     ```bash
     pip install fastapi uvicorn
     ```

2. **Crear una aplicación FastAPI**:
   - Crea un archivo `main.py` y define tu aplicación FastAPI:
     ```python
     from fastapi import FastAPI

     app = FastAPI()

     @app.get("/")
     def read_root():
         return {"Hello": "World"}

     if __name__ == "__main__":
         import uvicorn
         uvicorn.run(app, host="0.0.0.0", port=8000)
     ```

3. **Ejecutar la aplicación FastAPI**:
   - Ejecuta el siguiente comando para iniciar el servidor de desarrollo:
     ```bash
     uvicorn main:app --reload
     ```

### React

1. **Instalar Node.js y npm**:
   - Asegúrate de tener Node.js y npm instalados en tu sistema. Puedes descargarlos desde [Node.js](https://nodejs.org/).

2. **Crear una aplicación React**:
   - Usa el siguiente comando para crear una nueva aplicación React:
     ```bash
     npx create-react-app my-app
     ```

3. **Iniciar la aplicación React**:
   - Navega al directorio de tu aplicación y ejecuta el servidor de desarrollo:
     ```bash
     cd my-app
     npm start
     ```

### Conclusión

Siguiendo estos pasos, habrás configurado y ejecutado los componentes principales de tu aplicación, incluyendo MinIO, PostgreSQL con PostGIS, Docker Compose, FastAPI y React. Asegúrate de personalizar las credenciales y configuraciones según tus necesidades específicas.



