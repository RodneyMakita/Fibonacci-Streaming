# Fibonacci Generator
This Python utility provides a generator function for generating an infinite sequence of Fibonacci numbers. The Fibonacci sequence starts with two 1s, and every subsequent number is the sum of the two previous numbers.

## Usage
Here's how you can use the Fibonacci generator:

Define the generator function:

```python
def all_fibonacci_numbers():
    a, b = 1, 1
    yield a
    yield b
    while True:
        a, b = b, a + b
        yield b
```
Create a generator object:
```python
fib_gen = all_fibonacci_numbers()
Iterate over the generator to get Fibonacci numbers:
python
Copy code
for i in range(10):
    print(next(fib_gen))
```
This will print the first 10 Fibonacci numbers.

### How It Works

The all_fibonacci_numbers function uses a generator to yield Fibonacci numbers one at a time. It starts with two 1s and then generates subsequent numbers by adding the previous two numbers together.

The generator can be used to efficiently generate Fibonacci numbers on-the-fly without having to store the entire sequence in memory.
