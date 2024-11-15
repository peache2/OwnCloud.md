# Instalación de OwnCloud

###### *Para instalar la cloud necsitamos descargar el archivo que he dejado en el README*

## Instalamos la versión 7.4 de PHP en el sistema operativo Ubuntu 24.04

Para instalar correctamente OwnCloud necesitamos la versión 7.4 de PHP, para  instalar en nuestro sistema debemos poner los siguientes comandos en la terminal:

Actualizamos las listas de paquetes y actualizamos todos los paquetes del sistema-. 

### **1. Instalamos los requisitos previos de PPA:**
```bash
sudo apt install software-properties-common -y
```

### **2. Instalamos las herramientas necesarias para trabajar correctamente con archivos personales (PPA).**
```bash
LC_ALL=C.UTF-8 sudo add-apt-repository ppa:ondrej/php -y
```

### **3. Actualizamos los repositorios:**
```bash
sudo apt update
```

### **4. Instalamos la libreria de PHP de la versión 7.4**
```bash
sudo apt install php7.4 -y
```
```bash
sudo apt install -y php libapache2-mod-php7.4
```

```bash
sudo apt install -y php7.4-fpm php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-gd php7.4-xml php7.4-intl php7.4-mysql php7.4-cli php7.4-ldap php7.4-zip php7.4-curl
```

### **5. Seleccionamos la versión de PHP que nosotros queremos:**
```bash
sudo update-alternatives --config php
```

### **6. Activamos los modulos de apache2 necesarios:**
```bash
sudo a2enmod proxy_fcgi setenvif
```

```bash
sudo a2enconf php7.4-fpm
```

### **7. Reiniciamos el apache2:**
```bash
sudo service apache2 restart
```
[*SIGUIENTE PASO*](https://github.com/peache2/OwnCloud.md/blob/main/aplicaci%C3%B3n-web.md)
