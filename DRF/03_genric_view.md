# What is genric View

Django genrics is were devloped for shortcut for common use case they tack creatin common idioms and patterns.

they also provider by DRF

# mixins
mixins is a class that provide extra functionality to other class.they provide the basic class view behavior 


mixins are already provide few Mixins for defult methods ListModelMixin ,createModelMixin,RetrieveModelMixin,UpdateModelMixin,DestroyModelMixin

they all method provide a basic defult functionality they are not use direcly get,post,put(APIView) they provide .list ,create,retrieve,update,destroy method


when you use genric view and you override so you difine get or list in (listAPIView and so more) for override defult logics

### >>> some exmple are in DRF doucumentation and DRF github repo location DRF 06_genreic 


