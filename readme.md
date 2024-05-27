# Back to node js again...

### This is a run time environment for javascript to use javascript outside the browser. 
## By "RYAN DAHL."

#### we can define node js as :

```
 node js = (google chrome's engine created in c++) V8 engine + javascript repper code
 ```

 ### Steps to begin :

 -  install node js for your os
 -  check the installation if err
 -  get basic understanding of npm "nahi pta mujhe"
 -  create new node js file with the command 
###### this will ask some questions related to project
 ```javascript
 npm init
 ```
###### this will build your packege.json file
 ```
 npm init -y
 ```
 -  understand how to read out the docs go to nodejs.org/docs
 -  be familiar with moduls like 
```javascript
//  file system, http, many more;
```
### File system module :
```javascript
const fs = require("fs");
```

##### You need to learn how : 
- you can write/create a file

```javascript
fs.writeFile("filename.ext","data",callback(err));
```
callback for handle error in between the process.

-   appending text to the file

```javascript
fs.appandFile("filename.ext","data",callback(err));
```
-   rename file

```javascript
fs.rename("filename.ext","newNameToFile",callback(err));
```
-   copy file

```javascript
fs.copyFile("firstfilenameOrPath","secondfilenameOrPath",callback(err));
```
Data of first file will be copied into the second file if everything heppn correctly or it will show specific error message.

- deleting a file 

```javascript
fs.unlink("filename.ext",callback(err));
```

- deleting an empty directory  (we can use "rm" or "rmdir")

```javascript
fs.rm("directorypath",callback(err));
```

- deleting a directory with files (we can use "rm" or "rmdir")

```javascript
fs.rm("directorypath",{recursive:true},callback(err));
```
this recursive is an optional argument, which is importent for delete the directory with files.

### Http module : 

##### you need to unerstand following topics to step up -

```javascript
const http = require('http');
```

- creating server with the help of HTTP module of node js

```javascript
//server via http method ✅
const http = require('http');
http.createServer((req,res)=>{
  res.writeHead(200,{content_type:"plane/text"});
  res.end("hello sir ... server is created by traditional http method");
}).listen(3000,()=>{
  console.log('on http://localhost:3000/');
})
```


### NPM :

- installing npm packeges
```
npm install packegename
```
or we can only use i to indicate install keyword

- uninstalling npm packeges
```
npm uninstall packegename
```
- installing particular version for specific packege
```
npm i packegename@version
```

### Node module folder

    whenever  you install any packege for particular work, it will install another required packeges for proper functioning of that packege into node module folder as well.
 #### Hence : 
- Dependencies : are these packeges & another required packeges for proper functioning of the application.

- Devdependencies : are those packeges, which are used in development phase only.

### Expres :

- create a server with express in an easy way then http method
```javascript
// server via express method ✅

const express = require("express")
const app = express()
app.get("/",(req,res)=>{
  res.send("hello sir.. server is created by express")
}).listen(3000,()=>{
  console.log("check on http://localhost:3000");
})
```

## Enough for today✅