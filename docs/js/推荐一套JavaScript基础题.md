原文链接： https://perfectionkills.com/javascript-quiz-es6/

### 1、
```
(function(x, f = () => x) {
  var x;
  var y = x;
  x = 2;
  return [x, y, f()];
})(1)
```
### 2、
```
(function() {
  return [
    (() => this.x).bind({ x: 'inner' })(),
    (() => this.x)()
  ]
}).call({ x: 'outer' });
```
### 3、
```
let x, { x: y = 1 } = { x }; y;
```
### 4、
```
(function() {
  let f = this ? class g { } : class h { };
  return [
    typeof f,
    typeof h
  ];
})();
```
### 5、
```
(typeof (new (class { class () {} })))
```
### 6、
```
typeof (new (class F extends (String, Array) { })).substring

```
### 7、
```
[...[...'...']].length

```
### 8、
```
typeof (function* f() { yield f })().next().next()

```
### 9、
```
typeof (new class f() { [f]() { }, f: { } })[`${f}`]

```
### 10、
```
typeof `${{Object}}`.prototype

```
### 11、
```
((...x, xs)=>x)(1,2,3)

```
### 12、
```
let arr = [ ];
for (let { x = 2, y } of [{ x: 1 }, 2, { y }]) { 
  arr.push(x, y);
}
arr;
```
### 13、
```
(function() {
  if (false) {
    let f = { g() => 1 };
  }
  return typeof f;
})()
```
