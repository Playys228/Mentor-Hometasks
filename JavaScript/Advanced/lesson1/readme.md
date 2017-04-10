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
