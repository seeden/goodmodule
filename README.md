# goodmodule
Be a better web developer. JavaScript tips for everybody. (One new tip every day)

## Be a better web developer and follow
- [www.goodmodule.com](http://www.goodmodule.com)
- [Github](https://github.com/seeden/goodmodule.com)
- [Instagram](https://www.instagram.com/goodmodule/)
- [Facebook](https://www.facebook.com/goodmodule/)

## Content

###[Frameworks / libraries differences](#frameworks) 
1. [Loop Statement](#frameworks-loop-statement)
  
<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-js.jpg"/>
### [JavaScript](#javascript) 
1. [Measuring Execution Times](#measuring-execution-time)
2. [Be careful with typeof](#typeof)
3. [Generate Random Number](#random) 

<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-es6.png"/>
###[ECMAScript 6](#es6) 
1. [Template Strings](#template-strings)
2. [Destructuring Assignment](#destructuring-assignment)
3. [Multi-line Strings](#multiline-strings)
4. [Arrow Functions](#arrow-functions)


 
## <a name="frameworks"></a>Frameworks / libraries differences

### 1. <a name="frameworks-loop-statement"></a>Loop Statement

| Framework  | syntax              |
|------------|---------------------|
| <img width="30" height="30" align="right" src="http://daynin.github.io/clojurescript-presentation/img/react-logo.png"/> React      | just use javascript |
| <img width="30" height="30" align="right" src="https://angular.io/resources/images/logos/angular2/angular.png"/> Angular 1  | ng-repeat           |
| <img width="30" height="30" align="right" src="https://pbs.twimg.com/media/CXkqdv5WMAACBvV.png"/> Angular 2  | ngFor               |
| <img width="30" height="30" align="right" src="https://cdn-images-2.medium.com/max/800/0*S1z4w1dGbfKxh7UI."/> Ember      | {{#each }}          |
| <img width="30" height="30" align="right" src="http://quintagroup.com/cms/js/js-image/knockout-js-logo.png"/> Knockout   | data-bind="foreach" |
| <img width="30" height="30" align="right" src="http://unbug.github.io/gdg14/resources/images/p-logo.svg"/> Polymer    | is="dom-repeat"     |
| <img width="30" height="30" align="right" src="https://vuejs.org/images/logo.png"/> Vue        | v-for               |
| <img width="30" height="30" align="right" src="https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcSXZPA7EUIFbdc4Buk1BgyWPOjv5SXJrVl3vpVOSFCiBhZH9isNcg"/> Aurelia    | repeat.for          |


## <a name="javascript"></a>JavaScript

<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-js.jpg"/>
### 1. <a name="measuring-execution-time"></a>Measuring Execution Times
```js
console.time('1000-iterations');

for( var i = 0; i < 1000; i++) {
  // your code
}

console.timeEnd('1000-iterations');
// Prints 1000-iterations: 25.438ms
```

Compatibility

| Chrome | Firefox | Internet Explorer | Opera | Safari | Node |
|--------|---------|-------------------|-------|--------|------|
| 2      | 10      | 11                | 9     | 4      | 0.1  |



<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-js.jpg"/>
### 2. <a name="typeof"></a>Be careful with typeof
```js
typeof null === 'object'; // true
typeof [1, 2] === 'object'; // true
typeof class C {} === 'function'; // true
typeof NaN === 'number'; // true
// NaN means "Not-A-Number"
```

Compatibility

| Chrome | Firefox | Internet Explorer | Opera | Safari | Node |
|--------|---------|-------------------|-------|--------|------|
| Yes    | Yes     | Yes               | Yes   | Yes    | Yes  |



<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-js.jpg"/>
### 3. <a name="random"></a>Generate Random Number
```js
// Get a float random number between <min, max)
function getRandom(min, max) {
  return Math.random() * (max - min) + min;
}

// Get an integer random number between <min, max)
function getRandomInt(min, max) {
  return Math.floor(Math.random() * (max - min)) + min;
}

var floatNumber = getRandom(1, 3); // 1.5392530886177522
var intNumber = getRandomInt(1, 3); // 2
```

Compatibility

| Chrome | Firefox | Internet Explorer | Opera | Safari | Node |
|--------|---------|-------------------|-------|--------|------|
| Yes    | Yes     | Yes               | Yes   | Yes    | Yes  |


## <a name="es6"></a>ECMAScript 6

<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-es6.png"/>
### 1. <a name="template-strings"></a>Template Strings
```js
var first = 'Zlatko';
var last = 'Fedor';

// ECMAScript 5
var msg = 'Hi ' + first + ' ' + last;
msg === 'Hi Zlatko Fedor'; // true

// ECMAScript 6
var msg = `Hi ${first} ${last}`;
msg === 'Hi Zlatko Fedor'; // true
```

Compatibility

| Chrome | Firefox | Edge | Opera | Node | Babel  | Safari |
|--------|---------|------|-------|------|--------|-------|
| 41     | 34      | 12   | 28    | 4    | 5      | 9     |

<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-es6.png"/>
### 2. <a name="destructuring-assignment"></a>Destructuring Assignment
```js
var user = {
  first: 'Zlatko',
  last: 'Fedor',
};

// ECMAScript 5
var first = user.first; // first === 'Zlatko'
var last = user.last; // last === 'Fedor'

// ECMAScript 6
var { first, last } = user;
first === 'Zlatko'; // true
last === 'Fedor'; // true
```

Compatibility

| Chrome | Firefox | Edge | Node | Babel | Safari |
|--------|---------|------|------|--------|-------|
| 49     | 2       | 14   | 6    | 5      | 7.1   |

<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-es6.png"/>
### 3. <a name="multiline-strings"></a>Multi-line Strings

```js
// ECMAScript 5 
var msg = 'This is\n' + 
  'multi-line string';

// ECMAScript 6
var msg = `This is
multi-line string`;

`\`` === "`" // true
```

Compatibility

| Chrome | Firefox | Edge | Opera | Node | Babel  | Safari |
|--------|---------|------|-------|------|--------|--------|
| 41     | 34      | 12   | 28    | 4    | 5      | 9      |

<img width="30" height="30" align="right" src="http://happykiwis.co.nz/public/goodmodule/logo-es6.png"/>
### 4. <a name="arrow-functions"></a>Arrow Functions

```js
var nums = [1, 2, 3];

//ECMAScript 5
var squares = nums.map(function (x) { 
  return x * x;
});

//ECMAScript 6
var squares = nums.map((x) => x * x);

// squares === [1, 4, 9]
```

Compatibility

| Chrome | Firefox | Edge | Opera | Node | Babel  | Safari |
|--------|---------|------|-------|------|--------|--------|
| 45     | 22      | 12   | 32    | 4    | 5      | No     |



## Be a better web developer and follow
- [www.goodmodule.com](http://www.goodmodule.com)
- [Github](https://github.com/seeden/goodmodule.com)
- [Instagram](https://www.instagram.com/goodmodule/)
- [Facebook](https://www.facebook.com/goodmodule/)
 
