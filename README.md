# Email_Address

```javascript
var userEmail = prompt("당신의 이메일 주소를 적어주세요.","");
var arrUrl = [".co.kr",".com",".net",".or.kr",".go.kr"];
```

이메일에 들어갈 주소와 URL를 입력하고 입력된 값을 저장하는 코드입니다.

<br><br>

```javascript
var check1 = false;
var check2 = false;
```

check1과 check2를 false값으로 지정하여 비활성화 시킨다.

<br><br>

```javascript
if( userEmail.indexOf("@") > 0) { check1 = true;}
```

indexOf는 입력한 이메일 주소에서 @ 가 있는 자릿수를 저장한다.    
그래서 입력된 값에 @ 가 있으면 indexOf는 0보다 큰 수가 오기 때문에   
check1에 true값이 오면서 활성화 된다.

<br><br>

```javascript
for(var i=0; i<arrUrl.length; i++) {
  if(userEmail.indexOf(arrUrl[i])>0){ 
    check2 = true;
  }
}
```

입력한 이메일 URL에서 arrUrl에 있는 배열과 중복되는 값이 있으면
check2에 true값이 오면서 활성화 된다.

<br><br>

```javascript
if( check1 && check2 ) {
  document.write(userEmail);
} else {
  alert("이메일 형식이 잘못되었습니다.");
}
```

check1 값과 check2 값이 둘다 활성화 상태이면 입력받은 이메일 주소를 출력한다.    
만약 둘중 한개라도 비활성화 상태이면 alert를 출력시킨다.

<br><br>
