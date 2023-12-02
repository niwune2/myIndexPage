# .startsWith()

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
スペルミスに注意。`start*s*With()`