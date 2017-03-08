## 1 task 

#### Hoisting или "поднятие переменных"? Что произойдет при выполнении следующего куска кода?

```javascript
myname = "global";
function func() {
    console.log(myname);
    var myname = "local";
    console.log(myname);
}
func();
```

## 2 task 

#### Какие языковые конструкции в javascript создают scope? Что произойдет при выполнении следующего куска кода?

```javascript
var a = 90100;
function someFunc(){
  if(false){
    var a = 1;
  } else {
    var b = 2;
  }
  console.log(b);
  console.log(a);
}
someFunc();
```

## 3 task

#### На что ссылаеться this в следующем фрагменте кода?

```javascript
function test() {
  this;
}
test();
```

## 4 task

#### Что такое глобальные переменные ? Как они создаются ? Какие проблемы связаны с использованием глобальных переменных?

// напишите ответы на вопросы своими словами

## 5 task 

#### Почему вызов a(); происходит успешно, а вызов b(); выдает ошибку?

```javascript
a(); //ok
b(); //error

var b = function(){
 alert( 'function b');
}

function a(){
 alert( 'function a' );
}
```

## 6 task 

#### Что выведет в консоль следующий код:

```javascript
var i = 0;

for (; i< 10; i ++) {
  console.log(i)
}
```
## 7 task 

Напишите функцию подсчета факториала числа, но каждый раз возвращая факториал умножайте его на 2 если число четное.

## 8 task

Подсчитайте время выполнения выше написанной вами функции c помощью объекта console.
