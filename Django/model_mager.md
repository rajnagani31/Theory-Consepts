# Django Model manager 

#### Django is Provide defult model manager in your own models 

#### This model manger is use for run your database query on your model

    Breakdown

    Student.objects.all()

    Student --> is the your model and model table create in database

    Objects --> is manage the talk with database using the Student model

    all()(data featch using SELECT Method bu defult) --> give all data of student table

# where is the show

    class student(models.model):
        your Field
        ...
        ..
        ...
        ..

        object=models.manager

        They not show in model.py file but is avaliable baydefult in your model

        > you can allshow make custom manager and you can change defult manager name
# defult and new

    object=models.Manager()

    # New

    manager=models.manager()

    you can also use 
    Studen.manager.all()
# Breakdown custom manager

    class PublishedBookManager(models.Manager):

#### -this line meaning is you inherit(models.manager) django class
<br>

    class PublishedBookManager(models.Manager):
    def get_queryset(self):
        return super().get_queryset().filter(is_published=True)

#### -get_queryset(self) : It's meaning is what data return when use all(),filter() etc to manager they overriding django defult behavior

#### -super().get_queryset() : call original data ,they give all record of the model

#### -.filter(is_published=True) : they give nedded data , get any data all(),filter(),__lukepus(),aggregate_functio(SUM,AVG,MIN,COUNT)Q(~,&,|),limit[:::],create,update

# Use case

1.creat custom method like range of age r1,r2
2.creat custom model give value 
3.most use sprete model for fix data and clean code
4.set proxy behaviyer
