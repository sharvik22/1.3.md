Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod
Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
После запуска увеличить количество реплик работающего приложения до 2.
Продемонстрировать количество подов до и после масштабирования.
Создать Service, который обеспечит доступ до реплик приложений из п.1.
Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.

### Решение 1

* Создал Deployment

![image](https://github.com/user-attachments/assets/77cdcc45-5b6f-4b18-b5d1-4ebfd788f864)

* Применил 

![image](https://github.com/user-attachments/assets/a1d759ad-4768-4172-a89d-2bb401a128f7)

* При запуске Deployment может возникнуть ошибка, связанная с тем, что контейнеры пытаются использовать один и тот же порт (80). 
* Чтобы решить эту проблему, можно изменить порт для контейнера multitool на отличный от 80 (8080)

![image](https://github.com/user-attachments/assets/f3f6a6fe-6142-4254-a644-bdc9c24e8239)

* Обновил Deployment

![image](https://github.com/user-attachments/assets/3f84f4b3-e435-4953-b3ab-f12ef5de5cea)

* Просмотр (есть ошибка перезапуска) 

![image](https://github.com/user-attachments/assets/da805e45-9bb5-4eb8-a064-2adaa9a4b9db)



