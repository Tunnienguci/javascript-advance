<h1 style="font-weight: bold; color: #5C8984"> JAVASCRIPT ADVANCE </h1>
<img src="https://techvccloud.mediacdn.vn/2018/11/23/js-15429579443112042672363-crop-1542957949936317424252.png" width="100%">
<img src="https://img.shields.io/badge/Author-Tunnienguci-blue" alt="Author" />
<img src="https://img.shields.io/badge/Version-1.0.0-red" alt="Version" />
<img src="https://img.shields.io/badge/Status-Completed-success"alt="Status" />

<h2 style="font-weight: bold; color: #374259">Type and Coercion / Các kiểu dữ liệu và ép kiểu</h2>
Trong JS có tất cả tổng cộng là 08 kiểu dữ liệu đó là: 

1. String
2. Number
3. Boolean
4. Undefined
5. Null
7. Object
8. Symbol
9. BigInt (ES2020)

Trong đó có Object là thuộc kiểu dữ liệu phức tạp (Reference Type) còn các kiểu kia là kiểu dữ liệu nguyên thủy (Primitive Type).
Trong kiểu dữ liệu Object có subtype chính và thường được sử dụng là:
- Function
- Array

<br><br>

<h3 style="font-weight: bold; color:#545B77"> Typeof </h3>
Để kiểm tra kiểu dữ liệu của một biến ta có thể sử dụng toán tử typeof. Toán tử typeof trả về một trong các giá trị sau:

- "string"
- "number"
- "boolean"
- "undefined"
- "object"
- "function"
- "symbol"
- "bigint"

<br><br>


<h3 style="font-weight: bold; color:#545B77"> Coercion </h3>
Coercion là quy trình chuyển đổi kiểu dữ liệu từ kiểu này sang kiểu khác. Coercion trong JS có 2 loại là:
- Implicit Coercion
- Explicit Coercion

<br><br>

<h3 style="font-weight: bold; color:#545B77"> Implicit Coercion </h3>
Implicit Coercion là quy trình chuyển đổi kiểu dữ liệu từ kiểu này sang kiểu khác mà không cần sử dụng toán tử chuyển đổi. Implicit Coercion thường xảy ra trong các trường hợp sau:
- Toán tử + với String
- Toán tử - * / với Number
- Toán tử == và !=
- Toán tử !!
- Toán tử || và &&
- Toán tử ??

Ví dụ:
```javascript
// Toán tử + với String
console.log(1 + "1"); // "11"
console.log(1 + "1" + 1); // "111"
console.log(1 + "1" + 1 + 1); // "1111"

// Toán tử - * / với Number
console.log(1 - "1"); // 0
console.log(1 * "1"); // 1
console.log(1 / "1"); // 1

// Toán tử == và !=
console.log(1 == "1"); // true
console.log(1 != "1"); // false

// Toán tử !!
console.log(!!"1"); // true
console.log(!!""); // false

// Toán tử || và &&
console.log(1 || "1"); // 1
console.log(1 && "1"); // "1"

// Toán tử ??
console.log(1 ?? "1"); // 1
console.log(0 ?? "1"); // 0
console.log(null ?? "1"); // "1"
```

<br><br>

<h3 style="font-weight: bold; color:#545B77"> Explicit Coercion </h3>
Explicit Coercion là quy trình chuyển đổi kiểu dữ liệu từ kiểu này sang kiểu khác mà cần sử dụng toán tử chuyển đổi. Coercion trong JS có 2 loại là:
- String()
- Number()
- Boolean()
- BigInt()
- Symbol()
- Object()
- Array()
- Function()

Ví dụ:
```javascript
// String()
console.log(String(1)); // "1"
console.log(String(true)); // "true"
console.log(String(null)); // "null"
console.log(String(undefined)); // "undefined"

// Number()
console.log(Number("1")); // 1
console.log(Number("1.1")); // 1.1
console.log(Number("1.1.1")); // NaN
console.log(Number(true)); // 1
console.log(Number(false)); // 0
console.log(Number(null)); // 0
console.log(Number(undefined)); // NaN

// Boolean()
console.log(Boolean("1")); // true
console.log(Boolean("")); // false
console.log(Boolean(1)); // true
console.log(Boolean(0)); // false
console.log(Boolean(null)); // false
console.log(Boolean(undefined)); // false

// BigInt()
console.log(BigInt(1)); // 1n
console.log(BigInt("1")); // 1n
console.log(BigInt("1.1")); // Error
console.log(BigInt(true)); // 1n
console.log(BigInt(false)); // 0n
console.log(BigInt(null)); // 0n
console.log(BigInt(undefined)); // Error

// Symbol()
console.log(Symbol(1)); // Symbol(1)
console.log(Symbol("1")); // Symbol(1)
console.log(Symbol("1.1")); // Symbol(1.1)
console.log(Symbol(true)); // Symbol(true)
console.log(Symbol(false)); // Symbol(false)

// Object()
console.log(Object(1)); // Number {1}
console.log(Object("1")); // String {"1"}
console.log(Object("1.1")); // String {"1.1"}
console.log(Object(true)); // Boolean {true}
console.log(Object(false)); // Boolean {false}
console.log(Object(null)); // Object {null}
console.log(Object(undefined)); // Object {undefined}

// Array()
console.log(Array(1)); // [empty]
console.log(Array("1")); // ["1"]
console.log(Array("1.1")); // ["1.1"]
console.log(Array(true)); // [true]
console.log(Array(false)); // [false]
console.log(Array(null)); // [null]
console.log(Array(undefined)); // [undefined]

// Function()
console.log(Function(1)); // ƒ anonymous()
console.log(Function("1")); // ƒ anonymous()

```

<br><br>

<h2 style="font-weight: bold; color: #374259">Truthy và Falsy </h2>
<b> Trong JS, có 7 giá trị được xem là Falsy và 7 giá trị được xem là Truthy. Các giá trị Falsy là: </b>
false
0
""
null
undefined
NaN
-0

Các giá trị Truthy là:
- true
- 1
- " "
- {}
- []
- function(){}

<br><br>

<h2 style="font-weight: bold; color: #374259"> Toán tử </h2>
<h3 style="font-weight: bold; color: #545B77"> Toán tử ++ và -- </h3>
Toán tử ++ và -- là toán tử tăng và giảm giá trị của biến lên 1 đơn vị. Toán tử ++ và -- có 2 cách sử dụng là:
- Toán tử tiền tố: ++a, --a
- Toán tử hậu tố: a++, a--

Ví dụ:
```javascript
// Toán tử tiền tố
let a = 1;
console.log(++a); // 2
console.log(a); // 2

// Toán tử hậu tố
let b = 1;
console.log(b++); // 1
console.log(b); // 2
```

<h3 style="font-weight: bold; color: #545B77"> Toán tử + và - </h3>
Toán tử + và - là toán tử chuyển đổi kiểu dữ liệu. Toán tử + và - có 2 cách sử dụng là:
- Toán tử tiền tố: +a, -a
- Toán tử hậu tố: a+, a-

Ví dụ:
```javascript
// Toán tử tiền tố
let a = "1";
console.log(+a); // 1
console.log(a); // "1"

// Toán tử hậu tố
let b = "1";
console.log(b+); // 1

```

<br><br>

<h2 style="font-weight: bold; color: #374259"> Scope, Lexical và Closure trong JS </h2>
<h3 style="font-weight: bold; color: #545B77">Scope</h3>
Scope là phạm vi hoạt động của biến. Trong JS, có 3 loại scope là:
- Global scope: là phạm vi hoạt động của biến toàn bộ chương trình.
- Local scope: là phạm vi hoạt động của biến trong 1 hàm.
- Block scope: là phạm vi hoạt động của biến trong 1 block code ({}).

Ví dụ:
```javascript
// Global scope
let a = 1;
console.log(a); // 1

// Local scope
function test() {
    let b = 2;
    console.log(b); // 2
}

// Block scope
{
    let c = 3;
    console.log(c); // 3
}
```
<br><br>


<h3 style="font-weight: bold; color:#545B77"> Lexical </h3>
Lexical là phạm vi hoạt động của biến trong 1 hàm. Lexical có 2 loại là:
- Lexical scope: là phạm vi hoạt động của biến trong 1 hàm.
- Lexical environment: là phạm vi hoạt động của biến trong 1 hàm và các hàm bên ngoài.

Ví dụ:
```javascript
// Lexical scope
function test() {
    let a = 1;
    console.log(a); // 1
}

// Lexical environment
function test() {
    let a = 1;
    function test2() {
        let b = 2;
        console.log(a); // 1
        console.log(b); // 2
    }
    console.log(a); // 1
    console.log(b); // Error
}
```

<br><br>

<h3 style="font-weight: bold; color:#545B77"> Closure </h3>
Closure là phạm vi hoạt động của biến trong 1 hàm và các hàm bên ngoài. Closure có 2 loại là:
- Closure scope: là phạm vi hoạt động của biến trong 1 hàm và các hàm bên ngoài.
- Closure environment: là phạm vi hoạt động của biến trong 1 hàm và các hàm bên ngoài và các biến bên ngoài.

Closure cho phép các hàm bên trong truy cập đến các biến khi function đó đã được hoàn thành xong.
Closures là cho phép truy cập và sử dụng biến từ phạm vi bên ngoài của nó ngay cả khi hàm đã kết thúc. Closures cho phép lưu trữ và duy trì trạng thái của biến, tạo ra một môi trường đóng gói những giữ liệu cần thiết.
Closure giúp ta có thể sử dụng các biến private trong JS.

Ví dụ:
```javascript
// Sử dụng Closure
function test() {
    let a = 1;
    function test2() {
        let b = 2;
        console.log(a); // 1
        console.log(b); // 2
    }
    console.log(a); // 1
    console.log(b); // Error
    return test2;
}

let test3 = test();
test3();
```
<br><br>

<h2 style="font-weight: bold; color: #E94057"> this trong JS </h2>
<h3 style="font-weight: bold; color:#545B77"> this trong đối tượng </h3>
this là một keyword được sử dụng để truy cập vào các thuộc tính và phương thức của đối tượng hiện tại. this có thể thay đổi giá trị tùy vào cách gọi hàm.

Ví dụ:
```javascript
let person = {
    name: "Nguyen Van A",
    age: 20,
    getName: function() {
        console.log(this.name);
    }
}

person.getName(); // Nguyen Van A
```
<br><br>

<h3 style="font-weight: bold; color:#545B77"> this trong hàm </h3>
Trong hàm, this có thể thay đổi giá trị tùy vào cách gọi hàm. Nếu gọi hàm thông thường thì this sẽ là window. Nếu gọi hàm thông qua phương thức của đối tượng thì this sẽ là đối tượng đó.

Ví dụ:
```javascript
function test() {
    console.log(this);
}

test(); // window

let person = {
    name: "Nguyen Van A",
    age: 20,
    getName: function() {
        console.log(this);
    }
}

person.getName(); // person
```
<br><br>

<h3 style="font-weight: bold; color:#545B77"> this trong class </h3>
Trong class, this sẽ là đối tượng được khởi tạo từ class đó.

Ví dụ:
```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }

    getName() {
        console.log(this);
    }
}

let person = new Person("Nguyen Van A", 20);
person.getName(); // Person { name: 'Nguyen Van A', age: 20 }
```
<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> Destructuring trong JS </h2>
Destructuring là cách khai báo biến từ các thuộc tính của một đối tượng.

Ví dụ:
```javascript
let person = {
    name: "Nguyen Van A",
    age: 20
}

let { name, age } = person;
console.log(name); // Nguyen Van A
console.log(age); // 20
```
<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> Rest parameter trong JS </h2>
REST parameter: REST parameter (cũng được gọi là rest operator) cho phép chúng ta truyền vào một số lượng tham số không xác định vào một hàm dưới dạng một mảng. Cú pháp của REST parameter là sử dụng dấu ba chấm "..." trước tên tham số cuối cùng của hàm. Ví dụ:

Ví dụ:
```javascript
function sum(...numbers) {
  let total = 0;
  for (let number of numbers) {
    total += number;
  }
  return total;
}

console.log(sum(1, 2, 3)); // Output: 6
console.log(sum(4, 5, 6, 7, 8)); // Output: 30
```
Trong ví dụ trên, REST parameter ...numbers cho phép hàm sum nhận vào một số lượng tham số không xác định và lưu trữ chúng trong một mảng có tên numbers. Chúng ta có thể sử dụng mảng numbers để tính tổng các số truyền vào.

<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> Spread operator trong JS </h2>
Spread operator: Spread operator cho phép chúng ta truyền một mảng vào một hàm có số lượng tham số không xác định. Cú pháp của spread operator là sử dụng dấu ba chấm "..." trước một mảng. 

Ví dụ:
```javascript
let numbers = [1, 2, 3, 4, 5];
console.log(...numbers); // Output: 1 2 3 4 5

let array1 = [6, 7, 8];
let array2 = [9, 10, ...array1, 11, 12];
console.log(array2); // Output: [9, 10, 6, 7, 8, 11, 12]
```

Trong ví dụ trên, Spread parameter ...numbers trải rải các phần tử trong mảng numbers thành các phần tử riêng lẻ khi in ra. Trong ví dụ thứ hai, chúng ta sử dụng Spread parameter để kết hợp các mảng lại với nhau và thêm các phần tử mới vào giữa.

<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> Hoisting trong JS </h2>
Trong JS như chúng ta đã biết rằng có các kiểu khai báo biến bằng var, let, const trong đó đa phần mọi người đều biết rằng chỉ var mới có thể hoisting còn các kiểu khai báo biến khác đều không. Nhưng thực tế thì tất cả đều có thể hoisting.
Engine của JS sẽ đọc code qua một lượt và tìm thấy cú pháp khai báo sau đó nó lưu vào bộ nhớ và sẽ hoisting lên đầu. 

Trong JS có 2 giai đoạn:
- Compile time: là giai đoạn mà engine sẽ đọc code và lưu vào bộ nhớ.
- Run time: là giai đoạn mà engine sẽ thực thi code.

Vì vậy var, let và const đều hoisting trong JS. Nhưng cách hoisting của nó khác nhau ở giai đoạn compile time và run time.
Đối với var thì giai đoạn compile time sẽ hoisting lên đầu và giai đoạn run time sẽ gán giá trị cho biến đó. Đối với let và const thì giai đoạn compile time sẽ hoisting lên đầu và giai đoạn run time sẽ gán giá trị cho biến đó và kiểm tra xem biến đó đã được khởi tạo chưa nếu chưa thì sẽ gán giá trị là undefined.

Đối với let và const thì ta không thể truy cập biến trước khi khai báo. Vì vậy khi khai báo biến bằng let và const thì ta phải khai báo trước khi truy cập.

Var có thể khai báo nhiều lần trong cùng một scope nhưng let và const thì không thể. Vì vậy khi khai báo biến bằng let và const thì ta phải khai báo duy nhất một lần trong cùng một scope. Nếu khai báo nhiều lần thì sẽ bị lỗi. 

Ví dụ:
```javascript
console.log(a); // undefined
var a = 1;
```

Ví dụ trên sẽ được hiểu như sau:
```javascript
var a;
console.log(a); // undefined
a = 1;
```

Ví dụ:
```javascript
console.log(a); // Error
let a = 1;
```

Ví dụ trên sẽ được hiểu như sau:
```javascript
let a;
console.log(a); // Error
a = 1;
```

Ví dụ:
```javascript
console.log(a); // Error
const a = 1;
```

Ví dụ trên sẽ được hiểu như sau:
```javascript
const a;
console.log(a); // Error
a = 1;
```
<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> forEarch, map, filter, reduce trong JS </h2>
<h3 style="font-weight: bold; color:#545B77"> forEach </h3>
forEach là một hàm của array để duyệt qua từng phần tử của array. Hàm forEach sẽ nhận vào một hàm callback và thực thi hàm callback đó cho từng phần tử của array. Hàm callback sẽ nhận vào 3 tham số là phần tử, vị trí của phần tử và array.

Ví dụ:
```javascript
let arr = [1, 2, 3, 4, 5];
arr.forEach(function(item, index, array) {
    console.log(item, index, array);
});
```
<br><br>

<h3 style="font-weight: bold; color:#545B77"> map </h3>
map là một hàm của array để duyệt qua từng phần tử của array. Hàm map sẽ nhận vào một hàm callback và thực thi hàm callback đó cho từng phần tử của array. Hàm callback sẽ nhận vào 3 tham số là phần tử, vị trí của phần tử và array. Sau đó hàm map sẽ trả về một array mới với các phần tử được thay đổi bởi hàm callback.

Ví dụ:
```javascript
let arr = [1, 2, 3, 4, 5];
let newArr = arr.map(function(item, index, array) {
    return item * 2;
});
console.log(newArr); // [2, 4, 6, 8, 10]
```
<br><br>

<h3 style="font-weight: bold; color:#545B77"> filter </h3>
filter là một hàm của array để duyệt qua từng phần tử của array. Hàm filter sẽ nhận vào một hàm callback và thực thi hàm callback đó cho từng phần tử của array. Hàm callback sẽ nhận vào 3 tham số là phần tử, vị trí của phần tử và array. Sau đó hàm filter sẽ trả về một array mới với các phần tử được thay đổi bởi hàm callback. Nếu hàm callback trả về true thì phần tử đó sẽ được thêm vào array mới, nếu hàm callback trả về false thì phần tử đó sẽ không được thêm vào array mới.

Ví dụ:
```javascript
let arr = [1, 2, 3, 4, 5];
let newArr = arr.filter(function(item, index, array) {
    return item % 2 === 0;
});

console.log(newArr); // [2, 4]
```
<br><br>

<h3 style="font-weight: bold; color:#545B77"> reduce </h3>
reduce là một hàm của array để duyệt qua từng phần tử của array. Hàm reduce sẽ nhận vào một hàm callback và thực thi hàm callback đó cho từng phần tử của array. Hàm callback sẽ nhận vào 4 tham số là phần tử, vị trí của phần tử, array và giá trị trả về của lần thực thi trước. Sau đó hàm reduce sẽ trả về giá trị của lần thực thi cuối cùng.

Ví dụ:
```javascript
let arr = [1, 2, 3, 4, 5];
let sum = arr.reduce(function(total, item, index, array) {
    return total + item;
}, 0);

console.log(sum); // 15
```
<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> Callback trong JS </h2>
Callback là một hàm được truyền vào một hàm khác như một tham số. Hàm nhận vào hàm callback sẽ thực thi hàm callback đó.

Ví dụ:
```javascript
function sayHello(callback) {
    callback();
}

function sayHi() {
    console.log('Hi');
}

sayHello(sayHi); // Hi
```
<br><br>
<br><br>

<h2 style="font-weight: bold; color: #374259"> Promise trong JS </h2>
Promise là một đối tượng được sử dụng để thực thi một hàm bất đồng bộ. Promise sinh ra để giải quyết vấn đề callback hell để lại. Và Promise
có 2 trạng thái là pending và settled. Trạng thái settled có 2 trạng thái con là fulfilled và rejected.
Trong promise có 3 phương thức là then, catch và finally. Phương thức then sẽ được gọi khi promise được resolved, phương thức catch sẽ được gọi khi promise được rejected và phương thức finally sẽ được gọi khi promise được resolved hoặc rejected.

Ví dụ:
```javascript
let promise = new Promise(function(resolve, reject) {
    setTimeout(function() {
        resolve('Success');
    }, 1000);
});

promise.then(function(result) {
    console.log(result);
}).catch(function(error) {
    console.log(error);
}).finally(function() {
    console.log('Done');
});
```
<br><br>

Các method của Promise:
- Promise.all(): Phương thức này sẽ nhận vào một array các promise và trả về một promise mới. Promise mới sẽ được resolved khi tất cả các promise được truyền vào đều được resolved và sẽ được rejected khi ít nhất một promise được truyền vào bị rejected. Nếu promise mới được resolved thì giá trị trả về của promise mới sẽ là một array các giá trị trả về của các promise được truyền vào. Nếu promise mới được rejected thì giá trị trả về của promise mới sẽ là giá trị của promise được truyền vào bị rejected đầu tiên.

Ví dụ:
```javascript
let promise1 = new Promise(function(resolve, reject) {
    setTimeout(function() {
        resolve('Success 1');
    }, 1000);
});

let promise2 = new Promise(function(resolve, reject) {
    setTimeout(function() {
        resolve('Success 2');
    }, 2000);
});

let promise3 = new Promise(function(resolve, reject) {
    setTimeout(function() {
        resolve('Success 3');
    }, 3000);
});

Promise.all([promise1, promise2, promise3]).then(function(result) {
    console.log(result); // ['Success 1', 'Success 2', 'Success 3']
}).catch(function(error) {
    console.log(error);
});
```
<br><br>
<br><br>


<h2 style="font-weight: bold; color: #374259"> Async/Await trong JS </h2>
Async/Await là một cách để thực thi một hàm bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ. Async/Await là một cách để viết code đồng bộ nhưng vẫn có thể thực thi bất đồng bộ.

Ví dụ:
```javascript
async function sayHello() {
    return 'Hello';
}

sayHello().then(function(result) {
    console.log(result); // Hello
});
```

Async function sẽ luôn trả về một promise. Nếu async function trả về một giá trị thì promise sẽ được resolved với giá trị đó. Nếu async function throw một lỗi thì promise sẽ được rejected với lỗi đó.

Ví dụ:
```javascript
async function sayHello() {
    return 'Hello';
}

sayHello().then(function(result) {
    console.log(result); // Hello
});

async function sayHello() {
    throw new Error('Error');
}

sayHello().catch(function(error) {
    console.log(error); // Error
});
```
<br><br>

Await là một keyword được dùng để đợi một promise được resolved hoặc rejected. Await chỉ có thể được dùng trong async function. Khi dùng await, async function sẽ đợi đến khi promise được resolved hoặc rejected và trả về giá trị của promise đó.

Ví dụ:
```javascript
async function sayHello() {
    let promise = new Promise(function(resolve, reject) {
        setTimeout(function() {
            resolve('Hello');
        }, 1000);
    });

    let result = await promise;
    console.log(result); // Hello
}

sayHello();
```

Ví dụ:
```javascript
async function sayHello() {
    let promise = new Promise(function(resolve, reject) {
        setTimeout(function() {
            reject(new Error('Error'));
        }, 1000);
    });

    try {
        let result = await promise;
        console.log(result);
    } catch(error) {
        console.log(error); // Error
    }
}

sayHello();
```

