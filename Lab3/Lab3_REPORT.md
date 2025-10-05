University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FTMI](https://ftmi.itmo.ru)  
Course: [Introduction-in-web-tech](https://https://itmo-ict-faculty.github.io/introduction-in-web-tech/)   
Year: 2025/2026   
Group: U4225  
Author: Duchenko Yulia Viktorovna  
Lab: Lab3  
Date of create: 04.10.2025  
Date of finished: ___.10.2025 

## Отчет по практике - Лабораторная работа №3 "Мониторинг с Prometheus и Grafana"
Во время выполнения задания выполнены следующие шаги:

### Создание конфигурации Prometheus:
- Создала папку prometheus для конфигурации и файл prometheus/prometheus.yml
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen16.png)
- Запустила контейнер Node Exporter для сбора системных метрик:
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen2.png)
- Проверила работу: curl http://localhost:9100/metrics
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen1.png)

### Запуск Prometheus:
- Создала том для данных Prometheus и запустила контейнер Prometheus
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen4.png)
- Проверила работу через http://localhost:9090 в браузере
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen3.png)

### Запуск Grafana:
- Создать том для данных Grafana и запустила контейнер Grafana:
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen12.png)
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen18.png)
- Проверила работу через http://localhost:3000 
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen5.png)

### Настройка Grafana:
- Залогинилась в Grafana (admin/admin) и добавила источник данных Prometheus:
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen17.png)
- Создала дашборд для источника данных Prometheus

### Тестирование системы:
- Проверка контейнеров: docker ps
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen14.png)
- Сбор метрик в Prometheus 
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen19.png)
- Открыть Grafana и проверить отображение графиков
![](https://github.com/juliadv8/devops-lab-duchenko/blob/main/Lab3/img/lab3_screen6.png)
