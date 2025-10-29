# Request Body

When you need to send data from a client (let's say, a browser) to your API, you send it as a request body.


A request body sent data the client to your api.A Response Body is the data your API sends to the client

API almost always has to send response body.but client don't necessarily need to send request bodies all the time , sometimes they only request a path , maybe with some query parameters but don't send a body.


#### you use pydentic for declare a request body

## Results

1. read the body of the request as JSON

2. Convert the corresponding types(if needed)

3. validate the data

    - if data is invalid , it will return nice and clear ERROR , indicating exactly where and what was incorrectdata


## validation (pydentic (Request Body)) + path + query

            class items(BaseModel):
                n:str
                x:int
                y:int


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
                        **item
                    }
                }`


# multiple body parameters

declare multiple body parameters e.g. Item and User

    class Item(BaseModel):
        name: str
        description: str | None = None
        price: float
        tax: float | None = None


    class User(BaseModel):
        username: str
        full_name: str | None = None


    @routes.put("/user_data")
    async def user_data(user_id, item :items, user: User):
        return {'user_id':user_id ,"items":item , "user":user}

#  embeded a single body parameter


    @routes.put("/body_data")
    async def body_data(data : items = Body(embed=True)):
        # data = {"body_data":data}
        return data