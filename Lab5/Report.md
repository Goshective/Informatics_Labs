## Лабораторная работа 5

### Задание 1. Автоматизация проверки формата файлов при коммите.
1. Создадим техническую папку `git/hooks`, в которой настроим запуск нужного скрипта перед коммитом (`pre-commit`)
![image](https://github.com/user-attachments/assets/d83ec8c8-26c2-4a74-b831-43d20e0aa12b)
![image](https://github.com/user-attachments/assets/ad0ffda8-4e06-4f28-9ede-719118f24771)

2. Напишем основной скрипт для проверки файлов `.txt` на наполненность и наличие `Подписи автора`

![image](https://github.com/user-attachments/assets/0ec16b6d-ea9c-426a-86f1-96034cb068f4)

3. Добавляем файлы `empty_book.txt` (Книга без текста) и `book_with_author.txt` (Книга с подписью)

![image](https://github.com/user-attachments/assets/0ccc6a27-6cb3-477c-b674-7b54a683c315)

4. Пытаемся сделать коммит с этими файлами

![image](https://github.com/user-attachments/assets/5c510c6e-94fd-4b1b-b319-7ef9db356902)

![image](https://github.com/user-attachments/assets/6a402469-6ce6-446f-8e7b-c716531745e9)

5. Добавляем файл `book_without_author.txt` (Без подписи) и повторяем коммит.

![image](https://github.com/user-attachments/assets/e67cbcc4-a523-4285-9d57-a0b6065e48d7)


#### Вывод по заданию
При помощи автоматической проверки коммитов через Git Hooks можно настроить свой проект так, чтобы исключить случайные поломки при неверно сохранённых файлах/программах.
Каждый коммит будет проверяться на соответствие требованиям, освобождая разработчика от самостоятельного тестирования, что ускоряет работу, 


### Задание 2. Использование Git Flow в проекте.
1. Инициализируем `git-flow`

![image](https://github.com/user-attachments/assets/ffd69b43-bc2c-4342-804f-cb1ef82310aa)

2. Создаём ветку для новой функциональности и закрываем после коммита

![image](https://github.com/user-attachments/assets/c24748d4-3e84-43c9-a21a-8386fd4cce77)

![image](https://github.com/user-attachments/assets/741dd2b2-fa4f-4308-8b30-15b552e2f892)


3. Переключаемся в `develop` и создаём релиз

![image](https://github.com/user-attachments/assets/be327ef7-5190-45b7-86ae-5574be4d3551)

4. После необходимых изменений закрываем его

![image](https://github.com/user-attachments/assets/7cba1996-9b94-470a-9e0a-2b1871d4fb5e)

5. Открываем и закрываем hotfix при необходимости

![image](https://github.com/user-attachments/assets/259a9d72-57de-4f5f-a60a-22a6acb505aa)

6. После все изменения передаются в develop, а в конце - в main

![image](https://github.com/user-attachments/assets/3f76d458-7eb5-4bde-b1b1-c511f78d49fe)

#### Вывод по заданию
При помощи Git Flow можно работать над большими проектами командой любого размера, так как эта методика позволяет чётко разделять каждый этап разраюотки и вносить ве изменения структурированно и обоснованно.

### Вывод
Изучены основы и продвинутые методы работы с системой контроля версий Git. В каждой из задач были сделаны выводы на основе их результатов.
