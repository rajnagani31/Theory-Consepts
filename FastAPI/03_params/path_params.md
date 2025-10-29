# request Body


Request bodies are typically declared using Pydantic models.


    from fastapi import FastAPI
    from pydantic import BaseModel

    app = FastAPI()

    class Item(BaseModel):
        name: str
        description: str | None = None
        price: float
        tax: float | None = None

    @app.post("/items/")
    async def create_item(item: Item):
        return item

# 1. path parameters


path parameters are defined directly within path string of the route decorator

    " with path params"
    async def get_items(request : Request , user_id:Annotated[int,'enter a items ID']):
        return {
            "user_id":user_id,
            "method":request.method,
            "URL":str(request.url),
            "headers":dict(request.headers)
        }

# 2. Enum (Dropdown)

Enum mean is enumerations   
python is provide enum

1. Defininf fixed value of parametrs like status , codes and categories.

2. Improving code readability and maintaining a set of allowed values in a centralized location.

        from enum import Enum
        from pydantic import BaseModel
        from fastapi import FastAPI

        app = FastAPI()

        class Name(str , Enum):
            active = "active"
            inactive = "inactive"
            suspended = "suspended"


        class User(BaseModel):
            name : str
            status : Name


        @app.post("/name")
        def Name_status(status_data: Name = Name.active):
            if status_data is Name.inactive:
                return {
                    "model":status_data,
                    "status":200    
                }
            
            if status_data.value  == "suspended":
                return {
                    "model":"suspended",
                    "status":400,
                }
            return {"status": status_data}

## What use case of Enum

1. validation : Fast ApI is automatically validate that the value provide for status matches on of the Enum value

If user send value that is not defined ,Fast api will reponse with error

### OpanAPI DOCS

Enum likely show DropDown in swagger UI

