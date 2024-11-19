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


# Проверка

Была ошибка в Service, пересоздал и запустил

![image](https://github.com/user-attachments/assets/da08b0e1-b972-45e5-a65a-621016d51de5)

* пересоздал Service

![image](https://github.com/user-attachments/assets/f0a5b89e-3d8c-4234-80ec-8b5dd85bdd3f)

![image](https://github.com/user-attachments/assets/b1eb07c2-94eb-4c97-805c-0a6e97297626)



* проверка доступа nginx

![image](https://github.com/user-attachments/assets/2efdaf0c-d8e0-4787-8fc9-01cb72056dcc)

* проверка доступа multitool

![image](https://github.com/user-attachments/assets/e25350dd-2522-4095-b732-73bf172e6b1f)

---

Задание 2. 
* Создать Deployment и обеспечить старт основного контейнера при выполнении условий
1) Создать Deployment приложения nginx и обеспечить старт контейнера только после того, как будет запущен сервис этого приложения.
2) Убедиться, что nginx не стартует. В качестве Init-контейнера взять busybox.
3) Создать и запустить Service. Убедиться, что Init запустился.
4) Продемонстрировать состояние пода до и после запуска сервиса.

### Решение 2

* Создаю и применяю манифест

![image](https://github.com/user-attachments/assets/645f072c-f5ae-4f5c-baee-cfe0051af655)

![image](https://github.com/user-attachments/assets/6f5518f0-e134-4c3a-bddb-447f41413205)

![image](https://github.com/user-attachments/assets/cf462cd0-3d1b-46cf-b448-530bf98813b4)

Под не запустился, состояние Init:0/1

* Создаю Service, применяю его, проверяю запуск пода

![image](https://github.com/user-attachments/assets/2295c4b2-893c-4690-a357-9e339f390239)

![image](https://github.com/user-attachments/assets/547f07a6-e3ba-45dc-a840-5007ae95949d)

![image](https://github.com/user-attachments/assets/18f20653-89b3-4e4a-bc40-f0213fc9b190)

После запуска Service запустился pod.

P.S. Удалил не нужный Service и проверил работы

![image](https://github.com/user-attachments/assets/ac50d4a3-6dd8-4b31-944d-7a598018ef1b)

![image](https://github.com/user-attachments/assets/5b507a98-8a7f-41c0-aabb-9a42d3ee977b)

![image](https://github.com/user-attachments/assets/b62b9484-bebb-40c8-bb80-2fd418840b5e)

**************






