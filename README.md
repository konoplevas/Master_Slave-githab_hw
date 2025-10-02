### «Репликация и масштабирование. Часть 1» - Коноплёв Александр


### Master-Slave репликация
- **Направление:** Одностороннее (Master → Slave)
- **Запись:** Только на Master
- **Чтение:** На всех серверах
- **Конфликты:** Невозможны
- **Сложность:** Простая

### Master-Master репликация  
- **Направление:** Двустороннее
- **Запись:** На любой узел
- **Чтение:** На всех серверах
- **Конфликты:** Вероятны
- **Сложность:** Сложная

## Задание 2: Настройка Master-Slave

## Запуск контейнеров
1. docker compose up -d
2. Ожидание запуска MySQL
sleep 30
3. Проверка статуса контейнеров
docker compose ps

<img width="1262" height="275" alt="Запуск контейнеров" src="https://github.com/user-attachments/assets/a2fd6304-da2b-4fd1-a94f-fd20b35548a9" />

## Настройка Master

Новый Мастер

<img width="777" height="362" alt="Новый мастер" src="https://github.com/user-attachments/assets/8e5a8994-409a-4a04-8e45-e7819ab03961" />

Статус Мастера

<img width="739" height="192" alt="Статус мастера" src="https://github.com/user-attachments/assets/e5f37d5d-e594-427d-abed-bdb5e6879c69" />

### Настройка Slave

Запуск Репликации

<img width="1271" height="175" alt="Запуск репликации" src="https://github.com/user-attachments/assets/245e3028-13b5-4582-9c5f-a6f13fe65f51" />

Проверка Слейв

<img width="937" height="259" alt="Проверка Слейв" src="https://github.com/user-attachments/assets/650dbbf8-7e6b-4cfd-a5f8-939e44e64745" />

Финальная проверка Репликации

<img width="1371" height="852" alt="Финальная проверка репликации" src="https://github.com/user-attachments/assets/01e519ef-4a7f-40f0-bd86-77bfb07b6149" />

### Настройка в DBiver

Проверка статуса Мастера

<img width="1399" height="790" alt="Статус Мастера" src="https://github.com/user-attachments/assets/8630c370-10b6-40ab-9cef-4d7f8fc7a4ed" />

Проверка роли Мастера

<img width="1430" height="776" alt="Проверка роли Мастера" src="https://github.com/user-attachments/assets/124ecf7c-f6f2-44ab-a71b-7c255e6d610f" />

Создание тестовой таблицы

<img width="1378" height="752" alt="Создание тестовой таблицы" src="https://github.com/user-attachments/assets/b8d3fa32-4a2f-4968-9440-41b045744eb2" />

Проверка данных на Мастере 

<img width="1361" height="792" alt="Проверка данных на Мастер" src="https://github.com/user-attachments/assets/20f8cf35-c9e1-4036-a7cc-b4f9e66dd6e5" />

Статус Репликации

<img width="1392" height="773" alt="Статус репликации" src="https://github.com/user-attachments/assets/883cd1dd-8993-4421-8b04-8346543eb1d8" />

Проверка роли Слейв

<img width="1388" height="755" alt="Проверка роли Слейв" src="https://github.com/user-attachments/assets/32939388-b394-4b8b-8235-8a27429f5966" />

Проверка данных Слейв

<img width="1386" height="778" alt="Проверка данных на Слейв" src="https://github.com/user-attachments/assets/dcdf6354-f871-4f61-bff3-8c9d101f0bdc" />

Проверка read_only

<img width="1426" height="764" alt="Проверка read_only" src="https://github.com/user-attachments/assets/58e3cfad-010f-4dfa-80bd-a5f322a9bdd3" />

Попытка записи на Slave (должна быть ошибка)

<img width="1427" height="773" alt="Попытка записи на Slave (должна быть ошибка)" src="https://github.com/user-attachments/assets/b763ef91-10da-4440-b94e-9957ba84abca" />




