# *args

meaning : numbur of arguments

Type: Passed into a function as a tuple.

Use case: When you don’t know beforehand how many positional arguments a function will receive.

    def add_numbers(*args):
    print(args)  # tuple of arguments
    return sum(args)

    print(add_numbers(1, 2, 3))      # 6
    print(add_numbers(10, 20, 30, 5)) # 65

    they eccepts Positional Argument

# **kwargs

Meaning : variable number of Keyword arguments

Type : Passed into a function as a dictionary.

Use Case : When you don’t know beforehand how many named parameters will be received.

    def print_details(**kwargs):
        print(kwargs)  # dictionary of arguments
        for key, value in kwargs.items():
            print(f"{key}: {value}")

    print_details(name="Raj", age=21, city="Surat")

    They eccepts keyword Argument


# combine exmples

    def demo(*args, **kwargs):
    print("args:", args)
    print("kwargs:", kwargs)

    demo(1, 2, 3, name="Raj", age=21)
