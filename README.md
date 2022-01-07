# Node-With-mySql
step1: Connect node with Sql
```
var mysql=require('mysql');

var DatabaseConnectionConfig={host:"localhost", user:"root", password:""}

var con=mysql.createConnection(DatabaseConnectionConfig);

con.connect(function (error) {
    if(error){
        console.log("Connection Fail")
    }
    else{
        console.log("Connection Success");
        //InsertData(con);
        //DeleteDataByID(con)
       //UpdateData(con);
    }
});
```
