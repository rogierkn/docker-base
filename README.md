### Basic PHP Docker setup

Very basic Docker setup that runs NGINX, PHP (7.1.1), and MySQL (5.7).  

Default config assumes:
* the folder containing ``docker-compose.yml`` is the project root
* root has a ``public`` folder containing the entry point of your application


Configure the MySQL database through a dotenv (``.env``) file in your project root.
````text
DB_PASSWORD=mysql_password
DB_DATABASE=database
````
Your application can then connect as the ``root`` user using your set password on the set database.  
The database is persisted to the ``./database`` folder.

Start the containers the default way with ``docker-compose up -d`` and shut them down them with ``docker-compose down``

