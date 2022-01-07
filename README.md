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
## Delete Data
```
function DeleteData(con) {
      let SQLQuery="DELETE FROM `students_list` WHERE  `id`='1'"
    con.query(SQLQuery, function (error) {
        if (error) {
            console.log("Data delete Fail")
        }
        else {
            console.log("Data delete Success");
        }
    });
}
```

## UpdateData Data
```
function UpdateData(con) {
      let SQLQuery="UPDATE `students_list` SET `name`='Moheuddin Monna', `phone`='019999999',`city`='Cumilla' WHERE `id`= '3' "
    con.query(SQLQuery, function (error) {
        if (error) {
            console.log("Update Data Fail")
        }
        else {
            console.log("Update Data Success");
        }
    });
}
```
## Select Data
```
function SelectData(con) {
      let SQLQuery="SELECT * FROM `students_list`  "
    con.query(SQLQuery, function (error, result) {
        if (error) {
            console.log("SELECT Data Fail")
        }
        else {
            console.log(result);
        }
    });
}
```
