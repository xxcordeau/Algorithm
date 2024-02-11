#Algorithm
===================================================
<h1> 2023.10.08 </h1>hu
<h3> 문제 20 | 특정한 문자를 대문자로 바꾸기 </h3>
<h5> 정수 num과 n이 매개 변수로 주어질 때, num이 n의 배수이면 1을 return n의 배수가 아니라면 0을 return하도록 solution 함수를 완성해주세요.<br>
  | num은 2의 배수이므로 1을 return && num은 3의 배수가 아니므로 0을 return </h5>

```javascript

function solution(num, n) {
    var answer = 0;
    if(num%n==1){
        answer = 0;
    }else{
        answer = 1;
    }
    return answer;
}

```
<br>

<h1> 2023.10.07 </h1>
<h3> 문제 19 | 특정한 문자를 대문자로 바꾸기 </h3>
<h5> 영소문자로 이루어진 문자열 my_string과 영소문자 1글자로 이루어진 문자열 alp가 매개변수로 주어질 때, my_string에서 alp에 해당하는 모든 글자를 대문자로 바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.

 | alp = n >> jeoNgyeoN </h5>

```javascript

function solution(my_string, alp) {
    var answer =[];
    let arr =  [...my_string];
    
    for( let i=0; i< arr.length; i++){
        if(arr[i] == alp){ //p === p
            alp = alp.toUpperCase() //p = P
            arr[i] = alp; 
        }   
        alp = alp.toLowerCase() //P = p
    }
    answer = arr.join("");
 
    return answer;
    
}
```
<br>

<h1> 2023.10.06 </h1>
<h3> 문제 18 | 대문자로 바꾸기 </h3>
<h5> 알파벳으로 이루어진 문자열 myString이 주어집니다. 모든 알파벳을 대문자로 변환하여 return 하는 solution 함수를 완성해 주세요. | jEonG >> JEONG </h5>

```javascript

function solution(myString) {
    var answer = '';
    
    answer = myString.toUpperCase();
    
    return answer;
}

```
<br>

<h1> 2023.10.05 </h1>
<h3> 문제 17 | 글자 이어 붙여 문자열만들기 </h3>
<h5> 문자열 my_string과 정수 배열 index_list가 매개변수로 주어집니다. my_string의 index_list의 원소들에 해당하는 인덱스의 글자들을 순서대로 이어 붙인 문자열을 return 하는 solution 함수를 작성해 주세요.<br> 
 | "cvsgiorszzzmrpaqpe" >>> [16, 6, 5, 3, 12, 14, 11, 11, 17, 12, 7]>>> "programmers" </h5>

```javascript

function solution(my_string, index_list) {
    var answer = [];
    
    for( let i = 0; i<index_list.length; i++){
        
     answer += my_string[index_list[i]];
        
    }
    
    return answer;
}

```
<br>



<h1> 2023.10.04 </h1>
<h3> 문제 16 | 문자열로 변환 </h3>
<h5> 문자열 my_string과 정수 n이 매개변수로 주어질 때, my_string의 뒤의 n글자로 이루어진 문자열을 return 하는 solution 함수를 작성해 주세요.  <br>  | "ProgrammerS123" >> n >> "grammerS123" </h5>

```javascript

function solution(my_string, n) {
    var answer = '';
    
    answer = my_string.substr(-n)
    
    return answer;
}

```
<br>

-  substr( start , length ) 
-  시작점부터 길이만큼 잘림 , start만 적을 경우 시작점부터 전부 잘림



<h1> 2023.10.03 </h1>
<h3> 문제 15 | 문자열로 변환 </h3>
<h5> 정수 n이 주어질 때, n을 문자열로 변환하여 return하도록 solution 함수를 완성해주세요. | 123 >> "123" </h5>

```javascript

function solution(n) {
    var answer = '';
    
    const arr = [n];
    answer = arr.join('');
    
    return answer;
}

```
<br>

-  배열을 join()으로 묶을 수 있다.
-  join('') 으로 String으로 묶을 수 있다.


<h1> 2023.10.02 </h1>
<h3> 문제 14 | 두 수의 연산값 비교하기 </h3>
<h5> 연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.<br>

- 12 ⊕ 3 = 123<br>
- 3 ⊕ 12 = 312<br>
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 2 * a * b 중 더 큰 값을 return하는 solution 함수를 완성해 주세요.<br>

단, a ⊕ b와 2 * a * b가 같으면 a ⊕ b를 return 합니다.<br> | a == 9 / b == 18 >>> 918 </h5>

```javascript

function solution(a, b) {
    var answer = 0;
    
    let num1 = Number(`${a}${b}`);
    let num2 = 2*a*b;
    
    if (num1 < num2 ){
        answer = num2;
    } else {
        answer = num1;
    }
    
    
    
    return answer;
}
```
<br>


<h1> 2023.10.01 </h1>
<h3> 문제 13 | 더 크게 합치기 </h3>
<h5> 연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.<br>

- 12 ⊕ 3 = 123<br>
- 3 ⊕ 12 = 312<br>
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 b ⊕ a 중 더 큰 값을 return 하는 solution 함수를 완성해 주세요.<br>

단, a ⊕ b와 b ⊕ a가 같다면 a ⊕ b를 return 합니다.<br> | a == 9 / b == 18 >>> 918 </h5>

```javascript
function solution(a, b) {
    var answer = 0;
    let num1 = Number(`${a}${b}`);
    let num2 = Number(`${b}${a}`);
    
    
    if ( num1 < num2){
       answer = num2;
    } else{
        answer = num1
    }
    
    return answer;
}
```
<br>


<h1> 2023.09.31 </h1>
<h3> 문제 12 | 문자열 곱하기 </h3>
<h5> 문자열 my_string과 정수 k가 주어질 때, my_string을 k번 반복한 문자열을 return 하는 solution 함수를 작성해 주세요.<br> | "string" / k >>> "stringstringstring" </h5>

```javascript
function solution(my_string, k) {
    var answer = '';
    
    for (let i=0; i<k; i++){
        answer += my_string
    }
    return answer;
}
```
<br>


<h1> 2023.09.30 </h1>
<h3> 문제 11 | 문자리스트를 문자열로 반환하기 </h3>
<h5> 문자들이 담겨있는 배열 arr가 주어집니다. arr의 원소들을 순서대로 이어 붙인 문자열을 return 하는 solution함수를 작성해 주세요. <br>| ["a","b","c"] >>> "abc" </h5>

```javascript
function solution(arr) {
    var answer = '';
    
    
    for(let i = 0; i<arr.length; i++){
        answer += arr[i]
    }
    
    
    return answer;
}
```
<br>


<h1> 2023.09.29 </h1>
<h3> 문제 10 | 문자열 섞기 </h3>
<h5> 길이가 같은 두 문자열 str1과 str2가 주어집니다.
두 문자열의 각 문자가 앞에서부터 서로 번갈아가면서 한 번씩 등장하는 문자열을 만들어 return 하는 solution 함수를 완성해 주세요. | aaaaa bbbbb >>> ababababab </h5>

```javascript
function solution(str1, str2) {
    var answer = '';
    str1 = [...str1];
    str2 = [...str2];
   
    for(let i =0; i<str1.length; i++ ){
       
        answer += str1[i]
        answer += str2[i]
        
    }
    
    return answer;
}
```
<br>


<h1> 2023.09.28 </h1>
<h3> 문제 9 | 문자열 겹쳐쓰기 </h3>
<h5> 문자열 my_string, overwrite_string과 정수 s가 주어집니다. 문자열 my_string의 인덱스 s부터 overwrite_string의 길이만큼을 문자열 overwrite_string으로 바꾼 문자열을 return 하는 solution 함수를 작성해 주세요.</h5>

```javascript
function solution(my_string, overwrite_string, s) {
    const myStr = [...my_string];
    myStr.splice(s,overwrite_string.length,overwrite_string);
    return myStr.join("");
}
```
<br>
- 오래 고민했던 문제.. 다시보자


<h1> 2023.09.27 </h1>
<h3> 문제 8 | 홀짝구분하기 </h3>
<h5> 자연수 n이 입력으로 주어졌을 때 만약 n이 짝수이면 "n is even"을, 홀수이면 "n is odd"를 출력하는 코드를 작성해 보세요.</h5>

```javascript
onst readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
    
}).on('close', function () {
    n = Number(input[0]);
    
    if(n%2 == 0){
        console.log(`${n} is even`);
    } else if ( n%2 == 1 ) {
        console.log(`${n} is odd`)
    }
    
});
```
<br>



<h1> 2023.09.26 </h1>
<h3> 문제 7 | 문자열 돌리기 </h3>
<h5> 문자열 str이 주어집니다.
문자열을 시계방향으로 90도 돌려서 아래 입출력 예와 같이 출력하는 코드를 작성해 보세요. | abcde >> a (enter) b (enter)...</h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line;
    
}).on('close',function(){
    
    for(i=0; i<input.length; i++){
        console.log(input[i])
    }
    
 
});
```
<br>


<h1> 2023.09.25 </h1>
<h3> 문제 6 | 문자열 붙여서 출력하기 </h3>
<h5> 두 개의 문자열 str1, str2가 공백으로 구분되어 입력으로 주어집니다.
입출력 예와 같이 str1과 str2을 이어서 출력하는 코드를 작성해 보세요. | apple pen >>> applepen </h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    str1 = input[0];
    str2 = input[1];
    console.log(str1+str2)
});
```
<br>

<h1> 2023.09.24 </h1>
<h3> 문제 6 | 덧셈식 출력하기 </h3>
<h5> 두 정수 a, b가 주어질 때 다음과 같은 형태의 계산식을 출력하는 코드를 작성해 보세요. | a + b = c </h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    console.log(`${input[0]} + ${input[1]}`+' = '+ (Number(input[0]) + Number(input[1])));
});
```
<br>



<h1> 2023.09.23 </h1>
<h3> 문제 5 | 특수문자 출력하기 </h3>
<h5> 다음과 같이 출력하도록 코드를 작성해 주세요. | !@#$%^&*(\'"<>?:; </h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let str = '!@#$%^&*(\'"<>?:;'
rl.on('close', function () {
    console.log('!@#$%^&*(\\\'\"<>?:;');
});
```
<br>

<h1> 2023.09.22 </h1>
<h3> 문제 4 | 대소문자 바꿔서 출력하기 </h3>
<h5> 영어 알파벳으로 이루어진 문자열 str이 주어집니다. 각 알파벳을 대문자는 소문자로 소문자는 대문자로 변환해서 출력하는 코드를 작성해 보세요.</h5>

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
- 문자열을 대문자로 바꿔주는 메서드 > toUpperCase();
- 문자열을 소문자로 바꿔주는 메서드 > toLowerCase();
<br>


<h1> 2023.09.21 </h1>
<h3> 문제 3 | 문자열 반복해서 출력하기 </h3>
<h5> 문자열 str과 정수 n이 주어집니다. str이 n번 반복된 문자열을 만들어 출력하는 코드를 작성해 보세요.</h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');

}).on('close', function () {
    str = input[0];
    n = Number(input[1]);
    answer = '';
    for(let i=0; i<n; i++){
        answer += str
        
    }
    console.log(answer);
});
```


<br>


<h1> 2023.09.21 </h1>
<h3> 문제 2 | a와 b 출력하기 </h3>
<h5>정수 a와 b가 주어집니다. 각 수를 입력받아 입출력 예와 같은 형식으로 출력하는 코드를 작성해 보세요.</h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];


rl.on('line', function (line) {
    input = line.split(' ');

}).on('close', function () {
    console.log('a = '+Number(input[0]));
    console.log('b = '+Number(input[1]));
});
```
- 문자열을 배열로 바꿔주는 메서드/ 괄호안에있는걸 기준으로 쪼갬 > .split(' ');
<br>










<h1> 2023.09.18 </h1>
<h3> 문제 1 | 문자열 출력하기 </h3>
<h5> 문자열 str이 주어질 때, str을 출력하는 코드를 작성해 보세요. </h5>

```javascript
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

let str = '';

rl.on('line', function (line) {
    input = [line];
}).on('close',function(){
    str = input[0];
    console.log(input[0])
});
```


