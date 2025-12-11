# Docker
---
Para el docker he decidido levantarlo con un docker-compose, me parece una manera más práctica y organizada de levantar y mantener los contenedores
Los comandos usados fueron los siguientes

**Para la instalación de docker**
```
sudo apt install docker.io -y
sudo apt install docker-compose -y
```

**El código**
```
services:
  nginx:
    image: nginx:latest
    container_name: PPSUnidad0-Tarea_Ismael
    ports:
      - "8085:80"
    volumes:
      # Monta la carpeta local con el contenido de gh-pages en /usr/share/nginx/html
      - .:/usr/share/nginx/html:ro
    restart: unless-stopped
```

El resultado final después de levantar el docker y acceder a la web por el puerto deseado fue el siguiente:
![Resultado](img/CAP14.png)
