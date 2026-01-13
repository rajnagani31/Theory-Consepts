# what is select()

```bash

select means "select row from this table"

# SQLAlchemy Example:

student_details_table.select()

# SQL Example:

SELECT * FROM student_details;
```

# what is where()

```bash

where means "filter the rows based on some condition"

# SQLALchemy Example:

student_details_table.select().where(student_details_table.c.age > 18)

# SQL Example:
WHERE user_id = <value>

NOTE : django orm and sqlalchemy both uses where looks like this .filter()
```

# slicing in sqlalchemy

```bash
#  core SQLAlchemy Example:
student_details_table.select().where(student_details_table.c.age > 18).limit(5).offset(10)

# SQL Example:
SELECT * FROM student_details WHERE age > 18 LIMIT 5 OFFSET 10;

# django orm example:
StudentDetails.objects.filter(age__gt=18)[10:15]
```

# Drop student detail table table use one foring key and onother table use studet_detail(pk) as forgian key