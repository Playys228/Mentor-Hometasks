};

var number = t.y;

number += 5;

console.log(t.y, number); // ?

```

#### 4.2

```
var t = {
    y: [1, 3, 5, 7]
};

var number = t.y[2];

for(var i = 0, len = t.y.length; i < len; i++) {
    t.y[i]++;
}

console.log(number); // ?

```

#### 4.3

```
var t = 9;

var obj = {
    number: t
};

obj.number++;

console.log(obj.number, t);
```
