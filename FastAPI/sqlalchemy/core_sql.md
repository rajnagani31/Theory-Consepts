# what is core sqlalchemy in sqlalchemy

Is a open source python sql toolkit and object relational mapper(ORM) that provides a flexible and powerful way for developer for intract with relational datavbse using python code instead of writing raw sql queries

```bash
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

# Core SQLAAlchemy Example:

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

# distinct in sqlalchemy

```bash
stmt = select(users_table.c.id, func.count(distinct(users_table.c.name)))

DISTINCT keyword is used to return individual values (no duplicates)
```

# select_from

```bash

I want one aggregate value - the total number of value

select_from is usef to 'count row frm this table'

where - this filter rows before counting

example:
count_query = ( select(func.count()) .select_from(student_details_table) .where( student_details_table.c.user_id == user_id, student_details_table.c.student_name == "rajjjjj" ) )
```

# group_by
