# D-DAY-COUNTER

Description
-----------
#### This web source is a D-DAY source that tells you how many days left before the College Scholastic Ability Test. If you set only the year, month, and day in the source, it tells you how many days left from the set date.
#### 이 웹소스는 대학수학능력시험일로부터 며칠이 남았는지 알려주는 디데이 소스입니다. 소스에서 년도와 월, 일만 설정하면 설정한 일로부터 며칠이 남았는지 결과가 나옵니다.

How to modify?
--------------
css/counter.css
```CSS
.box {
  position:absolute;
  top:50%; left:50%;
  transform: translate(-50%, -50%);
  -webkit-box-shadow: 0px 0px 20px -8px rgba(199,199,199,1);
  -moz-box-shadow: 0px 0px 20px -8px rgba(199,199,199,1);
  box-shadow: 0px 0px 20px -8px rgba(199,199,199,1);
  vertical-align: middle;
  border-radius: 150px; // You can mediate border-radius.
  padding: 175px;
  width: 55%;
  background: #A770EF;
  background: -webkit-linear-gradient(to left, #FDB99C, #CF8BF2, #A770EF);
  background: linear-gradient(to left, #FDB99C, #CF8BF2, #A770EF);
}
```

js/counter.js
```Javascript
var day = new Date('2019, 11, 14'); // ('2019, 11, 14') means 2019/11/14.
var present = new Date();
var alpha = present.getTime() - day.getTime();
var dday = Math.floor(alpha / (1000 * 60 * 60 * 24)) * -1;
if (dday==0) {
  document.getElementById("inday").innerHTML="D-Day";
}
else {
  document.getElementById("inday").innerHTML="D - "+dday;
}
```

Screenshot
-----------
![screenshot](https://user-images.githubusercontent.com/42485713/61586787-08696300-abb7-11e9-9882-7c7cf2c9da03.JPG)
