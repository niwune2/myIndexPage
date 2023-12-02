# .forEach()

### `.forEach()`メソッドを使ったもの
```javascript
let index0 = myArray.pop();
myArray.push('mario' , 'luigi');
let myString0 = [];
myArray.forEach((element,index) =>{
    myString0.push(`${element}(${index})`);
});
let myString = myString0.join('-');
    //Ryu(0)-Ken(1)-Chun-Li(2)-Cammy(3)-Guile(4)-Sakura(5)-Sagat(6)-mario(7)-luigi(8)
```

### `forEach()` メソッドを使用する方法：

```javascript
const myArray = ['apple', 'banana', 'orange'];
const newArray = [];

myArray.forEach((element, index) => {
  newArray.push(`(${index}) ${element}`);
});

console.log(newArray);
```

このコードでは、`forEach()` メソッドを使って配列をイテレートし、各要素とインデックス番号を組み合わせた新しい要素を `newArray` に追加しています。

どちらの方法も、**配列の各要素に対して処理を行い、新しい配列を生成する**ことができます。使いやすい方法を選んでください。

### `.forEach()`について
`.forEach()`は、**配列の各要素に対して指定された関数を実行する**JavaScriptのメソッドです。

以下は基本的な使用例です:

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((num) => {
  console.log(num);
});
```

この場合、`.forEach()`は配列の各要素に対してコールバック関数を呼び出し、それぞれの要素を引数として渡します。上記の例では、各要素がコンソールに表示されます。

`.forEach()`は、**配列を変更せずに要素を順番に処理するため、新しい配列を返しません。**

`.forEach()`のコールバック関数は、要素の値だけでなく、インデックスや配列自体も引数として受け取ることができます。以下はその例です:

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((num, index, array) => {
  console.log(`Index: ${index}, Value: ${num}`);
  console.log(`Original Array: ${array}`);
});
```

`.forEach()`は、`.map()`とは異なり、**新しい配列を生成せず**、主にループ処理や要素に対する副作用を実行するために使用されます。要素ごとに特定の処理を行いたい場合や、配列内の要素を直接変更したい場合に適しています。