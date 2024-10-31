## Лабораторная работа 3

#### Запустим 3 виртуальных машины. Начнём создавать между ними соединение при помощи настроек сети в Virtual Box.

1. Адрес машины А - `192.168.56.3` - находим при помощи команды `$ ip route`.

![image](https://github.com/user-attachments/assets/cf8c7c33-f203-465d-b2ca-fe2029b0363a)

2. Аналогично находим адрес машины Б: `192.168.56.4`. Проверяем подключение.
- Машина А установила соединение с машиной Б
- Но машина А не получила ответ от подключения к самой себе 

![image](https://github.com/user-attachments/assets/cc1e8d6a-8981-4fa3-b2a0-3047e000bcdc)
![image](https://github.com/user-attachments/assets/e8e9062f-d0f3-4ccc-981a-0d97fcd5a3cc)

3. Дополнительно проверяем соединение командой `$ ping` для А и Б.

![image](https://github.com/user-attachments/assets/4ca01602-5f3d-409e-aba2-095e0256e03c)
![image](https://github.com/user-attachments/assets/4755a017-65e0-4230-9d8e-c5804dcf9256)

4. Подключаем машину В. С ней устанавливает соединение только машина Б. Из машины А ответ не может быть получен.

![image](https://github.com/user-attachments/assets/7f4b0949-d4c5-42bf-b813-a5c7514410dc)
![image](https://github.com/user-attachments/assets/9502b3c1-29cd-411a-a20d-1c0352f83cbe)

### Вывод
Изучены основы работы с настройкой сетей, взаимодействия со средой Virtual Box. Также были использованы на практике консольные команды для работы с сетями.
