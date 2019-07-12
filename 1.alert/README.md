## 要求 
    
- 补充以下HTML，实现点击某一个数字可以alert出该数字。

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>事件监听</title>
  </head>
  <body>
  
  <ul id="no">
      <li>1</li>
      <li>2</li>
      <li>3</li>
      <li>4</li>
      <li>5</li>
      <li>6</li>
      <li>7</li>
  </ul>
  
  <script>
    var ul =  document.getElementById("no");
	var list = ul.querySelectorAll('li');
	for (var i = 0; i < list.length; i++) {
        list[i].index = i+1;
	}
	ul.addEventListener('click',function(e){
        alert(e.target.index);
})
  </script>
  </body>
  </html>
```
