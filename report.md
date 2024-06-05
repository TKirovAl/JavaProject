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

Я долго промучился прежде, чем войти в свою баху данных, а оказывается, что необходимо писать название с нижним регистром:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/1ce3c54d-480b-4807-bb0d-93532a7d5f81)

Создаем таблицы и добавляем записи:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/69ab9588-d6e9-4d85-9bcd-619a372228b5)

ТА-ДА! Вот она таблица, вот они записи:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/38791c29-b577-4b64-b37c-5937080ae26d)

Соотвественно, и вторую таблицу по тз сделаем:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/3b53ff0c-b790-4e2c-970f-e0336261670f)

Теперь нужно усатновить Maven. ~~Ссылка прилагается:
https://maven.apache.org/download.cgi~~
Сделаем это командой sudo apt install maven.

~~Послесловие~~

~~Далее времени у меня уже нет, я в тупике. Я использовал visual studio 2022 года и, посмотрев на рапорт Самойлова, понял, что просчитался где-то. К слову, я не нашел в VS расшрения(плагина, пакета) PostgreSQL, поэтому и писать тут уже больше нечего. Но опыт был интересный, жаль, что неудачно вышло...~~

Как хорошо быть самим собой! У меня появилось, метфорически выражаясь, второе дыхание, поэтому незамедлительно продолжаю!
Устанавливаем maven:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/e24ccab2-39ea-4c93-98a8-df92e86e7f9e)

Скачиваем и устанавливаем Spring:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/9f306f0d-fdd8-47b9-85ff-ba53a7ae5802)

...

Знаете то чувство, когда все вокруг воют современным оружием по типу АК-74М, а ты стреляешь с лука. Вот и я такой же... Использовал VS Microsoft, когда нужно было использовать VS Code... Просчитался, но где...
Короче, устанавливаю эту визуалку и полагаю сделаю пару скриншотов, как я преодолел скорость полета стрелы скоростью полета пули... 

О-о-о, я зашел в VS Code и мне тут же предложили установить WSL:


![image](https://github.com/TKirovAl/JavaProject/assets/93568292/baa0e11c-eef7-4246-9588-fa637724efca)


Повезло, повезло))

Полагаю, что следующие проецссы установки можно не скриншотить, ведь можно просто "загуглить" и парой кликлов установить все необходимое. 

Я уже устанавливал maven, так что мне выдает сообщение о том, что данное расширение уже существует.
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/e00a36e2-bd1f-420a-be35-5208c1e495b6)

Гугл - установить - работаем:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/f2997b8f-09d7-4666-9abf-5943e4182e60)

Возвращаемся к работе с SQL:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/3f6e18fe-6dba-48bf-8b9d-f86d83d20d3e)

Connection:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/fdb40e66-bacf-4e59-9773-61f9c6f729b0)

Переходи в vs code, а конкретнее во вкладку "Database":
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/8d7266a3-5d2e-4548-a089-809adf9ceb75)

Что-то знакомое... Кажется я разбирался с подключением вручную, через терминал и файлы конфигуарции, но рапорт товарища Самойлова указал мне верный путь:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/dae0c970-34b7-48a6-9451-06302e355b58)

Даа, я тут пару лишних баз данных создал, ну да ладно, используем "kirov":
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/3692dd43-d9cc-4713-96b6-55692d425c67)

Урааа, теперь можно не мазолить глаза в сером интерфейсе, всё цветное и крутое. Ах, без театральной эйфории мне жизнь не мила!
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/b7e0f4dc-9a3d-418a-b3b8-4bc4a828b526)

Сергей Вольдемарович мной бы гордился, наверное:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/63607c6e-982a-4e21-bee5-0264b0e1b19a)

Разбираемся со Spring, инициализируем:
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/cb5eee3a-b0f3-444e-aa7f-5ed057ba361a)

Успех!
![image](https://github.com/TKirovAl/JavaProject/assets/93568292/86dac88b-d84f-4103-b755-a361644770a6)





























