# my doubts

- what is "this._io"? what is the purpose of the  "underscore"?
- what is context api? what is Redux ?
# the process
install turborepo
```
npx create-turbo@latest
```

create a server folder inside apps
```
cd apps
mkdir server 
cd server
touch package.json
```
inside package.json
```
{
	"name":"server",
	"version":"1.0.0",
	"private":true,
	"script":{
		"dev":"tsc-watch --onSuccess \"node dist/index.js""
	}
}
```

```
yarn workspace server add typescript -D
yarn workspace server add tsc-watch -D
cd apps/server 
tsc init
```

edit the tsconfig.json file 
```
rootDir":"./scr"

outDir":"./dist"
```

