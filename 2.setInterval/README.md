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
  
  <script type="text/javascript">
		
		function settime(a){
			if(a<10)
				a = "0"+a;
			return a;
		}
			 h = 0;
			 m = 0;
			 s = 0;
 
		function starttime(){
        	var showh = settime(h);
        	var showm = settime(m);
        	var shows = settime(s);
        	document.getElementById("showtime").innerHTML=showh+":"+showm+":"+shows;
 
       		s++;
        	if(s == 60)
       		{
        		s = 0;
        		m++;
       		 }
        	if(m == 60){
        		m = 0;
        		h++;
        	}
 
        	t = setTimeout("starttime()",1000);
		}
 
		function endtime() {
			clearTimeout(t);
		}
  </script>
  </body>
  </html>
```
