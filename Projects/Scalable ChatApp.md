inatall turborepo
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
	"private":true
}
```

```
yarn workspace server add typescript -D
yarn workspace server add tsc-watch -D
```