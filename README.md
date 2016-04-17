# iridium-dashboard
Browser based dashboard for the [iridium-toolkit](https://github.com/muccc/iridium-toolkit) built with Flask, Websockets, MySQL and Charts.js

![iridium-dashboard](https://raw.githubusercontent.com/devnulling/iridium-dashboard/master/images/dashboard.png)

### Requisites

 * Python (2.7)
 * Flask
 * Flask-SocketIO
 * Flask-MySQL
 * Gevent 
 * MySQL
 

#### Install MySQL

    sudo apt-get install mysql-server mysql-client libmysqlclient-dev
    sudo mysql_install_db
    sudo mysql_secure_installation

#### Install Requisites

    sudo pip install flask flask-socketio flask-mysql flask-mysqldb gevent 

#### Login & Create MySQL Database

    mysql -uroot -p 
    create database iridium;

#### Create MySQL User

    CREATE USER 'iridium'@'%' IDENTIFIED BY 'password';
    GRANT ALL PRIVILEGES ON iridium.* TO 'iridium'@'%';
    FLUSH PRIVILEGES;

#### Create Iridium Table

    mysql -u<user> -p<password> iridium < iridium.sql

#### Edit 
Edit app.py with password set for mysql iridium user

#### Start
Start the dashboard by running 

    python app.py

Enable the dashboard from extractor.py with the -x flag, set host or port with -y or -z flags (default is localhost:5000)

    extractor.py -x True -y localhost -z 5000
