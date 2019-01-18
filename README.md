# node_mysql
使用node连接mysql的demo案例

新建文件夹demo

1. 切到node文件没有了，通过git `npm install` 会自动生成 `package-lock.json` 和 `package.json` 文件
2. 安装 mysql 环境 `npm install mysql` 自动生成 `node_modules` 文件目录
3. 开启数据库，新建一个数据库和表测试使用
4. 初始化 app.js 文件
5. 切到文件目录，运行 `app.js` 即可

```
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'root',
  password : 'root',
  database : 'test'
});
 
connection.connect();
 
connection.query('select * from student', function (error, results, fields) {
  if (error) throw error;
  console.log('The solution is: ', results);
});
 
connection.end();
```

