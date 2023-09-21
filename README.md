#algorithm
===================================================

<h1> 2023.09.21 </h1>
<h3> 문제 4 </h3>
<h5> 영어 알파벳으로 이루어진 문자열 str이 주어집니다. 각 알파벳을 대문자는 소문자로 소문자는 대문자로 변환해서 출력하는 코드를 작성해 보세요.</h5>
- input값 aBcDeFg
- output값 AbCdEfG

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = [line];
   
}).on('close',function(){
    str = input[0];
    
    let answer = '';
    for(let i=0; i<str.length; i++){
        if(str[i].toUpperCase() === str[i]) {
            str[i].toLowerCase();
            answer += str[i].toLowerCase();
        } else {
            str[i].toUpperCase();
            answer += str[i].toUpperCase();
        }
    }
    console.log( answer );
    
});
```
문자열을 대문자로 바꿔주는 메서드 > toUpperCase();
문자열을 소문자로 바꿔주는 메서드 > toLowerCase();
