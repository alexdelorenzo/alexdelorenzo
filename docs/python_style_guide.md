# Python style guide
This style guide is for contributions to any repository [found here](https://github.com/alexdelorenzo/). It's pretty simple.

# Style
  - Assume PEP8 guidelines. 
  - Instead of using 4 spaces for indents, contributions should use 2 spaces.
  - Assume 80 character width limits, although 120 character limits can be used sparingly for clarity.
  - Use immutable objects by default. That means using `tuple`s, `frozenset`s, `NamedTuple`s and frozen `dataclasses`.
  - Prefer `NamedTuple`s and `dataclasses`. Use the former when iteration over attributes matters, or for object destructuring.
  - Use type hints for all functions and methods, constants, and class and instance attributes.
  - Variables pointing to collections should have type hints.
  - Types should be treated as static. If they change, then variables must be casted with `typing.cast()`.
  - Use generics and generic type hints.
  - Keep `mypy` happy.
  - Prefer using lazy iterators wherever possible.
  - Include trailing commas.
  - No hanging indents. Prefer this:
  ```python3
  # no
  function_name(param1, 
                param2, 
                param3, 
                param4)

  # yes
  function_name(
    param1,
    param2,
    param3,
    param4,
  )
  ```
