# What is FastAPI Dependencies?

Dependencies in simple meaning is instead of manually creating instance of services , utilities , or data object inside your route functions , FastAPI allows you to declare the dependencies and it will inject them autometically when the funcction is called.

# This is Very useful when you need to:

- Have Shared logic (the same code logic again and again)
- share database connection.
- Eforce security ,authentication , role requrements, etc.
- And many other things

# FastAPI compatibility¶
The simplicity of the dependencies injection system makes FastAPI compatible with:

- all the relational databases
- NoSQL databases
- external packages
- external APIs
- authentication and authorization systems
- API usage monitoring systems
- response data injection systems
- etc.


# Class Based depends

FastAPI a Provide class bassed Dependencies decler logic in pythonic class 

fake_items_db = [{"item_name": "Foo"}, {"item_name": "Bar"}, {"item_name": "Baz"}]


    class CommonQueryParams:
        def __init__(self, q: str | None = None, skip: int = 0, limit: int = 1000):
            self.q = q
            self.skip = skip
            self.limit = limit


    @app.get("/items/")
    async def read_items(commons: Annotated[Any, Depends(CommonQueryParams)]):
        response = {}
        if commons.q:
            response.update({"q": commons.q})
        items = fake_items_db[commons.skip : commons.skip + commons.limit]
        response.update({"items": items})
        return response

# Sub-dependencies

main dependencies used in sub dependencies when fastapi use sub dependencies they use main depedency and this main dependencies have used many places

        from typing import Annotated

        from fastapi import Cookie, Depends, FastAPI

        app = FastAPI()


        def query_extractor(q: str | None = None):
            return q


        def query_or_cookie_extractor(
            q: Annotated[str, Depends(query_extractor)],
            last_query: Annotated[str | None, Cookie()] = None,
        ):
            if not q:
                return last_query
            return q


        @app.get("/items/")
        async def read_query(
            query_or_default: Annotated[str, Depends(query_or_cookie_extractor)],
        ):
            return {"q_or_cookie": query_or_default}


# Dependencies with path opration

In some cases you don't really need the return value of a dependency inside your path operation function.

Or the dependency doesn't return a value.

But you still need it to be executed/solved.

For those cases, instead of declaring a path operation function parameter with Depends, you can add a list of dependencies to the path operation decorator.




    @router.post("/decoretor_depends" , dependencies = [Depends(verify_token), Depends(verify_key)])
    async def cheak_token(x):
        function = await asyncio.gather(
            cheak_asyncio.cheak("This is function"),
            cheak_asyncio.cheak_again("This is function")
        )
        data =[f for f in function]
        print(data)
        return JSONResponse(status_code=200 , content={"data":data , "Token": "Valid token and secret key"}, media_type="application/json")