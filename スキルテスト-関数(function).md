# スキルテスト-関数(function)
- [スキルテスト-関数(function)](#スキルテスト-関数function)
  - [DOM操作：便利だと思う](#dom操作便利だと思う)
  - [関数1](#関数1)
    - [メモ-1](#メモ-1)
    - [GPTアドバイス-1](#gptアドバイス-1)
      - [`return`の重要性](#returnの重要性)
    - [模範解答-1](#模範解答-1)
  - [関数2](#関数2)
    - [メモ–２](#メモ２)
      - [GPTアドバイス-2](#gptアドバイス-2)
    - [模範解答-2](#模範解答-2)
  - [関数3](#関数3)
    - [メモ-3](#メモ-3)
      - [GTPアドバイス-3](#gtpアドバイス-3)
    - [模範解答-3](#模範解答-3)
  - [関数4](#関数4)
      - [メモ-4](#メモ-4)
      - [GPTアドバイス-4](#gptアドバイス-4)
    - [模範解答-4](#模範解答-4)

[JavaScriptでランダムな配列を作成する](https://www.suzu6.net/posts/91-js-random-array/)

[アロー関数式](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/Arrow_functions#:~:text=%E3%81%AE%E3%82%A6%E3%82%A7%E3%83%96%E6%8A%80%E8%A1%93-,%E3%82%A2%E3%83%AD%E3%83%BC%E9%96%A2%E6%95%B0%E5%BC%8F,-Save)

## DOM操作：便利だと思う
以下の問題の中には、新しいHTML要素を作成し、そのテキスト内容を特定の文字列値と等しくなるように設定し、ページ上の既存の要素の中に入れ込むなど、DOM操作のコードを記述する必要があるものがありますが、すべてJavaScriptで行います。

このコースではまだ明確に教えていませんが、それを利用したいくつかの例を見たでしょうし、問題にうまく答えるために必要なDOM APIについて調べてほしいと思います。そのため、問題を解くために必要なDOM APIについて調べておくことをお勧めします。

[文章の操作](https://developer.mozilla.org/ja/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents#:~:text=%E9%96%8B%E7%99%BA%E3%82%92%E5%AD%A6%E3%81%B6-,%E6%96%87%E6%9B%B8%E3%81%AE%E6%93%8D%E4%BD%9C,-Save)

## 関数1
最初の課題では、
1. 与えられた配列（`names`）からランダムな名前を与えられた段落（`para`）に出力する簡単な関数 - `chooseName()` - を作成し、
2. それを一度実行する必要があります。

```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada']
const para = document.createElement('p');
// Add your code here

// Don't edit the code below here!
section.innerHTML = ' ';
section.appendChild(para);
```
### メモ-1
```js
function chooseName(){
    names[Math.floor(Math.random() * names.length)];
}
para.textContent = chooseName();
```

### GPTアドバイス-1
```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada']
const para = document.createElement('p');

function chooseName() {
  return names[Math.floor(Math.random() * names.length)];
}

para.textContent = chooseName();

section.innerHTML = '';
section.appendChild(para);
```
#### `return`の重要性
はい、`return`文は関数内で計算結果や処理結果を呼び出し元に返すための重要な要素です。関数が値を返さない場合、呼び出し元は関数からの戻り値を受け取ることができず、その結果を他の処理に活用することができません。

`return`文は、関数内で実行された結果や計算結果、あるいは特定の値を呼び出し元に返すために使用されます。関数が値を返す場合、`return`文を使用してその値を指定する必要があります。

したがって、関数が値を返す場合には、`return`文を使用して返り値を明示的に指定する必要があります。そうすることで、関数が期待どおりに動作し、呼び出し元でその結果を利用できるようになります。

### 模範解答-1
```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada']
const para = document.querySelector('p');

function chooseName() {
  const randomNumber = Math.floor(Math.random() * names.length);
  const choice = names[randomNumber];
  para.textContent = choice;
}

chooseName();
```


## 関数2
関数に関連する2つ目のタスクでは、与えられた5つの入力変数に基づいて、与えられた `<canvas>` (参照変数 `canvas`, `ctx` で利用できるコンテキスト) に矩形を描画する関数を作成する必要があります：

- `x` - 矩形の x 座標．
- `y` - 矩形の y 座標．
- `width` - 矩形の幅。
- `height` - 矩形の高。
- `color` - 矩形の色。

描画の前にキャンバスをクリアしておくと、ライブ版の場合、コードが更新されたときに、たくさんの矩形が重なって描かれることがありません。
```js
const canvas = document.querySelector('canvas');
const ctx = canvas.getContext('2d');

const x = 50;
const y = 60;
const width = 100;
const height = 75;
const color = 'blue';
// Add your code here
```
### メモ–２
```js
function draw(){
    return ctx.fillStyle = color;
    return ctx.fillRect(x,y,width,hight);
}
```
#### GPTアドバイス-2
コードの中で2つの問題があります。

1. `return`文の位置が誤っています。
2. `height`の変数名が誤っています。

正しいコードは以下のようになります：

```js
const canvas = document.querySelector('canvas');
const ctx = canvas.getContext('2d');

const x = 50;
const y = 60;
const width = 100;
const height = 75;
const color = 'blue';

function draw() {
    ctx.fillStyle = color;
    ctx.fillRect(x, y, width, height);
}

draw();
```

修正点：
1. 関数`draw`内の`return`文は不要です。描画処理を行うだけで返り値は必要ありません。
2. `height`の変数名が誤っていました。正しい変数名は`height`です。

修正後のコードでは、`draw`関数が`ctx.fillStyle`に指定された色で矩形を描画します。最後に`draw()`関数を呼び出して描画処理を実行します。
***
`return`が不要で、`height`のスペルミスと、最後に`draw()`が必要だったのですね
***
はい、正しく理解されています。

- `return`文は関数からの値の返却に使われますが、この場合は描画処理が目的なので返り値が必要ありません。そのため、`return`文は不要です。
- `height`のスペルミスは修正が必要です。正しい変数名は`height`です。
- 最後に`draw()`関数を呼び出すことで、実際に矩形が描画されます。

修正後のコードでは、関数`draw`内で矩形の描画設定を行い、`draw()`関数を呼び出すことで矩形が描画されます。

### 模範解答-2
```js
const canvas = document.querySelector('canvas');
const ctx = canvas.getContext('2d');

const x = 50;
const y = 60;
const width = 100;
const height = 75;
const color = 'blue';

function drawSquare(x, y, width, height, color) {
  ctx.fillStyle = 'white';
  ctx.fillRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = color;
  ctx.fillRect(x, y, width, height);
}

drawSquare(x, y, width, height, color);
```

## 関数3
この課題では、課題1で出された問題に戻り、それを改善することを目的としています。改善してほしいのは、次の3点です：

1. 乱数を生成するコードを `random()` という別の関数にリファクタリングし、乱数がその間にあるべき2つの一般的な境界をパラメータとして受け取り、その結果を返すようにする。
2. chooseName()`関数を更新し、乱数関数を利用し、選択する配列をパラメータとして受け取り（より柔軟に）、その結果を返すようにする。
3. 返された結果をパラグラフ (`para`) の `textContent` に出力する。
***
1. Refactor the code that generates the random number into a separate function called `random()`, which takes as parameters two generic bounds that the random number should be between, and returns the result.
2. Update the `chooseName()` function so that it makes use of the random number function, takes the array to choose from as a parameter (making it more flexible), and returns the result.
3. Print the returned result into the paragraph (`para`)'s `textContent`.
***
**GPT翻訳**

この課題では、次の手順に従ってコードをリファクタリング（改良）していくよう指示されています。以下、各手順の解説です。

1. ランダムな数値を生成するコードを、`random()`という別の関数にリファクタリングします。この関数は、ランダムな数値が存在する範囲の下限と上限をパラメータとして受け取り、その範囲内のランダムな数値を生成して結果を返します。
2. `chooseName()`関数を更新し、ランダムな数値の関数を利用するようにします。また、選択する配列をパラメータとして受け取るように変更します（柔軟性が向上します）。そして、結果を返すようにします。
3. 返された結果を段落（`para`）の`textContent`に表示します。

この課題では、コードの機能をより分割し、再利用可能な関数を作成することが求められています。それにより、コードの柔軟性と保守性が向上します。
***

```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada']
const para = document.createElement('p');
// Add your code here
// Don't edit the code below here!
section.innerHTML = ' ';
section.appendChild(para);
```
### メモ-3
```js
function random(){
    let max = names.length;
    return Math.floor(Math.random() * Math.floor(max));
    // 0からmax-1までの整数を返す
}
function chooseName() {
    return names[random()];
}
para.textContent = chooseName();

```
#### GTPアドバイス-3
提供されたコードは、指示に従って正しくリファクタリングされています。各手順が適切に実装されているため、機能が期待通りに動作するはずです。

1. `random()`関数では、与えられた範囲（`names`配列の長さ）内でランダムな整数を生成するための処理が行われています。
2. `chooseName()`関数では、`random()`関数を使用してランダムに要素を選択しています。`names`配列の要素の中からランダムに名前を選ぶことができます。
3. 最後に、選択された名前が段落（`para`）の`textContent`に表示されています。

これにより、指定されたタスクが適切に実行されています。

### 模範解答-3
```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada']
const para = document.querySelector('p');

function random(min, max) {
  const num = Math.floor(Math.random() * (max - min)) + min;
  return num;
}

function chooseItem(array) {
  const choice = array[random(0, array.length)];
  return choice;
}

para.textContent = chooseItem(names);
```

## 関数4
このタスクでは、名前の配列があり、5文字より短い名前だけを集めた配列を得るために `Array.filter()` を使っています。このフィルターには現在、名前の長さをチェックする関数 `isShort()` が渡されており、名前が5文字未満であれば `true`、そうでなければ `false` を返しています。

これをアロー関数に変えてください。どれだけコンパクトにできるか試してみてください。
>We'd like you to change this into an arrow function. See how compact you can make it.
```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada'];
const para = document.createElement('p');
function isShort(name) {
  return name.length < 5;
}
const shortNames = names.filter(isShort);
para.textContent = shortNames;

// Don't edit the code below here!
section.innerHTML = ' ';
section.appendChild(para);
```
#### メモ-4
```js
let isShort = (name) => {name.length < 5};
```
#### GPTアドバイス-4
アロー関数の記述において、返り値を明示的に返す必要があります。現在のコードでは、アロー関数内の処理は正しく実行されているものの、実際の返り値が指定されていません。修正するには、以下のようにアロー関数の本体を `{}` で囲んで明示的に返り値を指定します。

```js
let isShort = (name) => {
  return name.length < 5;
};
```

または、単一の式である場合は中括弧 `{}` を省略し、直接式を返すこともできます。

```js
let isShort = (name) => name.length < 5;
```

どちらの書き方でも、返り値が正しく指定されるため、期待する結果を得ることができます。修正後に再度試してみてください。
### 模範解答-4
```js
const names = ['Chris', 'Li Kang', 'Anne', 'Francesca', 'Mustafa', 'Tina', 'Bert', 'Jada']
const para = document.createElement('p');

const shortNames = names.filter(name => name.length < 5);
para.textContent = shortNames;
```