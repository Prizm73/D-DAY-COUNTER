# D-DAY-COUNTER

#### This web source is a D-DAY source that tells you how many days left before the College Scholastic Ability Test. If you set only the year, month, and day in the source, it tells you how many days left from the set date.
#### 이 웹소스는 대학수학능력시험일로부터 며칠이 남았는지 알려주는 디데이 소스입니다. 소스에서 년도와 월, 일만 설정하면 설정한 일로부터 며칠이 남았는지 결과가 나옵니다.

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
