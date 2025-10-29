# What is Meta data

<h3> meta data is give about this data e.g. description

<br>

moreden way combine type hints with FastAPI request parameters

## App meta data (FastAPI use python modul Annoteted )

    from fastapi import FastAPI

    app = FastAPI(
        title="ToDo API",
        description="A simple API for managing tasks",
        version="1.0.0",
        terms_of_service="https://example.com/terms/",
        contact={
            "name": "Raj Nagani",
            "url": "https://example.com/contact",
            "email": "raj@example.com",
        },
        license_info={
            "name": "MIT License",
            "url": "https://opensource.org/licenses/MIT",
        },
    )


## 2. Route metadata

Each endpoint can have endpoint 

    from fastapi import FastAPI

    app = FastAPI()

    @app.get("/tasks", summary="Get all tasks", description="Returns a list of all tasks in the system")
    def get_tasks():
        return [{"id": 1, "title": "Learn FastAPI"}]

## 3. parameter metadata

    from fastapi import Query

    @app.get("/search")
    def search_tasks(q: str = Query(..., title="Search Query", description="The keyword to search tasks by")):
        return {"query": q}


## 4. model metadata


    from pydantic import BaseModel, Field

    class Task(BaseModel):
        title: str = Field(..., title="Task Title", description="The name of the task")
        completed: bool = Field(False, title="Completed", description="Whether the task is done")
