# Smart Wardrobe - Deploy a Producció 👕

Projecte de finalització del mòdul M12 (Síntesi) del CFGS Sistemes Microinformàtics i Xarxes (SMX) - Institut Camí de Mar.

## 👥 Rol de l'Equip: TEAM (Desenvolupament tècnic)
Ens hem encarregat de la implementació tècnica i la pujada a producció basant-nos en els requisits de l'equip Product Owner.

## 🚀 Infraestructura i Stack Tecnològic
* **Hosting:** AWS EC2 (Ubuntu Server 22.04 LTS)
* **IP Pública:** 54.165.56.73
* **Stack:** LAMP (Apache2, MariaDB, PHP 8.1)
* **CMS:** WordPress

## 📦 Procés de Desplegament
1. Transferència d'arxius (`.tar.gz`) via SCP i extracció a `/var/www/html/`.
2. Creació de la base de dades i importació de l'arxiu `.sql`.
3. Sincronització de l'arxiu `wp-config.php` amb credencials de producció.
4. Actualització de les variables `siteurl` i `home` a la base de dades cap a la nova IP.
5. Ajust de permisos d'Apache (`www-data`).