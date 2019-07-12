## 要求 
    
- 实现一个基础的计时器应用，点击开始按钮开始计时，点击结束按钮结束计时，并把计时的结果显示在上面的输入框中。

```html
<!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>定时器示例</title>
  </head>
  <body>
  
  <input type="text" id="result">
  
  <input type="button" value="开始" >
  <input type="button" value="结束" >
  <script>
  var oTxt=document.getElementsByTagName("input")[0];
  var oStart=document.getElementsByTagName("input")[1];
  var oStop=document.getElementsByTagName("input")[2];
  var oReset=document.getElementsByTagName("input")[3];
  var n= 0, timer=null;
  //开始计时
  oStart.onclick= function () {
    clearInterval(timer);
    timer=setInterval(function () {
      n++;
      var m=parseInt(n/60);
      var s=parseInt(n%60);
      oTxt.value=toDub(m)+":"+toDub(s);
    },1000/60);
  };
  //暂停并且清空计时器
  oStop.onclick= function () {
    clearInterval(timer);
  }
  //重置
  oReset.onclick= function () {
    oTxt.value="00:00";
    n=0;
  }
  //补零
  function toDub(n){
    return n<10?"0"+n:""+n;
  }
</script>
</body>
 </html>
```
