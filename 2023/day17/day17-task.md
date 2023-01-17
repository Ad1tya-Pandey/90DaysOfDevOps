# Task - Day 17

 - content of Dockerfile 
 ```
 # syntax=docker/dockerfile:1
FROM node:18-alpine
WORKDIR /app
COPY . . 
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000

 ```
 
 - screenshots of Docker commands
 
 ![Screenshot 2023-01-17 at 11 32 00 PM](https://user-images.githubusercontent.com/101057601/212976701-c7e15393-a49d-436e-a579-49a475646ac5.png)

- Output

![Screenshot 2023-01-17 at 11 32 33 PM](https://user-images.githubusercontent.com/101057601/212976876-d551b5b4-a541-4f63-80d4-882bb91ca5b0.png)
