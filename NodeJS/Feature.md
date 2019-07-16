##What is Node
- Node is runtime JavaScript that uses V8 engine written in C++, that takes in JS code and compiles into C++ code
- [npmjs.com](npmjs.com)  many packages

##Global
- 使用Global keyword可以获得全局变量，跟javascript的window一样
- 使用Process可以拿到Node Process 就像在JS的Document 可以拿到当面页面的Dom

##Feature
- Non-blocking IO（当作blocking IO操作的时候，接下来的操作被暂时阻挡了）
- 不等来自IO的data，下面的语句也可以进行了，等拿到data再做回调

![Non-blocking IO](../image/BlockingIO.PNG)

#Grammar

##Common lib to use
- app.js intialization file for Node

```NodeJs
//file system
const fs = require('fs');
//operation system
const os = require('os');
//will give username, pid, uid, homedir, shell path
var user = os.userInfo();
const notes = require('./notes.js ');

fs.writeFileSync('node.json', originalNoteString);
fs.readFileSync('notes.json');
```

##省略function keyword的anomynous function

```NodeJs
module.exports.add = (a, b) => {
  return a + b;
};
```

###lodash
```
  _.isString(string)
  //filter duplicates
  _.uniq(array)
```

###nodemon
- 能够生成一个即时反应的localhost
- 当nodemon project, 如果Project里的nodejs变了,那会自动重启这个project
- 使用control + c来结束nodemon

###command line 调入参数
```nodejs
var command = process.argv[2];
console.log('Command: ', command);
if (command == 'add') {

}

```
调用时
node app.js add remove

###yargs
- yargs can make passing arguments super easy
```
const yargs = require('yargs');
const argv = yargs.argv;

```

###json
```
var obj = {
  name : 'Andrew'
};
//这是一个string 会输出 {"name":"Andrew"} 生成了JSON Object的String形式
var stringObj = JSON.stringify(obj);

//personString是从JS file里边读出来的
var personString = '{"name", "Andrew", "age" : 25}';
//这是一个object, 把JSON 变成了 JSON Object
var person = JSON.parse(personString);
```
