# ebooks
test
```
case class Employee(first_name:String, dept_no:Long)
val employeeDF = Seq( Employee("John", 31),
Employee("Jeff", 33),
Employee("Mary", 33),
Employee("Mandy", 34),
Employee("Julie", 34),
Employee("Kurt", null.asInstanceOf[Int])
).toDF
case class Dept(id:Long, name:String)
val deptDF = Seq( Dept(31, "Sales"),
Dept(33, "Engineering"),
Dept(34, "Finance"),
Dept(35, "Marketing")
).toDF
```