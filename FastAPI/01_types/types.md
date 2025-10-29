# what is type?

FastAPI is use python typing modual for "type hints"

By declering types for your variables,editors nad tools can give better support

FastAPI is all besed on these type hints , they give manu advantages and benefits

int , str , float , bool , bytes , List , Dict ,tuple , set , Union

    def process_items(items: list[str]):
    for item in items:
        print(item)

    
# Tuple
    def process_items(*items: tuple[str]):
        print(items)


    process_items(1,2,3,'5',5.7)

# Optional | None

    def home(name : str | None = None):
        if name is not None:
            print(f"Name is {name}")
        else:
            print("Name is None")

    home()            


# classes as types

    class person:
        def __init__(self , name):
            self.name = name

    def get_person(name_person : person):
        return name_person        

    print(get_person('raj'))


### many more method used for create hints....  