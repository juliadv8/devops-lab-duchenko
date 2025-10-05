University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FTMI](https://ftmi.itmo.ru)  
Course: [Introduction-in-web-tech](https://https://itmo-ict-faculty.github.io/introduction-in-web-tech/)   
Year: 2025/2026   
Group: U4225  
Author: Duchenko Yulia Viktorovna  
Lab: Lab2 
Date of create: 04.10.2025  
Date of finished: ___.10.2025  

## Отчет по практике - Лабораторная работа №2 "CI/CD для Docker приложения"
Во время выполнения задания выполнены следующие шаги:

### 1. Подготовка проекта:
- Скопировала файлы из первой лабораторной (app.py, requirements.txt, Dockerfile) в новый репозиторий
- Создала аккаунт на Docker Hub и новый репозиторий на Docker Hub для образа

### 2. Настройка GitHub Actions:
- Создала папку .github/workflows/ в корне проекта и создала файл docker-build.yml (.github/workflows/docker-build.yml) с пайплайном, который должен выполнять условия:
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen8.jpg)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen6.png)

### 3. Настройка секретов:
- В настройках GitHub репозитория добавила секреты:
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen7.png)

### 4.Тестирование пайплайна:
- Сделала коммит и пуш в main ветку
- Проверила выполнение пайплайна в разделе Actions
- Провелила наличие образа в Docker Hub
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen5.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen4.png)
- Проверила логи выполнения каждого шага

## Дополнительное задание: 
- Создала ветку develop для разработки, выполнила условия и проверила. 

![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen1.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen3.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab2/lab2_screen2.png)
