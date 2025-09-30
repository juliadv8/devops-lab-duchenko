University: ITMO University  
Faculty: FTMI  
Course: [Introduction-in-web-tech](https://itmo-ict-faculty.github.io/introduction-in-web-tech/education/labs2025-2026/lab1/lab1/#_4)  
Year: 2025/2026   
Group: U4225  
Author: Duchenko Yulia Viktorovna  
Lab: Lab1  
Date of create: 30.09.2025  
Date of finished: ___.09.2025  

## Отчет по практике - Лабораторная работа №1
Во время выполнения задания выполнены следующие шаги:

1. docker --version
2. docker run hello-world
3. Базовые команды: 
- docker images, 
- docker ps, 
- docker ps -a

### Работа с готовыми образами:

4. docker pull ubuntu:latest
5. docker run -it ubuntu bash
6. apt update && apt install -y curl
7. curl --version
8. exit

### Запуск веб-сервера:

9. docker run -d -p 8080:80 --name web-server nginx:alpine
10. http://localhost:8080
11. docker logs web-server
12. docker exec -it web-server sh

### Управление контейнерами:

13. docker ps
14. docker ps -a
15. docker stop web-server
16. docker start web-server
17. docker rm web-server
18. docker rmi nginx:alpine

### Работа с томами (volumes):

19. docker volume create my-volume
20. docker run -it --name volume-test2 -d -v my-volume:/data ubuntu bash ВМЕСТО docker run -d -v my-volume:/data --name volume-test ubuntu 
21. docker exec -it volume-test bash
22. echo "Hello from volume" > /data/test.txt
23. Удалить контейнер и создать новый с тем же томом + Проверить, что файл сохранился
