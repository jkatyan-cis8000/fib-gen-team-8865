# ARCHITECTURE.md

Written by team-lead before spawning teammates. This is the shared blueprint —
teammates read it to understand what they are building and how their module fits.
Update it when the structure changes; do not let it drift from the actual code.

## Module Structure

- `fibonacci.py`: Core Fibonacci generator module with main logic
  - `generate_fibonacci(n)`: Generate Fibonacci numbers up to n
  - `generate_fibonacci_count(count)`: Generate first `count` Fibonacci numbers
- `main.py`: CLI entry point that accepts user input and displays results
- `tests/test_fibonacci.py`: Unit tests for the fibonacci module

## Interfaces

### fibonacci.py
- `generate_fibonacci(n: int) -> list[int]`: Returns list of Fibonacci numbers <= n
- `generate_fibonacci_count(count: int) -> list[int]`: Returns first `count` Fibonacci numbers
- Both functions validate input and raise ValueError for negative numbers

### main.py
- `parse_args()`: Parse command line arguments (--limit or --count)
- `main()`: Entry point that coordinates generation and output

## Shared Data Structures

- `list[int]`: Return type for all Fibonacci generation functions
- CLI argument structure:
  - `--limit n`: Generate all Fibonacci numbers up to and including n
  - `--count n`: Generate the first n Fibonacci numbers

## External Dependencies

- None required. Uses only Python standard library.
