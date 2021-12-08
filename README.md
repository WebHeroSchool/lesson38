# 1. Объявление переменных.
Для объявления переменных следует всегда использовать let или const. Если переменная не переназначается - следует использовать const.
#### Плохой пример 😠
``` js
    function func() { a = 9; }
```
#### Хороший пример 😃
``` js
    function func(){ let a=10; }
```
# 2. Объекты

Объекты (в том числе и массивы) следует объявлять через фигурные скобки
#### Плохо 😠
``` js
  const user = new Object();
  const cars = new Array();
```
#### Хорошо 😃
``` js   
  const user = {};
  const cars = [];
```
# 3. НЕ объявляйте числовые, строковые или логические объекты это снижает скорость выполнения кода.

#### Плохой пример 😠
``` js
    let catName = new String('Leo');
```
#### Хороший пример 😃
``` js
    let catName = 'Leo';
```
# 4. Размещать скрипты в конце страницы. `script` размещаем внутри тега `body` в конце
 Это делает загрузку страницы максимально быстрой для пользователя
# 5. Использовать camelCase для названий переменных, объектов и функций.
#### Плохой пример 😠
``` js
    const newlength = 10;
  function getNEWlength() {}
```
#### Хороший пример 😃
``` js
  const newLength = 10;
  function getNewLength() {}
```
- Используйте `extends` для наследования.
- #### Плохой пример 😠
``` js
    const inherits = require('inherits');
    function PeekableQueue(contents) {
    Queue.apply(this, contents);
}
    inherits(PeekableQueue, Queue);
    PeekableQueue.prototype.peek = function () {
    return this.queue[0];
};
```
#### Хороший пример 😃
``` js
class PeekableQueue extends Queue {
  peek() {
    return this.queue[0];
  }
}
```
# 6. Для всех многострочных блоков следует использовать фигурные скобки.
#### Плохой пример 😠
``` js
  if (test)
  return false;
  function foo() { return false; }
```
#### Хороший пример 😃
``` js
  if (test) return false;
  function foo() {
    return false;
  }
```
# 7. Точка с запятой

В конце выражения обязательна точка с запятой.
#### Плохой пример 😠
``` js
    alert('Привет')
    alert('Мир')
```
#### Хороший пример 😃
``` js
    alert('Привет');
    alert('Мир');
```
# 8. Следует использовать строгое сравнение (=== или !==) вместо нестрогого (== или !=).
Это позволяет избегать неяного преобразования типов.
#### Плохой пример 😠
``` js
  if (answer == 4) {
    console.log(true);
  }
  if (attempts != 0) {
    console.log('Ты пытался')
  }
```
#### Хороший пример 😃
``` js
   if (answer === 4) {
    console.log(true);
  }
  if (attempts !== 0) {
    console.log('Ты пытался')
  }
```
# 9. Пробелы
Следует использовать отступ 2 пробела
#### Плохой пример 😠
``` js
     if (answer == 4) {
     console.log(true);
  }
  if (attempts != 0) {
   console.log('Ты пытался')
  }
```
#### Хороший пример 😃
``` js
  if (answer === 4) {
    console.log(true);
  }
  if (attempts !== 0) {
    console.log('Ты пытался')
  }
```
# 10. Каждое новое свойства пишется с новой строки.

#### Плохой пример 😠
``` js
     const user = { firstName: "Петр", age: 43 }
```
#### Хороший пример 😃
``` js
       const user = { 
     firstName: "Петр", 
     age: 43 
     }
```
