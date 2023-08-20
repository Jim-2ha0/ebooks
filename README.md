# ebooks
test
```
case class Employee(first_name:String, dept_no:Long)
val employeeDF = Seq( 
    Employee("John", 31), Employee("Jeff", 33),
    Employee("Mary", 33), Employee("Mandy", 34),
    Employee("Julie", 34), Employee("Kurt", null.asInstanceOf[Int])
).toDF
case class Dept(id:Long, name:String)
val deptDF = Seq( 
    Dept(31, "Sales"), Dept(33, "Engineering"),
    Dept(34, "Finance"), Dept(35, "Marketing")
).toDF
```

## Table 4-2. Join Types
|Type| Description|
|-|-|
|Inner join (a.k.a. equi-join)|Return rows from both datasets when the join expression evaluates to true.|
|Left outer join |Return rows from the left dataset even when the join expression evaluates as false.|
|Right outer join |Return rows from the right dataset even when the join expression evaluates as false.|
|Outer join |Return rows from both datasets even when the join expression evaluates as false.|
|Left anti-join |Return rows only from the left dataset when the join expression evaluates as false.|
|Left semi-join |Return rows only from the left dataset when the join expression evaluates to true.|
|Cross (a.k.a. Cartesian) |Return rows by combining each row from the left dataset with each row in the right dataset. the number of rows is a product of the size of each dataset.|

employeeDF.crossJoin(deptDF).count