## Лабораторная работа 4

#### Запустим 2 контейнера. Проверим работоспособность командой `aafire`. Далее настроим связь между ними
1. Создадим `dockerfile` с загрузкой нужных команд.

![image](https://github.com/user-attachments/assets/eee1c361-a745-4e7a-befc-a1928d48fc2c)

2. Запустим контейнер

![image](https://github.com/user-attachments/assets/76e8a3c1-dd62-44ac-8f15-9c7557c89621)

3. Результат команды `aafire`

![image](https://github.com/user-attachments/assets/191c651e-9d9b-439f-87b7-0fb50720e716)

4. Проверяем запуск первого контейнера
   
![image](https://github.com/user-attachments/assets/41be000f-cca8-4741-b098-d2006bb3a3dd)

5. Запускаем параллельно второй контейнер

![image](https://github.com/user-attachments/assets/81ee5c57-1ad7-4e85-9263-e8cb8b3dd2d2)

6. Создаём сеть и подсоединяем к ней контейнеры по их Id

![image](https://github.com/user-attachments/assets/f801a84b-4e74-405a-80c5-6ef0747eaf70)

7. IP-адреса контейнеров в созданной сети

![image](https://github.com/user-attachments/assets/f7200270-1919-428d-8881-0b83f505c4eb)

8. Ping для первого контейнера

![image](https://github.com/user-attachments/assets/42563822-acf6-4fef-8ae3-a702997d56c4)

9. Ping для первого контейнера

![image](https://github.com/user-attachments/assets/e5cfdc5a-8713-4199-9cc9-77d6806e9805)

### Вывод
Изучены основы работы с настройкой сетей в docker и созданием контейнеров. Также были использованы на практике консольные команды для работы с сетями и docker.
