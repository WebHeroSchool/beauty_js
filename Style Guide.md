# JavaScript Style Guide 

## 1. Понятные имена переменных и функций
Код легче читать, когда при написании используются понятные, описательные имена функций и переменных, отражающие их смысл. Имена функций - это глаголы. Имена переменных - существительные.

*Правильный вариант*
``` js
function toCube(num) {
    let result = num * num * num;
    return result;
}
```
*Неправильный вариант*
``` js
function wr(a) {
    let b = a * a *a;
    return b;
}
```
## 2. Зарезервированные слова
Не используйте зарезервированные слова в качестве ключей объектов.

*Правильный вариант*
``` js
let superman = {
  defaults: { clark: 'kent' },
  hidden: true
};
```
*Неправильный вариант*
``` js
let superman = {
  default: { clark: 'kent' },
  private: true
};
```
## 3. Имена переменных на английском языке
Имена переменных и функций не нужно писать транслитом, необходимо использовать английский язык.

*Правильный вариант*
``` js
let house = {};
let name = '';
function editName(name) {
    //тело функции
}
```
*Неправильный вариант*
``` js
let dom = {};
let imya = '';
function pravkaImeni(imya) {
    //тело функции
}
```
## 4. Скобки
Открывающая фигурная скобка располагается на той же строке. Перед скобкой пробел. Закрывающая скобка располагается на новой строке.

*Правильный вариант*
``` js
function edit(name, age) {
  if (age < 100) {
    // тело цикла
  }
}
```
*Неправильный вариант*
``` js
function edit(name, age)
{
  if (age < 100) { /*тело цикла*/ }
}
```
## 5. Точка с запятой
Каждое предложение должно отделяться точкой с запятой. Полагаться на автоматическую вставку точек с запятыми запрещается.

*Правильный вариант*
``` js
alert('Hello');
let person = {};
person.name = 'Kate';
```
*Неправильный вариант*
``` js
alert('Hello')
let person = {}
person.name = 'Kate'
```

## 6. Не использовать var
Объявляйте все переменные с помощью const или let. По умолчанию используется const, за исключением случаев, кгда нужно переназначить переменную. Ключевое слово var не должно использоваться.

*Правильный вариант*
``` js
const five = 5;
function toCube(num) {
    let result = num * num * num;
    return result;
}
let fiveInCube = toCube(five);
```
*Неправильный вариант*
``` js
var five = 5;
function toCube(num) {
    var result = num * num * num;
    return result;
}
var fiveInCube = toCube(five);
```

## 7. Использовать одинарные, а не двойные кавычки
Обычные строковые литералы ограничиваются одинарной кавычкой (''), а не двойной ("").

*Правильный вариант*
``` js
let person = {
    name: 'Kate',
    surname: 'Nikishina',
    age: 21
}
```
*Неправильный вариант*
``` js
let person = {
    name: "Kate",
    surname: "Nikishina",
    age: "21"
}
```

## 8. Менять стили через css, а не с помощью js
Вместо того, чтобы менять стили элементов через DOM
лучше создать класс с нужными стилями в файле style.css
и в коде javascript добавилять нужный класс со стилями 
элементу

*Правильный вариант*
``` js
let button = document.getElementById('main-button');
button.className.add('red');
```
*Неправильный вариант*
``` js
let button = document.getElementById('main-button');
button.style.padding = '20px';
button.style.background = 'red';
button.style.color = 'white';
button.style.fontWeight = 'bold';
}
```

## 9. Объявляйте переменные для 'for" вне циклов
 Цикл будет медленне работать, если ему придеться вычислять длинну массива, например, на каждой итерации. 

*Правильный вариант*
``` js
let names = ['Kate','Alex','Pavel','Marina'];
let all = names.length;
for(let i=0;i<all;i++){
  doSomeThingWith(names[i]);
}
```
*Неправильный вариант*
``` js
let names = ['Kate','Alex','Pavel','Marina'];
for(let i = 0; i < names.length; i++){
  doSomeThingWith(names[i]);
}
```

## 10. Снижение числа глобальных переменных
Сведением количества глобальных переменных к минимуму, вы значительно снижаете шансы нежелательного взаимодействия с другими приложениями, виджетами или библиотеками

*Правильный вариант*
``` js
let DudeNameSpace = {  
   name : 'Jeffrey',  
   lastName : 'Way',  
   doSomething : function() {...}  
}  
console.log(DudeNameSpace.name);
```
*Неправильный вариант*
``` js
let name = 'Jeffrey';  
let lastName = 'Way';  
  
function doSomething() {...}  
  
console.log(name);
```
# Спасибо за прочтение!
![Welcome](https://octodex.github.com/images/welcometocat.png "Have a good day")