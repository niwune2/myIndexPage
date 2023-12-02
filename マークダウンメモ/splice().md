# .splice()

`.splice()`メソッドは、配列に対して要素の追加や削除、置換を行うためのメソッドです。以下に基本的な情報を説明します。

`.splice()`メソッドの構文は以下の通りです。

```javascript
array.splice(start, deleteCount, item1, item2, ...)
```

- `start`: 変更を開始するインデックスを指定します。正の整数の場合は配列の先頭からの位置を示し、負の整数の場合は末尾からの位置を示します。
- `deleteCount`: 削除する要素の数を指定します。省略すると`start`以降のすべての要素が削除されます。
- `item1, item2, ...`: 追加する要素を指定します。`start`の位置に追加されます。

`.splice()`メソッドは以下のような動作をします。

- 指定した位置から要素を削除します。削除した要素は配列として返されます。
- 削除した要素の数だけ元の配列が変更されます。
- 必要に応じて指定した位置に新しい要素を追加します。

以下に具体例を示します。

例1: 要素の削除
```javascript
let numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 2); // インデックス2から2つの要素を削除

console.log(numbers); // [1, 2, 5]
```

例2: 要素の置換
```javascript
let colors = ["red", "green", "blue"];
colors.splice(1, 1, "yellow"); // インデックス1の要素を"yellow"に置換

console.log(colors); // ["red", "yellow", "blue"]
```

例3: 要素の追加
```javascript
let fruits = ["apple", "banana", "orange"];
fruits.splice(2, 0, "grape", "kiwi"); // インデックス2の位置に"grape"と"kiwi"を追加

console.log(fruits); // ["apple", "banana", "grape", "kiwi", "orange"]
```

このように、`.splice()`メソッドは柔軟な要素の変更を実現するための重要なメソッドです。

もちろんです。以下にさらなる`.splice()`メソッドの使用例を示します。

例4: 要素の削除と追加
```javascript
let numbers = [1, 2, 3, 4, 5];
numbers.splice(1, 3, 6, 7, 8); // インデックス1から3つの要素を削除し、その位置に6, 7, 8を追加

console.log(numbers); // [1, 6, 7, 8, 5]
```

例5: 削除した要素を別の変数に代入
```javascript
let numbers = [1, 2, 3, 4, 5];
let deleted = numbers.splice(2, 2); // インデックス2から2つの要素を削除し、削除した要素を変数deletedに代入

console.log(numbers); // [1, 2, 5]
console.log(deleted); // [3, 4]
```

例6: 要素の削除と追加を組み合わせ
```javascript
let colors = ["red", "green", "blue"];
colors.splice(1, 2, "yellow", "orange"); // インデックス1から2つの要素を削除し、その位置に"yellow"と"orange"を追加

console.log(colors); // ["red", "yellow", "orange"]
```

例7: 要素の全削除
```javascript
let numbers = [1, 2, 3, 4, 5];
numbers.splice(0); // 配列のすべての要素を削除

console.log(numbers); // []
```

これらの例から、`.splice()`メソッドが要素の削除や追加、置換を柔軟に行うことができることがわかります。また、削除した要素を取得したり、削除せずに要素を追加することもできます。

***
***
```javascript
// Add your code here

let index = birds.indexOf('Eagles');
if (index !== -1){  
      ///`index`が`!==(厳密に不等)`、もしつまりbirdsの配列に'Eagles'があれば下のコードを実行する。-1は不在を表す(?)
    birds.splice(index,1); ///`index`で特定したインデックス位置とそれ以降で削除する数

}
let eBirds = birds.filter(item => item.startsWith('E'));
    ///birdsの要素一つ一つをstartsWithでfilterし、条件に当てはまるものを新しい配列に含める。
    //Emus,Egrets

// Don't edit the code below here!
```