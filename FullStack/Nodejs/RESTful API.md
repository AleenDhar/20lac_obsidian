# what is the REST API

# Dynamic Route Params

```javascript
app.route("/api/user/:id")
.get((req,res)=>{
	const id = Number(req.parmas.id)
	cosnt user = user.find((user)=> user.id === id)
	return res.json(user)
})
.patch((req,res)=>{
 //patch 
})
```