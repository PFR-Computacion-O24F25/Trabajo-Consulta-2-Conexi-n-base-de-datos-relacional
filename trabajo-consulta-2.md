## Conexión a Base de Datos Relacional

### 1.¿Qué es JDBC y cuáles son sus componentes?

JDBC (Java Database Connectivity) es una API (Interfaz de Programación de Aplicaciones) que permite a los desarrolladores de software conectar sus aplicaciones Java con bases de datos relacionales. En pocas palabras, JDBC actúa como un puente que facilita la comunicación entre una aplicación Java y una base de datos, permitiendo la ejecución de consultas y la manipulación de datos de manera eficiente.

Las bases de datos relacionales almacenan la información en tablas que se relacionan entre sí. Cuando una aplicación Java necesita acceder a los datos almacenados en una base de datos relacional, utiliza JDBC para establecer una conexión con la base de datos, enviar consultas SQL y procesar los resultados obtenidos.

#### Componentes principales de JDBC:

- **API JDBC**: Un conjunto de interfaces y clases que definen cómo las aplicaciones Java interactúan con las bases de datos.
- **Controlador**: Un controlador específico para un SGBD particular que implementa las interfaces y maneja la comunicación entre la aplicación y la base de datos.
- **Driver JDBC**: Un controlador que permite la conexión a una base de datos específica.
- **Conexión**: Una conexión a la base de datos que permite enviar consultas y recibir resultados.
- **Consulta SQL**: Instrucciones SQL utilizadas para interactuar con la base de datos.
- **Statement**: Una sentencia SQL preparada o una declaración para ejecutar en la base de datos.

---

## 2. Librerías de Scala para Conexión a Bases de Datos Relacionales

A continuación, se presentan dos librerías populares de Scala para conectarse a bases de datos relacionales:

### * **Slick**
Slick es una librería orientada a objetos, con un enfoque de ORM (Object-Relational Mapping). Esto significa que puedes usar modelos de datos de Scala para representar tus tablas y consultas de base de datos, facilitando la manipulación de datos con un enfoque más declarativo.

### * **Doobie**
Doobie es una librería más cercana al estándar JDBC, pero con un enfoque funcional. Se enfoca en usar SQL puro, lo que te da un mayor control sobre las consultas y transacciones, sin las abstracciones de un ORM.

---

### Resumen de las Diferencias

| **Característica**            | **Slick**                                                   | **Doobie**                                                   |
|-------------------------------|-------------------------------------------------------------|-------------------------------------------------------------|
| **Enfoque**                    | ORM (Object Relational Mapping)                             | Funcional, basada en JDBC, sin ORM                          |
| **Manejo de conexiones**       | Abstracción completa de la conexión y gestión de la base de datos | Manejo explícito de conexiones y transacciones               |
| **Lenguaje de consultas**      | DSL (Domain Specific Language) para consultas SQL           | SQL puro, con soporte para composición funcional de consultas |
| **Tipos de datos**             | Soporte completo para tipos de datos Scala y SQL             | Uso de tipos de datos JDBC estándar, sin mapeo directo a objetos |
| **Integración con Scala**      | Bien integrado con las características del lenguaje Scala   | Más "puro" y funcional, sin muchas abstracciones sobre Scala |
| **Tamaño de la comunidad**     | Gran comunidad, bastante popular en proyectos de Scala      | Menor comunidad, pero cada vez más adoptado por usuarios que prefieren un enfoque más funcional |
| **Manejo de errores**          | Manejo de errores mediante `Try`, `Future` y `Option`        | Manejo de errores mediante `Either` y `Option`, enfoque funcional |
| **Configuración y uso**        | Requiere configuración más detallada, pero proporciona más abstracción | Requiere más código explícito, pero es más flexible y controlado |
| **Soporte para transacciones** | Transacciones mediante combinaciones de `Future` y `DBIO`   | Transacciones explícitas con control más fino sobre el ciclo de vida de la conexión |
| **Soporte para bases de datos**| Compatible con PostgreSQL, MySQL, SQLite, H2 y más          | Compatible con PostgreSQL, MySQL, H2, y otras bases de datos JDBC |

---

### Conclusión

- **Slick** es ideal si prefieres un enfoque más declarativo con un ORM para manejar tus interacciones con bases de datos. Es muy popular en proyectos de Scala y se integra bien con el lenguaje.
  
- **Doobie** es perfecto para quienes buscan un enfoque más funcional y directo al trabajar con bases de datos, utilizando SQL puro y control total sobre la conexión y transacciones.

### Referencias

- definición-de-jdbc. (s. f.). ProgramaciónPro. Recuperado 23 de enero de 2025, de https://programacionpro.com/que-es-jdbc-en-base-de-datos-y-por-que-es-importante/

- explicación jdbc. (s. f.). TechEdu. Recuperado 23 de enero de 2025, de https://techlib.net/techedu/jdbc/

- Funcionalidades de JDBC. (s. f.). Data Sunrise. Recuperado 23 de enero de 2025, de https://www.datasunrise.com/es/centro-de-conocimiento/que-son-odbc-y-jdbc/

- Uso y codificación a través de JDBC. (s. f.). Decodigo. Recuperado 23 de enero de 2025, de https://decodigo.com/java-conexion-a-base-de-datos-con-jdbc

