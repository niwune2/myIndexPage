# .map()

### `.map()`メソッドを使ったもの
```javascript
let index0 = myArray.pop();
myArray.push('mario' , 'luigi');
let myString0 = myArray.map((Element,index) =>`${Element}(${index})`);
let myString = myString0.join('-');
    //Ryu(0)-Ken(1)-Chun-Li(2)-Cammy(3)-Guile(4)-Sakura(5)-Sagat(6)-mario(7)-luigi(8)
```

`map()` メソッドを使用する方法：

```javascript
const myArray = ['apple', 'banana', 'orange'];

const newArray = myArray.map((element, index) => `(${index}) ${element}`);

console.log(newArray);
```

このコードでは、`map()` メソッドを使って新しい配列 `newArray` を作成しています。コールバック関数内で、各要素とインデックス番号を組み合わせて新しい要素を生成しています。

### `.map()`について

`.map()`は、配列の各要素に対して**指定された関数を実行し、その結果を新しい配列として返す**JavaScriptのメソッドです。

以下は基本的な使用例です:

```javascript
const numbers = [1, 2, 3, 4, 5];

const doubledNumbers = numbers.map((num) => {
  return num * 2;
});

console.log(doubledNumbers); // [2, 4, 6, 8, 10]
```

`.map()`は**配列の要素を順番に取り出し**、指定された関数をそれぞれの要素に対して呼び出します。関数の返り値が新しい配列の対応する位置の要素となります。最終的に、新しい配列が生成されます。

`.map()`のコールバック関数は、要素の値だけでなく、インデックスや配列自体を引数として受け取ることもできます。以下はその例です:

```javascript
const numbers = [1, 2, 3, 4, 5];

const multipliedNumbers = numbers.map((num, index, array) => {
  return num * index * array.length;
});

console.log(multipliedNumbers); // [0, 2, 6, 12, 20]
```

`.map()`は元の配列を変更するのではなく、**新しい配列を返すため、元の配列は変更されません。**

`.map()`は配列の要素に対して繰り返し処理を行い、変換や加工を行いたい場合に便利です。例えば、配列内の全ての要素を大文字に変換する、要素の長さを取得するなど、多くのシナリオで利用されます。