# if...else

if...else文は、条件に基づいてプログラムの一部を実行するための制御構造です。条件が真（true）の場合はifブロック内のコードが実行され、条件が偽（false）の場合はelseブロック内のコードが実行されます。

if...else文の基本的な構文は以下の通りです:

```javascript
if (条件) {
  // 条件が真の場合に実行するコード
} else {
  // 条件が偽の場合に実行するコード
}
```

具体的な例を見てみましょう:

```javascript
let age = 18;

if (age >= 20) {
  console.log("成人です");
} else {
  console.log("未成年です");
}
```

この例では、`age`変数の値が20以上の場合は「成人です」とコンソールに表示されますが、それ以外の場合は「未成年です」と表示されます。

また、複数の条件をチェックする場合には、if...else文をネスト（入れ子）にすることもできます。これはif文の中に別のif...else文を記述する形になります。

```javascript
let score = 80;

if (score >= 90) {
  console.log("優秀です");
} else if (score >= 70) {
  console.log("合格です");
} else {
  console.log("不合格です");
}
```

この例では、`score`変数の値に応じて異なるメッセージが表示されます。`score`が90以上の場合は「優秀です」、70以上の場合は「合格です」、それ以下の場合は「不合格です」と表示されます。

if...else文は条件に基づいてプログラムのフローを制御するための重要なツールです。条件を正しく設定し、適切なコードを実行することで、プログラムの挙動を制御することができます。

## if...elseの具体例
以下にいくつかの具体例を示します。

例1: 奇数か偶数かの判定
```javascript
let number = 10;

if (number % 2 === 0) {
  console.log("偶数です");
} else {
  console.log("奇数です");
}
```
この例では、`number`変数が偶数か奇数かを判定しています。`number`を2で割った余りが0の場合は偶数と判定され、それ以外の場合は奇数と判定されます。

例2: 条件の組み合わせ
```javascript
let temperature = 25;
let weather = "晴れ";

if (temperature >= 30 && weather === "晴れ") {
  console.log("プールに行きましょう");
} else if (temperature >= 25 && weather === "晴れ") {
  console.log("ピクニックに行きましょう");
} else {
  console.log("家で過ごしましょう");
}
```
この例では、`temperature`変数が30以上でかつ`weather`変数が"晴れ"の場合は「プールに行きましょう」と表示されます。`temperature`が25以上でかつ`weather`が"晴れ"の場合は「ピクニックに行きましょう」と表示されます。それ以外の場合は「家で過ごしましょう」と表示されます。

例3: 複数の条件をチェック
```javascript
let username = "";
let password = "";

if (!username) {
  console.log("ユーザー名を入力してください");
} else if (!password) {
  console.log("パスワードを入力してください");
} else {
  console.log("ログインに成功しました");
}
```
この例では、`username`と`password`が空の場合にそれぞれのエラーメッセージを表示します。どちらかの入力が空でない場合は「ログインに成功しました」と表示されます。

これらの具体例を通じて、if...else文がどのように条件に基づいたプログラムの実行フローを制御するための重要なツールであるかを理解できると思います。