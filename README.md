Aaron Federico Alonso Torres 200617 10B IDGS 🐸

¡Hola! mi aplicacion es una API REST CRUD escrita en Go que utiliza un ORM llamado GORM para interactuar con una base de datos MySQL. La API REST permite realizar las operaciones CRUD (Create, Read, Update, Delete) en la tabla `users` de la base de datos.

Aquí hay una descripción de cada parte del programa:

1. "main.go": Este archivo es el punto de entrada del programa. Define las rutas para la API REST y configura el servidor web Gin.

2. "User": Este struct define el modelo `User` que se utiliza para interactuar con la tabla `users` en la base de datos.

3. "db, err := gorm.Open(mysql.Open(dsn), &gorm.Config{})": Esta línea de código establece una conexión a la base de datos MySQL utilizando GORM.

4. "db.AutoMigrate(&User{})": Esta línea de código ejecuta las migraciones necesarias para crear la tabla `users` en la base de datos.

5. "r.GET("/users", func(c *gin.Context)": Esta ruta acepta solicitudes GET y devuelve una lista de todos los usuarios en la tabla `users`.

6. "r.GET("/users/:id", func(c *gin.Context)": Esta ruta acepta solicitudes GET con un parámetro de ID y devuelve el usuario correspondiente en la tabla `users`.

7. "r.POST("/users", func(c *gin.Context)": Esta ruta acepta solicitudes POST y crea un nuevo usuario en la tabla `users`.

8. "r.PUT("/users/:id", func(c *gin.Context)": Esta ruta acepta solicitudes PUT con un parámetro de ID y actualiza el usuario correspondiente en la tabla `users`.

9. "r.DELETE("/users/:id", func(c *gin.Context)": Esta ruta acepta solicitudes DELETE con un parámetro de ID y elimina el usuario correspondiente en la tabla `users`.

Para utilizar el programa, debes seguir los siguientes pasos:

1. Instala Go en tu sistema operativo.
2. Instala XAMPP en tu sistema operativo.
3. Inicia XAMPP y asegúrate de que Apache y MySQL estén activos.
4. Abre PHPMyAdmin en tu navegador web y crea una base de datos llamada `test`.
5. Crea una carpeta para tu proyecto y clona el repositorio del programa dentro de ella.
6. Ejecuta el siguiente comando para instalar las dependencias necesarias:

go get -u github.com/gin-gonic/gin
go get -u gorm.io/gorm
go get -u gorm.io/driver/mysql

7. Ejecuta el siguiente comando para ejecutar las migraciones:
go run migrate/migrate.go

8. Ejecuta el siguiente comando para iniciar el servidor web:
go run main.go

9. Ahora puedes probar la API REST CRUD que cree usando herramientas como Postman o curl.
Espero que esto te ayude a entender cómo funciona el programa y cómo utilizarlo. 🐸
