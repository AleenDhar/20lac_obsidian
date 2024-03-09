using  http
```
const http = require("http")

const server = http.createServer((req,res)=>{
	res.send("hello")
})
server.listen(8000,()=> console.log)
```
using express as a handler and http
```
const express = require("express")
const http = require("http")

const app = express()
app.get("/",(req,res)=>{
	res.send("home")
})
const server = http.createServer(app)

server.listen(8000)

```