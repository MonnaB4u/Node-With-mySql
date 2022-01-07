# Node-With-mySql
## Connect node with Sql
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
       
    }
});
```
## Insert Data
```
function InsertData(con) {
      let SQLQuery="INSERT INTO `students_list`(`name`, `roll`, `class`, `phone`, `city`) VALUES ('Monna','03','CS','016','Dhaka')"
    con.query(SQLQuery, function (error) {
        if (error) {
            console.log("Data insert Fail")
        }
        else {
            console.log("Data insert Success");
        }
    });
}
```
