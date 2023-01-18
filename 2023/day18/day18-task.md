# Task of Day 18 

## Task 1

- Here I have created a Docker compose file which will automate the process of creating containers and making them communicate in order to function as required.

-  `Docker-compose` file initially with passwords and sensitive info exposed in it (Used in development environment)
```
services:
  app:
    image: node:18-alpine
    command: sh -c "npm install && npm run dev"
    ports: 
      - 3000:3000
    working_dir: /app
    volumes:
      - ./:/app
    environment:
      MYSQL_HOST: mysql
      MYSQL_USER: root  
      MYSQL_PASSWORD: secret
      MYSQL_DB: todos
  mysql:
    image: mysql:8.0
    volumes:
      - todo-mysql-data:/var/lib/mysql
    environment:
      MYSQL_ROOT_PASSWORD: secret
      MYSQL_DATABASE: todos

volumes:
  todo-mysql-data:

```
- `Docker-compose` file with a .env file in the same parent directory (as a best practice used for deployment)

```
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
- Outcome:

![Screenshot 2023-01-18 at 11 36 44 PM](https://user-images.githubusercontent.com/101057601/213260089-a91da70d-7e44-4870-a0a0-34e76bd04a40.png)

# Task 2
- executed the specified commands from pulling a image from dockerhub to inspecting it, stopping it to removing it .
