# Comands
Тут хранятся разные команды



npm init -y  - установка самого NPM в папку с проектом </br>
npm install babel-cli babel-core babel-preset-es2015 --save-dev   - установка Babel находясь в корне проекта



Для файла packadge.json изменить


  "scripts": {</br>
    "bild": "babel src -d -dist -presets es2015",</br>
    "watch": "babel src -d -dist -presets es2015 -w"</br>
  },
 
"bild": "babel src -d -dist -presets es2015",   -  "src" название папки в корне откуда будет браться код es2015 и "-dist" куда он будет компелироваться в старом формате.
 
 "watch": "babel src -d -dist -presets es2015 -w"  - автоматическое компилирование после сохранения. 


npm run bild  - запуск  билда
npm run watch - запуск смотрителя 



Команды GIT

git -inint   - создать репазиторий гит</br>
echo >> README.md - создаем папку </br>
git config --local user.email "тут вводим емаил"</br>
git config --local user.name "тут вводим имя"</br>

git add -A  - добавляем все файлы в гит</br>
git status</br>

git commit -a -m "Первый коммит"  - добавляем коммит</br>
git add *.html   -добавляем только файлы формата </br>

git log</br>
 



