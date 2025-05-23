# Commands


## Тут хранятся разные команды



`npm init -y`  - установка самого NPM в папку с проектом </br>
`npm install babel-cli babel-core babel-preset-es2015 --save-dev`   - установка Babel находясь в корне проекта</br>
`npx babel src --out-dir dist`   - добавление соответствующих папок</br>

`npm i bootstrap --save--dev`   - усиаервмит будстрап </br>

`npm uninstall bootstrap`   -  удалить установленный пакет </br>

`npm install axios`

` npm i vuex -S`

## React start *************

`npm install prop-types`  - библиотека для определения входящих свойств компонентов props
`import PropTypes from 'prop-types'`

## React finish *************

### eslint плагин для автоматической проверки ошибок
`npm i --save--dev eslint`  - установка плагина который будет проверять код на js на ошибки по спецификации airbnb  
`npm i --save--dev eslint-config-airbnb eslint-plugin-html eslint-plugin-import eslint-plugin-jsx-a11y`  
`npm i --save--dev eslint-config-prettier eslint-plugin-prettier prettier`  

нужно создать файл вида `.eslintrc` и в нем создать объект вида:  

` 
{
  "extends": ["airbnb/base"]
}

`  

ещё можно создать файл `.eslintignore` в нем записывать файлы которые не нужно проверять.  

---------------------
HtmlWebpackPlugin. Этот плагин также позволяет автоматически встраивать в html созданные вебпаком бандлы.</br>


------
`npm install --save--dev clean-webpack-plugin`  - этот плагин удаляет файлы перед тем как билдить заново, чтобы не создавалось дублей
const {CleanWebpackPlugin} = require('clean-webpack-plugin');  добавить в webpack.config.js </br>
и там же в раздел  plugins    new CleanWebpackPlugin(), 


----
Сначала нужно установить плагин с помощью команды </br>

`npm i -D  html-webpack-plugin`</br>

Используем флаг -D (save-dependencies) потому, что этот пакет нам нужен только для этапа разработки. Для функционирования конечного приложения этот пакет не нужен.</br>

-------------------



`npm i`   -  установить все пакеты которые есть в package.json - если он есть как отдельный файл со сборкой проекта.

Для файла packadge.json изменить

`
  "scripts": {</br>
    "bild": "babel src -d -dist -presets es2015",</br>
    "watch": "babel src -d -dist -presets es2015 -w"</br>
  },
`

`"build": "babel src -d -dist -presets es2015",`   -  "src" название папки в корне откуда будет браться код es2015 и "-dist" куда он будет компелироваться в старом формате.
 
` "watch": "babel src -d -dist -presets es2015 -w"`  - автоматическое компилирование после сохранения. 


`npm run build`  - запуск  билда</br>
`npm run watch` - запуск смотрителя </br>

`npm run dev`  - запуск веб сервера</br>



### Команды GIT

----
https://ru.stackoverflow.com/questions/431520/%D0%9A%D0%B0%D0%BA-%D0%B2%D0%B5%D1%80%D0%BD%D1%83%D1%82%D1%8C%D1%81%D1%8F-%D0%BE%D1%82%D0%BA%D0%B0%D1%82%D0%B8%D1%82%D1%8C%D1%81%D1%8F-%D0%BA-%D0%B1%D0%BE%D0%BB%D0%B5%D0%B5-%D1%80%D0%B0%D0%BD%D0%BD%D0%B5%D0%BC%D1%83-%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%83 - переходы по комитам и веткам полезно

`git -inint`   - создать репазиторий гит</br>
`echo >> README.md` - создаем папку </br>
`git config --local(--global) user.email` "тут вводим емаил"</br>
`git config --local(--global) user.name` "тут вводим имя"</br>

`git status`</br>

git diff ветка1 ветка2 - посмотреть чем отличаются две эти ветки  
git diff --name-only ветка1 ветка2 -  посмотреть не сами отличия, а список отличающихся файлов  

`git log`  - показывает все коммиты сделанные в данной ветке</br>
`git log --follow css/style.css` - можно отследить историю конкретного файла</br>
`git log --all --graph` - вывести лог всех веток с графикой ветки</br>


`git config --global format.pretty '%C(red)%h%Creset %C(yellow)%ad%Creset | %C(bold blue)%s%Creset %C(dim green)(%an)%Creset %C(dim yellow)%d%Creset' `
`git config --global log.date short`
`git config --global log.graph true` - не работает
`git config --global --unset log.graph` - не работает


`--pretty="..."` — определяет формат вывода.</br>
`%`h — укороченный хеш коммита.</br>
`%ad` — дата коммита.</br>
`|` — просто визуальный разделитель.</br>
`%s` — комментарий.</br>
`%d` — дополнения коммита («головы» веток или теги).</br>
`%an` — имя автора.</br>
`--date=short` — сохраняет формат даты коротким и симпатичным.</br>


`gi cat-file -p *****` - посмотреть какие файлы есть. в звездочках первые пять сиволов названия файла с хешом.</br>

`git checkout -b` название_ветки  - создать и перейти в новую ветку (команда разовая)</br>
`git checkout` название_ветеки - просто перейти на другую ветку </br>

`git add -A`  - добавляем все файлы в гит чтобы он о них знал, это нужно делать перед комитом</br>
`git add *.html`   -добавляем только файлы формата </br>

`git commit -m "Сообщение к коммиту"`  - перед тем как запушить данные в гитхаб, их нужно закомитеть</br>
`git commit -a -m "Первый коммит"`  - добавляем коммит</br>
`git commit --amend -m "коммит"` - примешать этот коммит к предыдущему изменив его название на новое</br>
`git reset --soft HEAD^` - Если вы сделали commit в git, но поняли, что он достаточно плох. Эта команда отменит последний коммит (но не изменения, которые внесли, они сохранятся).</br>

`git push origin master`  - залить локальные изменения на ветку master на гитхабе</br>

`git push origin название_текущей_ветки(не мастер)` - для загрузки на удаленный репозиторий нужно отправлять именно мою отдельную ветку а не мастер

`git pull origin название_ветки` - скачать обновления с репозитория</br>  
`git reset --merge` - откатить попытку скачать удаленный репозиторий  </br>
`git reset HEAD hello.html` - отменить файл добавленный для коммита</br>
`git reset HEAD~1`  - откатиться на один комит назад</br>
`git checkout hello.html` - если файл еще не добавлен для коммита, то отменяет все изменения в нем.</br>

`git tag tagName` - создание тега для коммита - удобней искать.</br>
`git tag -d tagName` - удаление тега.</br>

`git show commitName` - просмотреть историю конкретного комита</br>

<hr>
`git remote update origin` - обновит ваши локальные ветви отслеживания.  

`git remote show origin` сравнивает ваш локальный репозиторий с удаленным:

`fast-forwardable` означает, что вы можете отправить свои локальные изменения в удаленную ветку.
`local out of date` означает, что ваша локальная ветка находится за удаленной веткой, и вы должны извлечь из нее.
`git status`  сравнивает ваш локальный рабочий каталог с текущей фиксацией текущей ветки (также известной как HEAD). Кроме того, он сравнивает вашу локальную ветку с (локальной!) Копией отслеживания удаленной ветки ( `origin/master`), следовательно,Your branch is ahead of 'origin/master' by 5 commits.

Чтобы устранить расхождение между `git status` (который показывает только локальные данные) и `git remote show origin` (который показывает "живые" удаленные данные), вы должны запустить, `git remote update origin` который обновит ваши локальные ветви отслеживания. Он обновит ваш локальный origin/masterдо состояния удаленного master. После этого `git status` вы должны получить что-то вроде `Your branch is behind 'origin/master' by X commits, and can be fast-forwarded`.

<hr>

`gitk --all&`  - открыть графический интерфейс по гиту, но нужно через консоль гит    

`git stash` - спрятать ветку перед пулом мастера  
`git merge master` - находясь в своей ветке выгрузить к себе мастера  


Если у вас уже есть ветка feature, то после коммита в нее сделайте git checkout master – это переключит текущую ветку на master.

Пока вы не вкоммитили изменения, вы не можете переключиться на другую ветку. Выхода два: вкоммитить изменения или отложить их. Второе можно сделать с помощью git stash – это добавит текущие незакоммиченные изменения в стек изменений и сбросит текущую рабочую копию до HEAD'а репозитория. Далее вы сможете:

`git stash list`: показать все изменения в стеке  
`git stash show`: показать последнее изменение в стеке (патч)  
`git stash apply`: применить последнее изменение из стека к текущей рабочей копии  
`git stash drop`: удалить последнее изменение в стеке  
`git stash pop`: применить последнее изменение из стека к текущей рабочей копии и удалить его из стека  
`git stash clear`: очистить стек изменений  


### Чтобы соединить ветки:</br>

--------
`git checkout master` - перейти в ветку master</br>
`git switch branchName` - перейти на ветку</br>
`git switch -c branchName` - создание ветки и переключение на нее</br>
`git merge название_ветки_которую_сливаем_с_мастером`</br>

`git branch -D название_ветки` - удаление ветки</br>

`git branch` - показывает какие ветки сейчас существуют</br>
`git branch -v` - увидим ветки и часть хеша коммита</br>
`git branch -a` - посмотреть ветки и на удаленном репозитории</br>

`git fetch` - обновить информацию об удаленных ветках</br>
`git branch -r` -  увидеть список всех удалённых веток</br>

Если вы знаете точное имя ветки, то достаточно:</br>
 `git fetch origin`</br>
 `git checkout` имя-ветки</br>

`git remote add origin https://github.com/SkorihV/tickets-project.git`   - привязка локального хранилища к виртуальному где "tickets-project.git" это название проекта </br>
`git remote -v`   - покажет к какому удаленному репозиторию привязан проект</br>


`git clone адрес_к_репозиторию`</br>


`ssh-keygen` - создать ssh ключ </br>


{
 	"word_separators": "`~!@#$%^&*()=+[{]}\\|;:'\",.<>/?"
}


####.editorconfig  

`
[*.{js,jsx,ts,tsx,vue}]  
indent_style = space  
indent_size = 2  
end_of_line = lf  
trim_trailing_whitespace = true  
insert_final_newline = true  
max_line_length = 100  

`


### Разширения для VSC

Better Comments  
Bracket Pair Colorizer  
ESLint 
GitLens — Git supercharged  
Live Server  
PowerShell  
Prettier Formatter for Visual Studio Code  
Project Manager 
Russian Language Pack for Visual Studio Code  
Vetur  
Auto Import - ES6, TS, JSX, TSX  
 
 
 
 ### Bash
 
 Открыть Bash здесь https://gist.github.com/Korveld/2f3895dd5e47b92ec241305effbb4a72
 

[client]  
host     = localhost  
user     = debian-sys-maint  
password = O1YuWbozDTAd6cm1  
socket   = /var/run/mysqld/mysqld.sock  
[mysql_upgrade]  
host     = localhost  
user     = debian-sys-maint  
password = O1YuWbozDTAd6cm1  
socket   = /var/run/mysqld/mysqld.sock  
~                                       


Подключиться к mysql

`mysql -u root -p`

php -S 127.0.0.1:10888 -t public

https://rtfm.co.ua/mysql-commands/ - команды по mysql

products | CREATE TABLE `products` 
        ( 
          `id` int(11) NOT NULL AUTO_INCREMENT,
          `name` varchar(255) NOT NULL,
          `price` int(11) DEFAULT '0',
          `article` varchar(255) NOT NULL DEFAULT '',
          `currency` varchar(255) NOT NULL DEFAULT 'RUB',
          `amount` int(11) DEFAULT '0',
          `body` varchar(255) NOT NULL DEFAULT '',
          `weight` int(11) NOT NULL DEFAULT '0',
          `unitWeight` varchar(255) NOT NULL DEFAULT 'г',
          PRIMARY KEY (`id`)
        ) ENGINE=InnoDB AUTO_INCREMENT=21 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci



## Composer

`composer update the-package/you-want-to-update`  - обновление зависимостей добавленных в ручну в composer.json
composer dumpautoload  - включение автозагрузки классов при соответствующей установки в конфигурации  



## Установка php и т.д.
sudo add-apt-repository ppa:ondrej/php  
sudo apt update  
sudo apt -y install php7.2 php7.2-fpm php7.2-mysql php7.2-mbstring php7.2-xml php7.2-gd php7.2-curl php-common php7.2-cli php7.2-common php7.2-json php7.2-opcache php7.2-readline  
sudo apt -y install php libapache2-mod-php  

https://gitlab.com/dev-coach/myapp/-/blob/master/back/Dockerfile

php -m  - выводит список установленных разрешений 

php mycli.php    

sudo update-alternatives --config php   - смена версии php



## Symfony  

symfony server:start -d - запуск сервера
symfony server:log - зупуск просмотра логов в реальном времени в командной строке   
symfony server:status  

symfony serve --port=8010 -d  
symfony proxy:start 

symfony run -d --watch=config,src,templates,vendor symfony console messenger:consume async  -- При использовании параметра --watch Symfony перезапускает команду каждый раз при изменении файловой системы в директориях config/, src/, templates/ или vendor/.  
symfony run -d yarn encore dev --watch  
symfony console messenger:stop-workers  - остановить воркеры в том числе и watch'ер  

symfony open:local:webmail - доступ к почтовому серверу  



symfony var:export  - просмотр переменных окружения 

symfony console make:controller НазваниеКонтроллера  - создание класса контролера. В дериктории src/Controller/  

symfony console make:entity НазваниеКлассаСущности - создание класса сущности  
symfony console make:entity ПовторноеНазваниеКлассаСущности - для создание связей между таблицами нужно повторно вызвать функцию создания класса, но уже к существующему классу.  

symfony console debug:router
symfony console debug:container workflow  -- Если вы не можете вспомнить, какое должно быть правильное имя аргумента, то попробуйте воспользоваться командой debug:container. Выполните следующую команду, чтобы получить список сервисов, в имени которых содержится «workflow»:  

symfony console cache:clear  - очистить кэш


Миграция — это класс, описывающий изменения, необходимые для обновления схемы базы данных с текущего состояния на новое, определённой в аннотациях сущности.   
symfony console make:migration - миграция данных из классов в виде sql таблицы  
symfony console doctrine:migrations:migrate - орбновление локальной базы данных


## req - добавление зависимостей

symfony composer req profiler --dev   - Symfony Profiler поможет сэкономить много времени в поиске источника проблемы  
symfony composer req logger  - логирование действий  
symfony composer req debug --dev   - инструмент отладки  
symfony composer req validator - добавляе добавляем зависимость для валидатора  
symfony composer req phpunit --dev  - добавляем модуль тестирования PHPunit  
symfony composer req "dama/doctrine-test-bundle:^6" --dev   -   Для очистки базы данных между прогонами тестов  
symfony composer req messenger -- Компонент Messenger управляет асинхронным кодом в Symfony  
symfony composer req mailer  - модуль для электронной почты  
symfony composer req encore  -- установка Webpack Encore  
symfony composer req "imagine/imagine:^1.2" -- работа с картинками  
symfony composer req annotations  - Для работы с аннотациями нужно добавить ещё одну зависимость  
symfony composer req notifier - модуль уведомлений
symfony composer req api - для создания своего АПИ

symfony composer req "orm:^2"  - установка ORM для настройки Doctrine 

symfony composer req maker --dev  -  Для лёгкой генерации контроллеров  
symfony console list make  -  выводит список всех команд в указанном пространстве имен
symfony console make:unit-test SpamCheckerTest - создание образца для тестирования класса SpamChecker    

symfony console debug:autowiring encoder -  Если вы не помните, какой сервис вам нужно использовать для выполнения какой-либо задачи, воспользуетесь командой debug:autowiring, указав в качестве аргумента ключевое слово для поиска: encoder  


## Docker Compose

docker-compose up -d - запуск  
docker-compose ps  - проверить что все работает нормально. Должен быть статус up
docker-compose logs  


## MySQL

mysql -ucodercc -p1 -h0.0.0.0 -P49153 codercc

### Загрузка БД
Получается подключаемся к локальной базе данных указываем название, пароль, хост, -P и через знак меньше (<) указываем путь до базы данных если в другой папке находимся  mysql -ucodercc -p1 -h0.0.0.0 -P49153 codercc < ../codercc.2021-12-10-10.42.59.sql


## PostgreSQL

symfony run psql - запуск 

sudo -u postgres psql  - вход в срезу командной строки  
sudo -i -u postgres

psql -U postgres -d название_бд -p 5433 -f minimal_dblis_etalon_20230819.sql (название файла или адрес до него)


\du - список всех пользователей.   
\? перечислить все команды  
\l список баз данных  
\conninfo отображать информацию о текущем соединении  
\c [DBNAME] подключиться к новой базе данных, например, \c template1  
\d table_name  - чтобы увидеть детали таблицы, используйте:  
\dt список таблиц
Затем вы можете запустить операторы SQL, например, SELECT * FROM my_table; (Примечание: оператор должен заканчиваться точкой с запятой ;)  
\q выйти из psql  

\dt Список таблиц.  
\di Список индексов.  
\dv Список представлений.  
\df Список функций.  
\dn Список схем.  
\dx Список установленных расширений.  
\dp Список привилегий.  
\d имя - Подробная информация по конкретному объекту базы данных.  
\d+ имя - И еще более подробная информация по конкретному объекту.  
\timing on -  Показывать время выполнения операторов.  



Основные команды взяты отсюда https://edu.postgrespro.ru/introbook_v6.pdf  

CREATE DATABASE [название базы данных];  - создание базы данных  
\c [название базы данных] - переключиться на базу данных  
table courses ( c_no text primary key, title text, hours integer);  
INSERT INTO courses(c_no, title, hours) VALUES ('cs301', 'Базы данных', 30); - добавление данных в существующую таблицу  
SELECT title AS course_title, hours FROM courses;  - выборка данных  
SELECT * FROM courses;  - выбрать все данные из таблицы
"title AS course_title"  - переименовывает столбец при выводе данных  
SELECT DISTINCT start_year FROM students;   - DISTINCT - вывести уникальные поля  
SELECT * FROM courses WHERE hours > 45;  
SELECT courses.title, exams.s_id, exams.score FROM courses, exams WHERE courses.c_no = exams.c_no; 


##В системе отчетов
php bin/console app:createCurrentReport

crontab -e
0 1 1 * * php bin/console app:createCurrentReport


Запуск проекта - symfony proxy:start && docker-compose up -d && symfony serve --port=8010 -d


## LINUX Командная строка

 `fuser -k 8080/tcp` -  Убить процессы на порту 8080 текущего юзера    </br>
` lsof -ti tcp:8080` - Посмотреть какие процессы взаимодействуют с портом 8080    </br>



