# Домашнее задание к занятию "`«Disaster recovery и Keepalived»`" - `Филон Андрей`

---

### Задание 1


    Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.
    На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
    Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
    Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
    На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.

### Ответ:  

![Ссылка на скриншот](https://github.com/AndreyFilon/Disaster_recovery/blob/main/1.1.jpg)
![Ссылка на скриншот](https://github.com/AndreyFilon/Disaster_recovery/blob/main/1.2.jpg)
![Ссылка на схему task1.pkt](https://github.com/AndreyFilon/Disaster_recovery/blob/main/task1.pkt)

---

### Задание 2


    Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного файла.
    Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах
    Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.
    Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script
    На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html

### Ответ:

![Ссылка на bash-скрипт](https://github.com/AndreyFilon/Disaster_recovery/blob/main/nginx.sh)  
![Ссылка на конфигурационный файл keepalived](https://github.com/AndreyFilon/Disaster_recovery/blob/main/keepalived.conf)

`Скриншоты работы nginx на главном сервере, резервном и виртуальном ip и при отключении главного сервера`

![Ссылка на скриншот](https://github.com/AndreyFilon/Disaster_recovery/blob/main/2.%20master%20ip.jpg)
![Ссылка на скриншот](https://github.com/AndreyFilon/Disaster_recovery/blob/main/2.%20backup%20ip.jpg)
![Ссылка на скриншот](https://github.com/AndreyFilon/Disaster_recovery/blob/main/2.%20virt%20ip.jpg)
![Ссылка на скриншот](https://github.com/AndreyFilon/Disaster_recovery/blob/main/2.%20broken%20master%20ip.jpg)

---

