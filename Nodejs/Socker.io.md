```javaScript
const {Server} = require("socketio")
const http = require("http")
const express = require("express")
const app = express()

cosnt server = http.createServer()


const io = new Server(server,()=>{
	cors:{
		origin:"http://localhost:3000"
	}
})

io.on("connection",(socket)=>{
	console.log(socket.id)

	socket.on("disconnect",()=>{
		console.log("user disconnected",socket.id)
	})
})

server.listen(8000,()=>console.log(`server started on port: 8000`))
```