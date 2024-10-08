# Домашнее задание к занятию 14 «Средство визуализации Grafana» Шарапат Виктор

## Задание повышенной сложности

**При решении задания 1** не используйте директорию [help](./help) для сборки проекта. Самостоятельно разверните grafana, где в роли источника данных будет выступать prometheus, а сборщиком данных будет node-exporter:

- grafana;
- prometheus-server;
- prometheus node-exporter.

За дополнительными материалами можете обратиться в официальную документацию grafana и prometheus.

В решении к домашнему заданию также приведите все конфигурации, скрипты, манифесты, которые вы 
использовали в процессе решения задания.

**При решении задания 3** вы должны самостоятельно завести удобный для вас канал нотификации, например, Telegram или email, и отправить туда тестовые события.

В решении приведите скриншоты тестовых событий из каналов нотификаций.

## Обязательные задания

### Задание 1

1. Используя директорию [help](./help) внутри этого домашнего задания, запустите связку prometheus-grafana.
1. Зайдите в веб-интерфейс grafana, используя авторизационные данные, указанные в манифесте docker-compose.
1. Подключите поднятый вами prometheus, как источник данных.
1. Решение домашнего задания — скриншот веб-интерфейса grafana со списком подключенных Datasource.

## Задание 2

Изучите самостоятельно ресурсы:

1. [PromQL tutorial for beginners and humans](https://valyala.medium.com/promql-tutorial-for-beginners-9ab455142085).
1. [Understanding Machine CPU usage](https://www.robustperception.io/understanding-machine-cpu-usage).
1. [Introduction to PromQL, the Prometheus query language](https://grafana.com/blog/2020/02/04/introduction-to-promql-the-prometheus-query-language/).

Создайте Dashboard и в ней создайте Panels:

- утилизация CPU для nodeexporter (в процентах, 100-idle);
- CPULA 1/5/15;
- количество свободной оперативной памяти;
- количество места на файловой системе.

Для решения этого задания приведите promql-запросы для выдачи этих метрик, а также скриншот получившейся Dashboard.

## Задание 3

1. Создайте для каждой Dashboard подходящее правило alert — можно обратиться к первой лекции в блоке «Мониторинг».
1. В качестве решения задания приведите скриншот вашей итоговой Dashboard.

## Задание 4

1. Сохраните ваш Dashboard.Для этого перейдите в настройки Dashboard, выберите в боковом меню «JSON MODEL». Далее скопируйте отображаемое json-содержимое в отдельный файл и сохраните его.
1. В качестве решения задания приведите листинг этого файла.

---

### Как оформить решение задания

Выполненное домашнее задание пришлите в виде ссылки на .md-файл в вашем репозитории.

---


## Решение

### Задание 1

не использовал директорию [help](./help) для сборки проекта. Создал собственную сборку и файл docker-compose.yml с установкой следующих компонентов:

- grafana;
- prometheus-server;
- prometheus node-exporter;

![Screenshot_7](https://github.com/user-attachments/assets/05dcbc59-14db-4646-9fd3-3b16f1063cf4)

![image](https://github.com/user-attachments/assets/35d4605e-5059-4644-b0e7-080c63940868)

![Screenshot_1](https://github.com/user-attachments/assets/fedd108d-a1f5-4c42-b6c5-81d61a5abe63)

![Screenshot_2](https://github.com/user-attachments/assets/f5a7c2f2-4619-410e-9433-3a9fe7fe31a8)

![Screenshot_3](https://github.com/user-attachments/assets/c3e360d6-8228-49d0-969f-6ab8b0d53f60)

![Screenshot_4](https://github.com/user-attachments/assets/f5327fa7-564e-4fb6-8cde-e5a7b205b1cc)


## Задание 2

cpu unilization

![image](https://github.com/user-attachments/assets/2d897e32-24bf-47e9-9f90-93037f4c8af7)


Memory

![image](https://github.com/user-attachments/assets/e29713d4-89e0-448f-b09b-703c70f9c872)

CPU Load Average

![image](https://github.com/user-attachments/assets/abf91a11-e4aa-4690-9a94-692db6bb9e4e)

Total/Used disk

![image](https://github.com/user-attachments/assets/ae4b5158-93dd-4baa-a4bd-72013f88c60a)

![image](https://github.com/user-attachments/assets/b605074b-cae5-43a1-a2bb-ee3279eb34bb)


## Задание 3

![image](https://github.com/user-attachments/assets/d1f5c61e-d249-4fc2-8e4a-ff4c9d1ab39f)

с помощью stress testa проверил работу оповещения 

![image](https://github.com/user-attachments/assets/56ebebbe-bfd9-413f-8328-122761093518)

![image](https://github.com/user-attachments/assets/83bf2cde-bd20-4f47-8e0a-1f3314467118)

![image](https://github.com/user-attachments/assets/070747cd-3de0-419e-a0f3-cf1fae00674b)

## Задание 4

[[netology.json](https://github.com/sharvik22/10-monitoring-03-grafana.git/)](https://github.com/sharvik22/10-monitoring-03-grafana/blob/main/netology.json)

