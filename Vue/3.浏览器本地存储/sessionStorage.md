## sessionStorage.html

```
<!DOCTYPE html> 
<html>
    <head>
    	<meta charset="UTF-8" />
    	<title>sessionStorage</title> 
    </head>
    <body>
    	<button onclick="saveData()">点我保存一个数据</button>
    	<button onclick="redData()">点我读取一个数据</button>
    	<button onclick="deleteData()">点我删除一个数据</button>
    	<button onclick="deleteAllData()">点我清空数据</button>
    	
    	<script type="text/javascript">
    		let p = {name:'张山',age:18}
    		
    		function saveData(){
    			sessionStorage.setItem('msg','hello')
    			sessionStorage.setItem('msg2','666')
    			sessionStorage.setItem('person',JSON.stringfy(p))
    		}
    		function redData(){
    			sessionStorage.getItem('msg')
    			sessionStorage.getItem('msg2')
    			
    			const result = sessionStorage.getItem('person') 
				console.log(JSON.parse(result))
    		}
    		function deleteData(){
    			sessionStorage.removeItem('msg2')
    		}
    		function deleteAllData(){
    			sessionStorage.clear()
    		}
    		
    	</script>
    </body>
</html>
```

