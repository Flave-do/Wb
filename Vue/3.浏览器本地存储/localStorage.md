## localStorage.html

```
<!DOCTYPE html> 
<html>
    <head>
    	<meta charset="UTF-8" />
    	<title>localStorage</title> 
    </head>
    <body>
    	<button onclick="saveData()">点我保存一个数据</button>
    	<button onclick="redData()">点我读取一个数据</button>
    	<button onclick="deleteData()">点我删除一个数据</button>
    	<button onclick="deleteAllData()">点我清空数据</button>
    	
    	<script type="text/javascript">
    		let p = {name:'张山',age:18}
    		
    		function saveData(){
    			localStorage.setItem('msg','hello')
    			localStorage.setItem('msg2','666')
    			localStorage.setItem('person',JSON.stringfy(p))
    		}
    		function redData(){
    			localStorage.getItem('msg')
    			localStorage.getItem('msg2')
    			
    			const result = localStorage.getItem('person') 
				console.log(JSON.parse(result))
    		}
    		function deleteData(){
    			localStorage.removeItem('msg2')
    		}
    		function deleteAllData(){
    			localStorage.clear()
    		}
    		
    	</script>
    </body>
</html>
```

