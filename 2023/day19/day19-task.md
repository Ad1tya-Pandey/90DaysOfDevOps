# Day19 - Tasks

## Task - 1

### `docker-compose.yaml` file
```
version: '3.8'
services:
  app:
    image: node:18-alpine
    command: sh -c "npm install && npm run dev"
    ports: 
      - 3000:3000
    working_dir: /app
    volumes:
      - ./:/app
    env_file:
      - .env
  mysql:
    image: mysql:8.0
    volumes:
      - todo-mysql-data:/var/lib/mysql
    env_file:
      - .env

volumes:
  todo-mysql-data:

```
- Commands: `docker-compose up` , `docker-compose ps`, `docker-compose logs` , `docker-compose down`
- ![Screenshot 2023-01-20 at 11 19 35 PM](https://user-images.githubusercontent.com/101057601/213779805-144b5dfe-9fa2-4689-9af8-de20d83b479c.png)
- ![Screenshot 2023-01-20 at 11 19 51 PM](https://user-images.githubusercontent.com/101057601/213779840-73bec7f0-6fbc-445e-bbc0-3e5e2c5ebae3.png)


## Task - 2
I created a volume using the command `docker volume create 'volumename'` to which i mounted the path `/data` of two containers which led to both of them sharing this volume and hence contents of one container were visible in another
![Screenshot 2023-01-20 at 11 59 49 PM](https://user-images.githubusercontent.com/101057601/213781148-56cac804-d5b3-48d9-b106-750de51298a6.png)


