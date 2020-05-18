# Comands
Тут хранятся разные команды



npm init -y  - установка самого NPM в папку с проектом </br>
npm install babel-cli babel-core babel-preset-es2015 --save-dev   - установка Babel находясь в корне проекта</br>
npx babel src --out-dir dist   - добавление соответствующих папок</br>

npm i bootstrap --save--dev   - усиаервмит будстрап </br>

npm uninstall bootstrap   -  удалить установленный пакет </br>

---------------------
HtmlWebpackPlugin. Этот плагин также позволяет автоматически встраивать в html созданные вебпаком бандлы.</br>


------
npm install --save--dev clean-webpack-plugin  - этот плагин удаляет файлы перед тем как билдить заново, чтобы не создавалось дублей
const {CleanWebpackPlugin} = require('clean-webpack-plugin');  добавить в webpack.config.js </br>
и там же в раздел  plugins    new CleanWebpackPlugin(), 


----
Сначала нужно установить плагин с помощью команды </br>

> npm i -D  html-webpack-plugin</br>

Используем флаг -D (save-dependencies) потому, что этот пакет нам нужен только для этапа разработки. Для функционирования конечного приложения этот пакет не нужен.</br>
-------------------



npm i   -  установить все пакеты которые есть в package.json - если он есть как отдельный файл со сборкой проекта.

Для файла packadge.json изменить


  "scripts": {</br>
    "bild": "babel src -d -dist -presets es2015",</br>
    "watch": "babel src -d -dist -presets es2015 -w"</br>
  },
 
"build": "babel src -d -dist -presets es2015",   -  "src" название папки в корне откуда будет браться код es2015 и "-dist" куда он будет компелироваться в старом формате.
 
 "watch": "babel src -d -dist -presets es2015 -w"  - автоматическое компилирование после сохранения. 


npm run build  - запуск  билда</br>
npm run watch - запуск смотрителя </br>

npm run dev  - запуск веб сервера</br>



Команды GIT

git -inint   - создать репазиторий гит</br>
echo >> README.md - создаем папку </br>
git config --local user.email "тут вводим емаил"</br>
git config --local user.name "тут вводим имя"</br>


git add -A  - добавляем все файлы в гит</br>
git commit -m "initial commit"</br>

git status</br>

git commit -a -m "Первый коммит"  - добавляем коммит</br>
git add *.html   -добавляем только файлы формата </br>

git push origin master

git log</br>
 

git remote add origin https://github.com/SkorihV/tickets-project.git   - привязка локального хранилища к виртуальному </br>


{
 	"word_separators": "`~!@#$%^&*()=+[{]}\\|;:'\",.<>/?"
}







