# query parameters

When decler a function parameters that are not part of the path parameters ,that are automatically interpreted as "query" parameters.

let's walk through with an example:

    @routes.post("/items/{item_id}" , description="data with optional and type(bool) parameters") 
    def get_user_data(item_id ,item: items  ,user_id :int | None = None , q:str | None = None , short : bool = False):
        if user_id is None:
            return {
                "status":400,
                "error":"Not Found User id"
            }
        return {
            "staus":200,
            "message":{
                "user_id":user_id,
                "data":q,
                "short":short,
                "item_id":item_id,
                "item":item
            }
        }

        here {item_id} is only path parameters another all function parameter is are query params


# Query parameters with string,numeric validations


## 
Generic validations and metadata:

- alias
    - alias use for chang URL parameters name

            @routes.get('/all_items/')
            def read_items(q : Annotated[list[str] , Query(alias="pk")] = ['A','b',1]):
                data_items = {"q":q}
                return data_items

            here Url http://127.0.0.1:8000/all_items/?pk=A&pk=b&pk=D

            without alias
            http://127.0.0.1:8000/all_items/?q=A&q=b&q=D
- title
- description
- deprecated


## Validations specific for strings:


- min_length
- max_length
- pattern
- gt
- lt
- ge
- le

## Custom validation

1. regex 

    - Simple string patter validtaion


            @app.get("/users/")
            async def get_users(email: str = Query(..., regex=r"^[\w\.-]+@[\w\.-]+\.\w+$")):
                return {"email": email}

2. Pydentic validator 

    - Custom, complex validation logic (numbers, strings, cross-field checks)


            class UserData(BaseModel):
                name : str
                age : int

                @validator("age")
                def age_must_be_positive(cls , v):
                    if v <= 0:
                        raise ValueError("Age must be positive")
                    return v
            

            @routes.get("/costom validation/")
            def age_data(name: str , age : int):
                try:
                    user = UserData(name = name , age = age)
                    return user
                
                except ValueError as e:
                    raise HTTPException(status_code=400,    detail=str(e))