# Project: 0x02. Python - Async Comprehension

## Learning Objectives
By the end of this project, you will be able to explain the following concepts without relying on external sources:

- How to write an asynchronous generator
- How to use async comprehensions
- How to type-annotate generators

## Writing an Asynchronous Generator
An asynchronous generator in Python allows for asynchronous operations during iteration. To write an asynchronous generator, follow these steps:

1. Define an asynchronous function using the `async def` syntax.
2. Use the `yield` statement to produce values asynchronously within the function.

Here's an example of an asynchronous generator that generates a sequence of numbers asynchronously:

```python
import asyncio

async def number_generator():
    for i in range(1, 5):
        await asyncio.sleep(1)  # Simulate an asynchronous operation
        yield i
