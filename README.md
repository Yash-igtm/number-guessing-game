A number guessing simulation with a random number generator and identifiers which help you to guess correctly
# Number Guessing Game

A console game in C++. The computer picks a secret number from 1 to 100, and you guess it. After each guess, the game tells you to go higher or lower. Play as many rounds as you like.

## Features

- New random secret number every round
- Higher or lower hints after each guess
- Replay without restarting the program

## Sample Output
Guess: 50
Go lower!
Guess: 25
Go higher!
Guess: 37
Congratulations! The number was 37.
Play the game again? (y/n): n
Thanks for playing!

## How It Works
Outer loop: play rounds while the player answers y
└── Inner loop: keep guessing until the guess is correct

The secret number comes from the `<random>` library:

```cpp
std::random_device rd;
std::mt19937 gen(rd());
std::uniform_int_distribution<int> dist(1, 100);
int secret = dist(gen);
```

## Requirements

- A C++ compiler with C++17 support, such as `g++`

## Getting Started

Compile:

```bash
g++ -std=c++17 guess.cpp -o guess
```

Run (use a terminal, since some online output panels don't accept typed input):

```bash
./guess        # Mac / Linux
guess.exe      # Windows
```

## Concepts Used

- `<random>` for random number generation
- Nested `while` loops
- `if` / `else` conditions
- `char` input for yes/no answers

## Possible Improvements

- Limit the number of attempts
- Track and display the number of guesses
- Add difficulty levels

## Author

Yash, first-year B.Tech student interested in cloud computing and fintech.

## License

Open for learning. Feel free to use and modify.