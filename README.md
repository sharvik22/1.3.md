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

* увеличил количество реприк до 2-х применил Deployment

![image](https://github.com/user-attachments/assets/d94714e6-9e01-412e-ad73-5c9610e881c3)

![image](https://github.com/user-attachments/assets/f4909e1c-4b96-428e-a05e-7d0319d034f5)

* Создать Service

![image](https://github.com/user-attachments/assets/2f5af9ed-5088-402c-b42e-eea1c168302a)

* Применяю и проверяю его

![image](https://github.com/user-attachments/assets/d2a98660-c2fa-48e8-bcc2-275f52d0ce4c)

![image](https://github.com/user-attachments/assets/52d8122f-f8c3-4e72-8774-36eb0eae1404)

* Создал отдельный Pod с приложением multitool, применил его

![image](https://github.com/user-attachments/assets/979b838b-be4f-4dbf-9dbe-ffa2170fc114)

![image](https://github.com/user-attachments/assets/3b35bda7-31a3-41de-97c5-43a4299831a3)

* все поды запущенны

![image](https://github.com/user-attachments/assets/b3076bca-1ac9-4eed-ab0b-998b92362676)


* проверка

![image](https://github.com/user-attachments/assets/da08b0e1-b972-45e5-a65a-621016d51de5)










