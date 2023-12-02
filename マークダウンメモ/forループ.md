- [forループ](#forループ)
  - [forループの基本](#forループの基本)
    - [具体的な使用例](#具体的な使用例)
  - [for...in](#forin)
    - [for...inループの具体例](#forinループの具体例)
  - [for...ofループ](#forofループ)
    - [for...ofループの具体例](#forofループの具体例)
# forループ

## forループの基本
forループはプログラムで反復処理を行うための制御構造の一つです。特定の条件の下で同じ処理を繰り返し実行することができます。

forループの基本構文は以下のようになります:

```javascript
for (初期化式; 条件式; 更新式) {
  // 繰り返し実行する処理
}
```

それぞれの部分について説明します:

1. 初期化式: ループの最初に一度だけ実行される式です。通常は変数の初期化やカウンターの設定などが行われます。

2. 条件式: 各反復の前に評価される式です。条件が真（true）の場合、ループのブロック内の処理が実行されます。条件が偽（false）の場合、ループは終了します。

3. 更新式: 各反復の最後に実行される式です。通常はカウンターの値の更新や変数の変化などが行われます。

4. ループのブロック内の処理: ループ内で実行される処理を記述します。この部分が繰り返し実行されます。

例として、1から10までの数値をコンソールに出力するforループのコードを示します:

```javascript
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

この例では、`let i = 1`で変数`i`を初期化し、`i <= 10`という条件式で繰り返しの条件を設定しています。ループのブロック内では`console.log(i)`が実行され、変数iの値がコンソールに出力されます。最後に`i++`によって`i`の値が1ずつ増加します。

以上が`forループ`の基本的な使い方です。繰り返し処理が必要な場合には`forループ`を活用しましょう。

### 具体的な使用例
forループは、同じ処理を複数回繰り返す場合に使用されます。以下に、forループの使用例と具体的なコードをいくつか示します。

1. 配列の要素を処理する場合:

```javascript
const numbers = [1, 2, 3, 4, 5];

for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}
```

この例では、配列`numbers`の要素を順番に処理して、それぞれの要素をコンソールに出力しています。`i`はループ変数で、`0`から始まり、`numbers`配列の長さ未満の値である限りループが続きます。ループの各反復で、配列の要素にアクセスするために`numbers[i]`を使用しています。

2. オブジェクトのプロパティを処理する場合:

```javascript
const person = {
  name: 'John',
  age: 30,
  gender: 'male'
};

for (let key in person) {
  console.log(key + ': ' + person[key]);
}
```

この例では、オブジェクト`person`のプロパティを順番に処理して、プロパティ名とその値をコンソールに出力しています。`key`はループ変数で、`person`オブジェクトの各プロパティ名が代入されます。ループのブロック内では、`person[key]`を使ってプロパティの値にアクセスしています。

3. 固定回数の繰り返し処理の場合:

```javascript
for (let i = 0; i < 5; i++) {
  console.log('Hello');
}
```

この例では、`5`回の繰り返し処理を行い、`Hello`という文字列をコンソールに出力しています。ループ変数`i`は`0`から始まり、`5`未満の値である限りループが続きます。

これらは一部の例ですが、`forループ`はデータの集合を反復処理したり、特定の回数の繰り返し処理を行う場合に頻繁に使用されます。制御の流れを明確に表現し、繰り返し処理を効率的に行うことができます。

***
## for...in
`for...inループ`は、オブジェクトのプロパティを反復処理するためのループです。`for...inループ`では、オブジェクトのキー（プロパティ名）を順番に取得して処理を行うことができます。

基本的な`for...inループ`の`構文は以下のようになります:

```javascript
for (let key in object) {
  // キーに対する処理
}
```

それぞれの部分について説明します:

1. key: オブジェクトのプロパティ名が代入される変数です。ループの各反復で異なるプロパティ名が代入されます。

2. object: 反復処理するオブジェクトです。

例として、以下のようなオブジェクトがあるとします:

```javascript
const person = {
  name: 'John',
  age: 30,
  gender: 'male'
};
```

この場合、`for...inループ`を使ってpersonオブジェクトのプロパティを反復処理するコードは以下のようになります:

```javascript
for (let key in person) {
  console.log(key + ': ' + person[key]);
}
```

このループでは、各反復で変数keyにオブジェクトpersonのプロパティ名が代入されます。ループのブロック内では、`person[key]`を使ってプロパティの値にアクセスし、コンソールに出力しています。

出力結果は以下のようになります:

```
name: John
age: 30
gender: male
```

注意点として、`for...inループ`はオブジェクトのプロパティを反復処理するために使用されることが一般的です。配列の反復処理には`forループ`や`Array.forEachメソッド`を使用するのが適しています。

``for...inループ``の使用時には、オブジェクトが継承したプロパティも反復されることに注意してください。また、反復の順序は一定ではないため、プロパティの順番に依存した処理には使わない方が良いでしょう。

### for...inループの具体例
`for...inループ`はオブジェクトのプロパティを反復処理するためのループです。以下に、`for...inループ`の具体的な例をいくつか示します。

1. オブジェクトのプロパティを表示する場合:

```javascript
const person = {
  name: 'John',
  age: 30,
  gender: 'male'
};

for (let key in person) {
  console.log(key + ': ' + person[key]);
}
```

この例では、オブジェクト`person`のプロパティを順番に処理して、プロパティ名とその値をコンソールに出力しています。`key`はループ変数で、`person`オブジェクトの各プロパティ名が代入されます。ループのブロック内では、`person[key]`を使ってプロパティの値にアクセスしています。

2. オブジェクトのプロパティを合計する場合:

```javascript
const sales = {
  product1: 100,
  product2: 200,
  product3: 150,
  product4: 300
};

let total = 0;

for (let key in sales) {
  total += sales[key];
}

console.log('Total sales: ' + total);
```

この例では、オブジェクト`sales`の各プロパティの値を合計しています。ループの各反復で、`sales[key]`を使ってプロパティの値にアクセスし、それを`total`変数に加算しています。

3. オブジェクトのプロパティに対して処理を行う場合:

```javascript
const person = {
  name: 'John',
  age: 30,
  gender: 'male'
};

for (let key in person) {
  if (typeof person[key] === 'string') {
    console.log('String property: ' + person[key]);
  }
}
```

この例では、オブジェクト`person`の各プロパティに対して処理を行っています。ループのブロック内では、`typeof`演算子を使ってプロパティの型をチェックし、文字列であればコンソールに出力しています。

これらは一部の例ですが、`for...inループ`は**オブジェクトのプロパティに対して反復処理を行う際**に便利です。ただし、**配列の反復処理**には`for...inループ`ではなく、`for...ofループ`が適しています。

もしこれ以外にも疑問や具体的な使い方について質問があれば、お知らせください。

***
## for...ofループ
`for...ofループ`は、**配列やイテラブルオブジェクトの要素を反復処理するためのループ**です。`for...ofループ`は、反復可能なオブジェクトの要素を直接取り出して利用するため、よりシンプルな記述が可能です。

以下に、`for...ofループ`の基本的な使い方と具体的な例を示します。

基本構文:
```javascript
for (let element of iterable) {
  // 要素に対する処理
}
```

- `element`: 反復処理中の各要素が代入される変数名です。
- `iterable`: 反復可能なオブジェクト（配列や文字列など）です。

具体例1: 配列の要素を表示する場合
```javascript
const numbers = [1, 2, 3, 4, 5];

for (let num of numbers) {
  console.log(num);
}
```
この例では、配列`numbers`の要素を順番に処理して、各要素をコンソールに表示しています。

具体例2: 文字列の文字を表示する場合
```javascript
const message = 'Hello';

for (let char of message) {
  console.log(char);
}
```
この例では、文字列`message`の各文字を順番に処理して、各文字をコンソールに表示しています。

`for...ofループ`は、配列や文字列などの反復可能なオブジェクトを簡潔に反復処理するための方法です。ループ内で取得した要素を直接利用する場合に便利です。

ただし、`for...ofループ`は反復可能なオブジェクトに対してのみ使用できます。オブジェクトのプロパティを反復処理する場合は、`for...inループ`を使用する必要があります。

### for...ofループの具体例
例1: 配列の要素を合計する

```javascript
const numbers = [1, 2, 3, 4, 5];
let sum = 0;

for (let num of numbers) {
  sum += num;
}

console.log(sum); // 出力: 15
```
この例では、配列`numbers`の要素を合計しています。`for...ofループ`を使用して配列の要素にアクセスし、それぞれの要素を`sum`に加算しています。

例2: 文字列の文字数をカウントする
```javascript
const message = 'Hello, world!';
let count = 0;

for (let char of message) {
  count++;
}

console.log(count); // 出力: 13
```
この例では、文字列`message`の文字数をカウントしています。`for...ofループ`を使用して文字列の各文字にアクセスし、カウントを増やしています。

例3: Mapの要素を処理する
```javascript
const map = new Map();
map.set('name', 'John');
map.set('age', 30);
map.set('city', 'Tokyo');

for (let [key, value] of map) {
  console.log(key, value);
}
```
この例では、Mapオブジェクトの要素を処理しています。`for...ofループ`を使用して、Mapの各エントリーをキーと値のペアとして取得しています。

これらの例は、`for...ofループ`の基本的な使用方法を示しています。配列や文字列、反復可能なオブジェクトを効果的に処理するために、`for...ofループ`を活用することができます。

***
***
##　配列３から
```javascript
index = myArray.pop();
myArray.push( "Mario" , "Luigi" ); //myArrayにpushする

for (let i = 0; i < myArray.length; i++){
myArray[i] = myArray[i] + '('+i+')';
}

myString = myArray.join('-');
  //Ryu(0)-Ken(1)-Chun-Li(2)-Cammy(3)-Guile(4)-Sakura(5)-Sagat(6)-Mario(7)-Luigi(8)
```