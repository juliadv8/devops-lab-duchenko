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
- Запустила контейнер Node Exporter для сбора системных метрик:
- Проверила работу: curl http://localhost:9100/metrics

### Запуск Prometheus:
- Создала том для данных Prometheus и запустила контейнер Prometheus:
- Проверила работу через http://localhost:9090 в браузере

### Запуск Grafana:
- Создать том для данных Grafana и запустила контейнер Grafana:
- Проверила работу через http://localhost:3000 
Настройка Grafana:


Войти в Grafana (admin/admin)
Добавить источник данных Prometheus:
Configuration → Data Sources → Add data source
Выбрать Prometheus
URL: http://prometheus:9090
Save & Test
Создать дашборд:
Create → Dashboard → Add visualization
Выбрать источник данных Prometheus
Добавить метрику: node_cpu_seconds_total
Сохранить дашборд

Тестирование системы:

Проверить все контейнеры: docker ps
Открыть Prometheus и убедиться, что метрики собираются
Открыть Grafana и проверить отображение графиков
Создать несколько графиков для разных метрик (CPU, память, диск)
