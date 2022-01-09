# Python style and coding guide
This style guide is for contributions to any repository [found here](https://github.com/alexdelorenzo/). It's based on PEP8 with some additions when it comes to typing.

# Guide
There are two sections, [Style](/#style) and [Coding](/#coding).

## Style
  - Assume [PEP8 guidelines](https://www.python.org/dev/peps/pep-0008/). 
  - Instead of using 4 spaces for indents, contributions should use 2 spaces.
  - Assume 80 character width limits, although 120 character limits can be used sparingly for clarity.
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

## Coding
  - Use immutable objects by default. That means using `tuple`s, `frozenset`s, `NamedTuple`s and frozen `dataclasses`.
  - Prefer `NamedTuple`s and `dataclasses` to bare classes. Use the former when iteration over attributes matters, or for object destructuring.
  - Take advantage of nominal and structural typing with `abc.ABC` and`typing.Protocol`.
  - Use type hints for all functions and methods, constants, and class and instance attributes.
  - Variables pointing to collections should have type hints.
  - Types should be treated as static. If they change, then types must be casted with `typing.cast()`.
  - Use generics and generic type hints.
  - Keep `mypy` happy.
  - Use lazy iterables wherever possible.
