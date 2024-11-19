# Домашнее задание к занятию «Запуск приложений в K8S» Шарапат Виктор

Задание 1.
* Создать Deployment и обеспечить доступ к репликам приложения из другого Pod
1) Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
2) После запуска увеличить количество реплик работающего приложения до 2.
3) Продемонстрировать количество подов до и после масштабирования.
4) Создать Service, который обеспечит доступ до реплик приложений из п.1.
5) Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.

### Решение 1

![image](https://github.com/user-attachments/assets/0b57a960-9f42-42d6-b29b-4bfa6b118465)

* Создал Deployment из двух контейнеров

![image](https://github.com/user-attachments/assets/babeedc0-1972-4e1c-9d64-462bfc44b0cf)

* Применил 

![image](https://github.com/user-attachments/assets/e244d5aa-4fbd-4d28-aebb-19f9ecdcf25c)

При запуске Deployment может возникнуть ошибка, связанная с тем, что контейнеры пытаются использовать один и тот же порт (80). 
Чтобы решить эту проблему, можно изменить порт для контейнера multitool на отличный от 80 (8080)

* Просмотр (есть ошибка перезапуска)

![image](https://github.com/user-attachments/assets/2c6ec2a3-e4fe-4c21-88dc-fa6d35b500b3)

![image](https://github.com/user-attachments/assets/70723c46-93de-41c5-9d56-963bdb860289)
