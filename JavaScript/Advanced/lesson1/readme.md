## 1 task

При выполнении этого кода вызов rabbit.eat() запишет в объект свойство full.

Вопрос — в какой объект: в rabbit или animal?

```javascript
var animal = { };
var rabbit = { };

rabbit.__proto__ = animal;

animal.eat = function() {
    this.full = true;
};

rabbit.eat();
```

## 2 task

Какие значения будут выводиться в коде ниже?

```javascript
var animal = { jumps: null };
var rabbit = { jumps: true };

rabbit.__proto__ = animal;

alert( rabbit.jumps ); // ? (1)

delete rabbit.jumps;
alert( rabbit.jumps ); // ? (2)

delete animal.jumps;
alert( rabbit.jumps);  // ? (3)
```

## 3 task

Есть объекты:

```javascript
var head = {
  glasses: 1
};

var table = {
  pen: 3
};

var bed = {
  sheet: 1,
  pillow: 2
};

var pockets = {
  money: 2000
};
```

Задание состоит из двух частей:

1. Присвойте объектам ссылки __proto__ так, чтобы любой поиск чего-либо шёл по алгоритму pockets -&gt; bed -&gt; table -&gt; head. То есть pockets.pen == 3, bed.glasses == 1, но table.money == undefined.
2. После этого ответьте на вопрос, как быстрее искать glasses: обращением к pockets.glasses или head.glasses? Попробуйте протестировать.

## 4 task

В примерах ниже производятся различные действия с prototype.

Каковы будут результаты выполнения? Почему?

```javascript
function Rabbit() { }
Rabbit.prototype = { eats: true };

var rabbit = new Rabbit();

Rabbit.prototype = {};

alert(rabbit.eats);
А если код будет такой? (заменена одна строка):

function Rabbit(name) { }
Rabbit.prototype = { eats: true };

var rabbit = new Rabbit();

Rabbit.prototype.eats = false; // (*)

alert(rabbit.eats);
А такой? (заменена одна строка)

function Rabbit(name) { }
Rabbit.prototype = { eats: true };

var rabbit = new Rabbit();

delete Rabbit.prototype.eats; // (*)

alert(rabbit.eats);
```

А если бы в последнем коде вместо строки (*) было delete rabbit.eats?

## 5 task

Создадим новый объект, вот такой:

```javascript
function Rabbit() { }
Rabbit.prototype.test = function() { alert(this); }

var rabbit = new Rabbit();
```
Есть ли разница между вызовами:

```javascript
rabbit.test();
rabbit.__proto__.test();
Rabbit.prototype.test();
Object.getPrototypeOf(rabbit).test();
```

Какие из этих вызовов идентичны в браузере IE9+? А в Chrome?

## 6 task

Вы — руководитель команды, которая разрабатывает игру, хомяковую ферму. Один из программистов получил задание создать класс «хомяк» (англ - "Hamster").

Объекты-хомяки должны иметь массив food для хранения еды и метод found, который добавляет к нему.

Ниже — его решение. При создании двух хомяков, если поел один — почему-то сытым становится и второй тоже.

В чём дело? Как поправить?

```javascript
function Hamster() {  }

Hamster.prototype.food = [ ]; // пустой "живот"

Hamster.prototype.found = function(something) {
  this.food.push(something);
};

// Создаём двух хомяков и кормим первого
speedy = new Hamster();
lazy = new Hamster();

speedy.found("яблоко");
speedy.found("орех");

alert(speedy.food.length); // 2
alert(lazy.food.length);   // 2 (!??)
```
