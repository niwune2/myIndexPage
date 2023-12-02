# .join()
```javascript
index = myArray.pop();
myArray.push( "Mario" , "Luigi" ); //myArrayにpushする

for (let i = 0; i < myArray.length; i++){
myArray[i] = myArray[i] + '('+i+')';
}

myString = myArray.join('-');
  //Ryu(0)-Ken(1)-Chun-Li(2)-Cammy(3)-Guile(4)-Sakura(5)-Sagat(6)-Mario(7)-Luigi(8)
```