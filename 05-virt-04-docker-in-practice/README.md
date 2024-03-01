# Домашнее задание к занятию 5. «Практическое применение Docker»

---

## Задача 1
1. [ССылка на репозиторий](https://github.com/aspire87/shvirtd-example-python)

---
### ВНИМАНИЕ!
!!! В процессе последующего выполнения ДЗ НЕ изменяйте содержимое файлов в fork-репозитории! Ваша задача ДОБАВИТЬ 5 файлов: ```Dockerfile.python```, ```compose.yaml```, ```.gitignore```, ```.dockerignore```,```bash-скрипт```. Если вам понадобилось внести иные изменения в проект - вы что-то делаете неверно!
---

## Задача 2 

[Отчет по  сканированию](vulnerabilities.csv)

## Задача 3

[Результат выполнения запроса](img/TASK_3_sql_requests.png)

## Задача 4
Скрипт для деплоя приложения 

```bash
#!/bin/bash

yum install git -y

curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh
systemctl  start docker && systemctl enable docker

cd /opt
git clone https://github.com/aspire87/shvirtd-example-python.git && cd shvirtd-example-python
docker compose up -d
echo "Wait mysql  container started...."
sleep 180

echo "Done...."

```
Fork-репозиторий
[ССылка на репозиторий](https://github.com/aspire87/shvirtd-example-python)

Результат выполнения sql-запроса

[](img/TASK_4_sql_requests.png)


Результат проверки через   ```https://check-host.net/check-http```

[](img/TASK_4_check_server.png)




## Задача 6
Получаем  файл terraform.bin с помощью dive  и  docker save
 
[](img/TASK_6_push_terraform.png)

[](img/TASK_6_dive_terraform.png)

[](img/TASK_6_copy_terraform.png)




## Задача 6.1
Запускаем контейнер ```hashicorp/terraform:latest```  и копируем  файл  из  контейнера с помощью  docker cp

[](img/TASK_6_docker_cp_terraform.png)


