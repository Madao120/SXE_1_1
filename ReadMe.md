| Elemento | Lo que dice la documentación | Lo que necesita la VM | Otros | Fuentes de info |
| :--- | :--- | :--- | :--- | :--- |
| **S.O.** | Cualquiera mientras tenga los requisitos de S.W. y BD | Ubuntu Server 26.04.1 | La escogí debido a el uso por terminal para no gastar en recursos | \* |
| **Servidor Web** | Nginx o Apache con el módulo `mod_rewrite` | Apache2 | Lo escogí debido a que había visto su funcionalidad en años anteriores | \* |
| **Versión PHP** | Versión 8.3 o superior. | 8.5.4 | Escogí esta version debido a que es la que me indicaba la guía de ubuntu **| NGXNB\* |
| **Gestor de BD** | MariaDB 10.11+ o MySQL 8.0+. | MySQL 8.4.11 | Escogí esta version debido a que es la que me indicaba la guía de ubuntu **| \* |
| **Memoria y Disco** | 1GB | 5GB | Debido al SO entre otros programas decidí darle más espacio | [WPBeginner](https://www.wpbeginner.com/es/beginners-guide/important-wordpress-server-requirements-you-should-know/) |

---

### "Leyenda" de la tabla

* *: [Requisitos Oficiales de WordPress](https://es.wordpress.org/about/requirements/)
* **: WordPress aún funciona con PHP 7.4+ y MySQL 5.5.5+, pero esas versiones han llegado a su fin de ciclo oficial y podrían exponer tu sitio a vulnerabilidades de seguridad.

### Realicé la máquina virtual en instalación desatendida

### 1. Dentro de la propia máquina virtual instalamos apache
![imagen apt install apache](/capturas/1Insatlacion_Apache2.png)

### 2. Aquí mostramos la instalación de Mysql, también instalé php, me olvidé de sacar foto pero lo realicé con este comando de la página de ubuntu
sudo apt update
sudo apt install php \
php-bcmath \
php-curl \
php-imagick \
php-intl \
php-json \
php-mbstring \
php-mysql \
php-xml \
php-zip
![imagen apt install mysql y php](/capturas/2Instalación_Mysql.png)

### 3. Aquí observamos como se instala wordpress desde terminal, utilizando curl
![imagen wordpress install con curl](/capturas/3%20Instalación%20wordpress.png)

### 4. Configuramos el wordpress.conf
![imagen wordpress.conf](/capturas/4%20Configuración%20Apache.png)

### 5. Habilitamos el site y la reescritura mientras deshabilitamos el .conf defaut del sistema
![imagen e2enable wordpress.conf](/capturas/5%20Habilitar%20el%20conf.png)

### 6. Configuramos la Base de Datos de mysql para que se sincronice con wordpress
![imagen mysql](/capturas/6%20Creación%20de%20la%20base%20de%20datos.png)

### 7. Copiamos el archivo de ejemplo de php para poder modificarlo con nuestros datos
![imagen wp-config.php](/capturas/7%20configuracion%20de%20php.png)

### 8. Modificamos el archivo php ligado a wordpress para poner nuestras cerenciales y la base de datos
![imagen wp.config.php parte 2](/capturas/8%20nano%20.png)

### 9. Página de instalación de Wordpress desde nuestro dispositivo
![imagen instalación wordpress](/capturas/09%20wordpress.png)

### 10. Introducimos las credenciales que escribimos en el archivo wp-config.php
![imagen credenciales wordpress](/capturas/10%20datos%20instalacion.png)

# 11. Página iniciada de Wordpress funcional en nuestro dispositivo
![imagen inicio wordpress](/capturas/11%20Wordpress%20Funcional.png)