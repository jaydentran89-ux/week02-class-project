# Week 02 Class Project: Ohm's Law Calculator

## Purpose
A terminal program that reads a voltage and a resistance and prints the current using Ohm's law (I = V / R).

## Input format
Two numbers separated by a space: voltage in volts, then resistance in ohms.

## Build and run
    g++ -std=c++17 -Wall -Wextra -pedantic src/main.cpp -o build/app
    ./build/app

Run all acceptance tests:

    bash test.sh

## Example
| Input  | Output         |
|--------|----------------|
| `12 4` | `Current: 3 A` |
| `12 0` | `Invalid input` |

## Limitations
- The program prints the same "Invalid input" message for every error, so the user can't tell whether the voltage or the resistance was the problem.
- Anything typed after the first two numbers is silently ignored, so an input like `12 4 99` is still accepted.
- Negative voltages are accepted and produce a negative current, which may not be what every user expects.

## Debugging reflection
Because I created the repository empty, my first push made `feature/implementation` the only branch, so there was no `main` to open a pull request against. 
I fixed this by creating an empty `main` branch with an initial commit, rebasing my feature branch onto it, and force-pushing, which let me open and merge 
the pull request normally. I also learned that VS Code's `code` command isn't installed in the terminal by default on macOS, 
so I opened the project folder through File → Open Folder instead.
