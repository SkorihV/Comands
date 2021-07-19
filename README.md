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

`git -inint`   - создать репазиторий гит</br>
`echo >> README.md` - создаем папку </br>
`git config --local(--global) user.email` "тут вводим емаил"</br>
`git config --local(--global) user.name` "тут вводим имя"</br>

`git status`</br>

git diff ветка1 ветка2 - посмотреть чем отличаются две эти ветки  
git diff --name-only ветка1 ветка2 -  посмотреть не сами отличия, а список отличающихся файлов  

`git log`  - показывает все коммиты сделанные в данной ветке</br>
`gi cat-file -p *****` - посмотреть какие файлы есть. в звездочках первые пять сиволов названия файла с хешом.</br>

`git checkout -b` название_ветки  - создать и перейти в новую ветку (команда разовая)</br>
`git checkout` название_ветеки - просто перейти на другую ветку </br>

`git add -A`  - добавляем все файлы в гит чтобы он о них знал, это нужно делать перед комитом</br>
`git add *.html`   -добавляем только файлы формата </br>

`git commit -m "Сообщение к коммиту"`  - перед тем как запушить данные в гитхаб, их нужно закомитеть</br>
`git commit -a -m "Первый коммит"`  - добавляем коммит</br>


`git push origin master`  - залить локальные изменения на ветку master на гитхабе</br>

`git pull origin название_ветки` - скачать обновления с репозитория</br>  

<hr>
`git remote update origin` - обновит ваши локальные ветви отслеживания.  

`git remote show origin` сравнивает ваш локальный репозиторий с удаленным:

`fast-forwardable` означает, что вы можете отправить свои локальные изменения в удаленную ветку.
`local out of date` означает, что ваша локальная ветка находится за удаленной веткой, и вы должны извлечь из нее.
`git status`  сравнивает ваш локальный рабочий каталог с текущей фиксацией текущей ветки (также известной как HEAD). Кроме того, он сравнивает вашу локальную ветку с (локальной!) Копией отслеживания удаленной ветки ( `origin/master`), следовательно,Your branch is ahead of 'origin/master' by 5 commits.

Чтобы устранить расхождение между `git status` (который показывает только локальные данные) и `git remote show origin` (который показывает "живые" удаленные данные), вы должны запустить, `git remote update origin` который обновит ваши локальные ветви отслеживания. Он обновит ваш локальный origin/masterдо состояния удаленного master. После этого `git status` вы должны получить что-то вроде `Your branch is behind 'origin/master' by X commits, and can be fast-forwarded`.

<hr>

`gitk --all&`  - открыть графический интерфейс по гиту, но нужно через консоль гит    


### Чтобы соединить ветки:</br>

--------
`git checkout master` - перейти в ветку master</br>
`git merge название_ветки_которую_сливаем_с_мастером`</br>

`git branch -D название_ветки` - удаление ветки</br>

`git branch` - показывает какие ветки сейчас существуют</br>
`git branch -v` - увидим ветки и часть хеша коммита</br>


 

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

products | CREATE TABLE `products` ( `id` int(11) NOT NULL AUTO_INCREMENT,`name` varchar(255) NOT NULL,`price` int(11) DEFAULT '0',`article` varchar(255) NOT NULL DEFAULT '',`currency` varchar(255) NOT NULL DEFAULT 'RUB',`amount` int(11) DEFAULT '0',`body` varchar(255) NOT NULL DEFAULT '',`weight` int(11) NOT NULL DEFAULT '0',`unitWeight` varchar(255) NOT NULL DEFAULT 'г',PRIMARY KEY (`id`)) ENGINE=InnoDB AUTO_INCREMENT=21 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci



## Composer

`composer update the-package/you-want-to-update`  - обновление зависимостей добавленных в ручну в composer.json

