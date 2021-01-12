# 12-JAN-2021

## Data types, operators, and variables

* Data types
    1. `dict` - Dictionary
        * labeled list
        * similar to Java map
    2. `NoneType`
        * absence of a value
        * null
    3. `str`
        * format string
            * `f"My favorite number is {favorite number} which is half of {favorite_number * 2}"`
            * allows for concatenating different data types without explicitly casting
    4. `list`
        * the list methods modify the list without explicit reassignment
        * list comprehension
            * special syntax that produces new lists
            * `new_list = [(n + 1) for n in list if (n % 2 == 0)]`
    5. tuple
        * immutable lists (cannot be changed)
        * to get a mutable version: `not_tuple = list(tuple)`
    6. `dict`
        * dictionary literal syntax:  `dictionary_name = {key : value}`
        * alternate syntax:  `dictionary_name = dict(); dictionary_name[key] = value`
        * alternate syntax:  `dictionary_name = dict(key = value)`
    * `type(value)`
        * returns the type of the value
    * Python is not type strict like Java.
        * The same variable can hold a transformed version of itself even if the transformed version is of a different data type.
* Variables
    * Formatting convention is snake case
        * snake_case_variable_name
* In Jupyter and VSCode, you can put multiple cursors on lines by holding Option (Alt on Windows) and click where you want your other cursors
* Restart the Jupyter notebook using the Kernal tab if it gets stuck in a process
* Operators
    * `in`
        * checks for membership
* In Jupyter notebook, you can put a question mark after a function and execute the statement to get the documentation for the function
    * `"String".upper?`
