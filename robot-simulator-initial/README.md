Este directorio contiene una plantilla básica para comenzar a resolver el problema
de Exercism

Se aporta la definición de la clase (.h) con los dos constructores y el código mínimo necesario para que
pasen los primeros tests.

Se han incluído también los ficheros
* `Makefile`
* `robot_simulator_main.cc`

Para compilar el programa de forma independiente de los tests de Exercism

# Robot Simulator

Welcome to Robot Simulator on Exercism's C++ Track.
If you need help running the tests or submitting your code, check out `HELP.md`.

## Instructions

Write a robot simulator.

A robot factory's test facility needs a program to verify robot movements.

The robots have three possible movements:

- turn right
- turn left
- advance

Robots are placed on a hypothetical infinite grid, facing a particular
direction (north, east, south, or west) at a set of {x,y} coordinates,
e.g., {3,8}, with coordinates increasing to the north and east.

The robot then receives a number of instructions, at which point the
testing facility verifies the robot's new position, and in which
direction it is pointing.

- The letter-string "RAALAL" means:
  - Turn right
  - Advance twice
  - Turn left
  - Advance once
  - Turn left yet again
- Say a robot starts at {7, 3} facing north. Then running this stream
  of instructions should leave it at {9, 4} facing west.

## Source

### Created by

- @chgraef

### Contributed to by

- @elyashiv
- @KevinWMatthews
- @patricksjackson

### Based on

Inspired by an interview question at a famous company.