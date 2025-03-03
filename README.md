<center><h1>Sistema de Gestión de Biblioteca</h1></center>
<center>Proyecto final desarrollado para la asignatura Base de Datos I, en colaboración con un equipo de cuatro integrantes.   

El sistema permite la gestión integral de una biblioteca, incluyendo el registro, modificación, consulta y eliminación de: usuarios, libros, préstamos y pagos. Para su implementación, diseñamos y administramos una base de datos <b>MySQL</b> y desarrollamos una aplicación de consola utilizando el lenguaje de programación <b>Python</b>.</center>

## Modo de uso
*Descargar el repositorio:* Puedes clonarlo mediante Git, o descargarlo en formato ZIP y luego extraerlo en una carpeta.    
*Configurar la base de datos:* Crea una base de datos local en MySQL e importa el código SQL del archivo "codigoSQL.sql".    
*Ejecutar:* Al ejecutarlo, te pedirá algunos datos (como usuario, contraseña y nombre de la base de datos) para establecer la conexión. Si la conexión es exitosa, ¡ya puedes comenzar a usar el programa! 
<br><br>

1. **Archivo codigoSQL.sql**  
 Este archivo contiene:  
 - Creación de la Base de Datos: Define la base BDbiblioteca y sus tablas principales: Usuarios, Libros, Préstamos, y Pagos.
 - Esquema Normalizado: Las tablas están normalizadas al menos hasta la 3NF, eliminando redundancias y asegurando la integridad de los datos.
 - Restricciones de Integridad: Se definen llaves primarias (Id) y restricciones como NOT NULL y valores predeterminados (por ejemplo, EstadoCuota para los usuarios).
 - Estructura Relacional: Las tablas están diseñadas con relaciones adecuadas para reflejar los casos de uso del sistema, como la conexión entre Usuarios y Préstamos.
 - Compatibilidad con Operaciones Avanzadas: Proporciona una base para implementar operaciones con JOIN, índices, y procedimientos almacenados necesarios.
2. **Archivo menu.py**  
 Implementa el menú CLI, ofreciendo una interfaz interactiva que permite:
 - Gestión de Usuarios: Agregar, ver, actualizar y eliminar usuarios.
 - Gestión de Libros: Registrar, editar y eliminar libros.
 - Manejo de Préstamos: Incluye opciones para calcular multas por retrasos.
 - Reporte de Morosos: Lista usuarios con cuotas pendientes, utilizando datos de la base de datos.
 - Modificación de Cuotas: Ajusta el valor de las cuotas mensuales según las necesidades.
3. **Archivo conexion.py**  
 Este archivo gestiona la conexión con la base de datos MySQL mediante mysql.connector.
 - Módulo Centralizado: Facilita la reutilización de la lógica de conexión en todos los módulos del proyecto.
 - Operaciones Robustas: Incluye métodos para conectar y desconectar la base de datos, asegurando un manejo adecuado de recursos.
4. **Archivo tablasDBdiagram.io.png**  
 La imagen del diseño de la base de datos proporciona:
 - Esquema Visual: Representa las entidades principales, sus relaciones, y las cardinalidades, facilitando la comprensión del modelo.
 - Soporte para Desarrollo: Permite verificar que el diseño cumple con los principios de normalización y las relaciones necesarias para las operaciones exigidas.
5. **Carpeta entidades**  
 Contiene módulos para manejar las entidades clave del sistema (Libro, Usuario, Préstamo, Pago).
