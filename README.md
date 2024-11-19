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

* Создал namespace, переключился на него, применил Deployment 

![image](https://github.com/user-attachments/assets/70566248-e923-4ff0-85e7-417040e370b4)

![image](https://github.com/user-attachments/assets/1aa0daa4-22a0-428e-9506-2eab7185facb)

![image](https://github.com/user-attachments/assets/cbd614c2-0411-424f-8015-d2a674488bfd)
