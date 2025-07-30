# many to many


many to many relation use for seleact a multi choice at on time or many user.

Ex.
Choice:java,python,c++,Java scripts

u1:python
u2:java,python
u3:java scripts,java,c++

it mean any user choice any leanguage ,any leanguage choice a user

    methods

    1.def write(self):
        return ",".join([str(p) for p in self.choices.all()])

        admin penel show leanguage details in string

    2.user=models.ForeignKey(User,on_delete=models.PROTECT)
    
    3.user=models.ForeignKey(User,on_delete=models.SET_NULL,null=True)

    4.user=models.OneToOneField(User,on_delete=models.PROTECT,limit_choices_to{'is_staff':False})
    
    5.user=models.OneToOneField(User,on_delete=models.CASCADE)

