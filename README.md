# proyecto_biblo

# RED DE BIBLIOTECAS: UNA APUESTA A LA CONEXIÓN 

Gutiérrez Verano Katherin Alexandra, Castillo López Gonzalo, Poveda Girata Hugo Steven, Silva Piracoca Edwin Leonardo 

{kagutierrez, g.castillol, H.Poveda, e.silva} }@javeriana.edu.co

Pontificia Universidad Javeriana 

Bogotá D.C. 

---

## Introducción
- **Resumen:** Acceder a las fuentes de conocimiento ofrecidas por las bibliotecas en Bogotá puede representar un desafío, dado que no siempre se dispone de información precisa sobre la existencia de un libro o documento en una biblioteca específica, ni sobre su ubicación geoespacial. Para abordar esta necesidad, el presente documento propone una solución tecnológica que, mediante la integración de datos en diferentes formatos, permite ubicar geo-espacialmente las bibliotecas más cercanas al usuario. Esto brinda la oportunidad de identificar fácilmente la biblioteca más próxima o la que más convenga según su ubicación actual.

  
- **Palabras claves:** BD Geoespacial, BD Vectoriales, BD Relacional, BD Geoespacial,  Docker.

- **Contexto y Alcance :** La innovación tecnológica beneficiada por ecosistemas de datos abiertos ha permitido la creación de soluciones y productos que responden a necesidades públicas.  Estas soluciones han integrado datos de diversos formatos, y dependiendo los casos de negocio han utilizado diferentes bases de datos, basados en la consistencia y disponibilidad de los datos.   La iteración entre datos heterogéneos con bases de datos de diferentes fuentes ha permitido el desarrollo de proyectos de integración de datos, iniciando con la comprensión de la información almacenada, con una posterior definición de mecanismos que permitan el flujo de datos entre sistemas y con implementación de cambios de estructuras.  De este proceso se obtiene información transformada para formar parte de una fuente de información ejemplo DWH o presentada al usuario final, como resultado de una consulta. 
En este entorno de datos y ecosistemas de aplicaciones, tenemos a la orden del día APIS que permiten extraer datos públicos, o aplicaciones APP diseñadas para solucionar necesidades de usuarios en el comercio, educación, salud o sector financiero, y con la oportunidad permanente de crear nuevas soluciones que permitan atender necesidades públicas, como es el caso presentado en este documento, con el cual se brinda la posibilidad a los usuarios de bibliotecas de ubicar geo espacialmente la más cercana a su ubicación. 
El acceso a las bibliotecas es fundamental para el uso cotidiano y su utilización como espacios de encuentro social y convivencia ciudadana, son la unidad de información más cercana a la comunidad. En el presente proyecto se presentan los datos no solo de bibliotecas públicas de la ciudad de Bogotá, sino también bibliotecas comunitarias, BibloRed, manzanas del cuidado, BibloEstación y Hemerotecas de la ciudad. como espacios que tienen desafíos a la accesibilidad por el desconocimiento del público de su ubicación o de la información que en ellas se puede encontrar. 
Las bibliotecas tienen servicios de búsqueda de libros digitales y físicos, consulta de tesis y proyectos de investigación, ofrecen servicios de educación continua que involucran a estudiantes y a la comunidad, por ello son centros de oportunidad para el aprendizaje y de avance para personas interesadas en lectura e investigación que no pueden comprar todas las publicaciones buscadas.
En el presente proyecto se busca conectar las bibliotecas en una aplicación tecnológica a través de los datos públicos ofrecidos por la página de Datos Abiertos de Bogotá, con las herramientas de bases de datos relacionales como PostgreSQL, bases de datos geoespaciales como PostGIS. Buscando analizar la relación entre los datos de las diferentes bibliotecas, la accesibilidad geográfica, la cobertura de libros manejados, y la información de contacto que brindan por medio de Docker Compose.

## Objetivos
- **Objetivos Generales:** Desarrollar una solución tecnológica integral que permita a los usuarios localizar geo-espacialmente las bibliotecas más cercanas en la ciudad de Bogotá, mejorando el acceso a la información bibliográfica y geoespacial mediante el uso de datos abiertos y diversas herramientas tecnológicas.  
- **Objetivos Específicos:** Metas más detalladas y específicas que se deben cumplir para alcanzar los objetivos generales.

