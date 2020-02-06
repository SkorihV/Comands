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
