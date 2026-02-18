# what is middleware?

### HTTP request

```bash

➡️ Client Request → Django View → Response → Client

```

### HTTP request with middleware
```bash
Client
  ↓
Middleware (request)
  ↓
View
  ↓
Middleware (response)
  ↓
Client
```

# why middleware is used

Authentication(who you are) / Authorization(what you can do)

Rate limiting (like your Redis example) (limt for any system access)

Logging requests & responses

Adding headers

CORS handling

Security checks

Performance monitoring

👉 Logic that should run for every request, not just one API.


# Types of middleware

## 1️⃣ Request Middleware

Runs before the view(main logic)

#### Used to :

- Block request
- Modify request
- Attach extra data to request
- Auth check
- Rate limiting
- IP blocking

```bash
Client → Request Middleware → View → Client

Diraction -> if you have 4 middleware so, that work on disending

4->3->2->1 
```

NOTE : 👉 Request middleware NEVER runs after the view

## 2️⃣ Response Middleware

### What is Respomse middleware?

Response middleware is the part of middleware that runs after the view returns a response, but before it's sent to the client

```bash
Response middleware runs AFTER the view

Client → Request Middleware → View → Response Middleware → Client

```

NOTE :

-> 👉 Response middleware NEVER runs before the view
<br>
-> 👉 Runs after the view
<br>


#### Used to:

- Modify response
- Add headers
- Log response status
- Transform output
- Add headers
- Logging response
- Compress response

#### Execution Order
```bash

Middleware =[
    "a",
    "b",
    "c"
]

-> Request flow

- View → C → B → A

-> Response flow

- A → B → C → View
⚠️ Request middleware runs in reverse order
```

#### Middleware has TWO PHASES

```bash
Client
  ↓
(Request phase of middleware) (only for request logic don't use response logic in middleware)
  ↓
View
  ↓
(Response phase of middleware)  ← THIS is response middleware (only for after response(api) never use Requst logic in a middleware)
  ↓
Client

```
# When Should YOU Use Middleware?

- ✔ Logic applies to many APIs
- ✔ Needs to run before or after view
- ✔ Not related to business logic

❌ Don’t put:

- Database-heavy business logic
- Feature-specific logic

One-Line Summary

Middleware is a global hook to procees requests before view and responses after views.Response middelware modifies or inspects the response before sending to client.


## Middleware consept with FastAPI

FastAPI provide manly two type of middleware 

- request middleware (always run before endpoint)

- response middleware (always run after endpoint)


### CODE

#### Function based middleware execute

``` bash

@app.middleware("http")
async def simple_middleware(request: Request, call_next):
    # 🔹 REQUEST MIDDLEWARE
    print("Before endpoint")

    response = await call_next(request)

    # # 🔹 RESPONSE MIDDLEWARE
    # print("After endpoint")
    status = response.status_code
    if status == 500:
        return JSONResponse(content={"details":"Internl server error"}) # For generate error after response and send before client

    return response

NOTE : await call_next(request) this line is fix, so never change call_next name.

then after run response middleware logic like cheak status code.
```

#### class based middleware

```bash
class LoggingMiddleware(BaseHTTPMiddleware):
    async def dispatch(self, request: Request, call_next):
        print("Before endpoint")

        response = await call_next(request)

        print("After endpoint")
        return response

NOTE: same thigs as function based
```

## Inportent note

#### decleration

```bash


# for function based
@app.middleware('http')
async def register_middleware(request: Request, call_next):
    return await demo_simple_middleware(request, call_next)

# for class based
app.add_middleware(StoreUserRequestMiddleware)

# in django you know alerdy

django deccler in settings.py file

# same logic and consept use both fream work
```

# 🔑 Key rule (this explains everything)

```bash
FastAPI executes middleware in REVERSE order of how they are added/declared.

# There are two ways you’re adding middleware:

-> @app.middleware("http") → added immediately

-> app.add_middleware(...) → added last

FastAPI builds a stack (LIFO — last in, first out).