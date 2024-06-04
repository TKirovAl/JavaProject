Итак, начинаю работу над созданием окружения для работы с Java.

Я пользователь Windows, поэтому необходимо устанвить "wsl". Для этого я запущу программу "Windows PowerShell" и напишу команду `wsl --instsll online`. После этого начнется процесс установки, затем программа порекомендует перезапустить систему. Я это уже сделал. Проверим установлен ли wsl.

`wsl` - эта простая команда и выдаст информацию о наличии пакета на ПК.
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/181c5dc5-2289-41ff-a7f1-f45b871b1f8b)

Я какое-то время не мог продолжать работу над данным проектом, но когда вернулся, то с удивлением обнаружил, что в VS уже есть функция "Установить WSL для меня", после чего я незамедлительно нажал счастилвую кнопочку.
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/5867cc0a-f489-43cf-984a-4156892df969)

Итак, WSL установлен и я стал счастливым обладателм интсрументраием и окружением для работы с Linux в среде Windows. Начну устанавливать необходимы для проекта пакеты и инструменты:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/198dd70a-bfcc-4da1-ae51-018df42b664d)

Какая жалость, у меня отсутсвует java, но вот удача, есть же команда `sudo apt-get install openjdk-17-jdk`!
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/8c7f9281-ce8d-458c-99b9-0d28547ff5cb)

Теперь осталось разобраьбся с postgresql и можно перейти к созданию базы данных.
Устанавливаем postgresql 
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/e74d0d36-0553-4b28-ba2d-52acb2b6b09b)

Теперь при помощи команд `sudo -u postgres psql` и `sudo servcie postgresql start` приступаем к работе с БД.

Создадим базу данных и таблицы при помощи языка запросов SQl. Но я уже ранее их создавал, поэтому выдаает ошибку, сообщаюшая, что у меня уже есть данные таблицы и база данных, соответсвенно.
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/c53da66e-761a-4d34-a0cb-fe08d3d72c84)

База данных, кстати, создается при помощи команды `CREATE DATABASE "имя"`

Кое-что произошло и придется изменить конфигурацию PostgreSQL:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/811deaee-bad9-4a7d-bc09-1e4595419b13)


