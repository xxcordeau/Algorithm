# algorithm

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
