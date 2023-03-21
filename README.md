# Nginx

#### Go to file config

```shell
cd /etc/nginx/sites-available/
```

#### View file config (make sure you are in path `/etc/nginx/sites-available/`)

```shell
cat default
```

#### Edit

```shell
sudo nano default
```

#### After done editing make sure you restart the Nginx service

```shell
sudo systemctl restart nginx.service
```

# Docker

#### List all running containers

```shell
docker ps
```

#### List all running and exited containers

```shell
docker ps -a
```

#### View the console of container

```shell
docker logs -f --tail 500 <container name>
```

#### Stop running container

```shell
docker stop <container name>
```

#### Restart container

```shell
docker restart <container name>
```

#### Clear all exited image

```shell
docker system prune -a
```

# Jenkens

#### When build containers with jenkins and have problem: `cannot connect to docker daemon` run command below:

```shell
restart docker
sudo chmod 666 /var/run/docker.sock
```

# Create cert with openssl rsa sha256
### cd to directory that you want to put your cert files in
```shell
openssl rsa -in private.pem -pubout -out public.pem
```

# Connect MYSQL
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'allweb17';
FLUSH PRIVILEGES;
```
