# what is genretor 

genretor  python is a special function that uses yield instead of return to produce a values one at a time without storing everyting a memory

# Difference between return and Yield

## return
- Ends of the function give one vlue
- function stop aftter return 
- value produced -> only once
- memory use -> store everything if you want multiple values

## yield 
- pauses the function and gives one value at a time
- function can continue from where it left off
- value produced - can produce many values (like a sequence)
- memory use -> more memory efficient (lazy evaluation)

NOTE : yield gives result many time and remember state , continues later

# why are Generators used in python ?

memory efficient = They don’t store all values in memory, only produce them when needed.

faster Execution = Good for large datasets (like streming files, logs or infinite sequencess)


Lazy evaluation: Values are generated only when requested, not upfront.

Readable code: yield makes complex iterators easier to write.

# generator most usfull in Django and FastAPI

## Django

1. Streaming large files (CSV, Excel, logs) to client
2. Background tasks
3. Handling QuerySets efficiently

## FastAPI

1. Streaming large responses
2. Processing big files upload
3. Server-Sent Events (SSE) / Live updates