# Conway's Game of Life Simulator

This project implements Conway's Game of Life, a cellular automaton simulation, in C using the ncurses library for visualization.

## Author

Rodolfo Lopez

## Date

October 18, 2020

## Features

- Configurable world size and initial state
- Step-by-step or continuous simulation modes
- Adjustable delay between generations
- Toroidal (wrap-around) world boundaries

## Requirements

- C compiler (gcc recommended)
- ncurses library
- UNIX-like environment (Linux, macOS, or WSL on Windows)

## Compilation

To compile the project, run:

```
make
```

This will generate the executable `gol`.

## Usage

```
./gol [-s] -c <config-file> -t <number of turns> -d <delay in ms>
```

Options:

- `-s`: Enable step mode (wait for user input between generations)
- `-c`: Specify the configuration file (required)
- `-t`: Set the number of turns/generations (default: 20)
- `-d`: Set the delay between generations in milliseconds (default: 250)

### Example

To run the simulation with the R-pentomino pattern for 100 generations and a 100ms delay:

```
./gol -c tests/r-pentomino.txt -t 100 -d 100
```

## Configuration File Format

```
<num_rows>
<num_cols>
<num_live_cells>
<col1> <row1>
<col2> <row2>
...
```

Example configuration files are provided in the `tests/` directory.

## Controls

In step mode, press any key to advance to the next generation.
To exit the simulation, press any key after the final generation.

## Acknowledgements

Professor Sat Garcia wrote the starter code and I implemented the rest.
