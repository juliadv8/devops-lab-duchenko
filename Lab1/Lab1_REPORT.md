University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FTMI](https://ftmi.itmo.ru)  
Course: [Introduction-in-web-tech](https://https://itmo-ict-faculty.github.io/introduction-in-web-tech/)   
Year: 2025/2026   
Group: U4225  
Author: Duchenko Yulia Viktorovna  
Lab: Lab1  
Date of create: 30.09.2025  (Extra task: 05.10.25)
Date of finished: 03.10.2025 (Extra task: __.10.25)

## Отчет по практике - Лабораторная работа №1 "Основы работы с Docker"
Во время выполнения задания выполнены следующие шаги:

1. docker --version
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen1.png)

2. docker run hello-world
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen2.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen5.png)

3. Базовые команды: 
- docker images, 
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen3.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen14.png)

- docker ps, 
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen7.png)

- docker ps -a
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen8.png)

### Работа с готовыми образами:

4. docker pull ubuntu:latest
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen9.png)

5. docker run -it ubuntu bash
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen10.png)

6. apt update && apt install -y curl
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen11.png)

7. curl --version
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen12.png)

8. exit
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen15.png)

### Запуск веб-сервера:

9. docker run -d -p 8080:80 --name web-server nginx:alpine
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen16.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen25.png)
10. http://localhost:8080
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen17.png)
11. docker logs web-server
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen18.png)
12. docker exec -it web-server sh
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen19.png)

### Управление контейнерами:

13. docker ps
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen20.png)

14. docker ps -a
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen21.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen13.png)

15. docker stop web-server
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen22.png)

16. docker start web-server
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen23.png) 
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen24.png)

17. docker rm web-server
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen_12.png)

18. docker rmi nginx:alpine
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen27.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen26.png)

### Работа с томами (volumes):

19. docker volume create my-volume
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen28.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen29.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen32.png)

20. docker run -it --name volume-test2 -d -v my-volume:/data ubuntu bash ВМЕСТО docker run -d -v my-volume:/data --name volume-test ubuntu 
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen30.png)

21. docker exec -it volume-test bash
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen33.png)

22. echo "Hello from volume" > /data/test.txt
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen35.png)

23. Удалить контейнер и создать новый с тем же томом + Проверить, что файл сохранился
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen36.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen38.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen39.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen41.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen37.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/Lab1_screen40.png)

## Дополнительное задание: 
Собрала в Visual Studio образ с файлами app.ry, requirements,txt и Dockerfile + проверила
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/lab1.1_screen5.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/lab1.1_screen4.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/lab1.1_screen3.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/lab1.1_screen1.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab1/img/lab1.1_screen2.png)
