using  http
```
const http = require("http")

const server = http.createServer((req,res)=>{
	res.send("hello")
})
server.listen(8000,()=> console.log)
```