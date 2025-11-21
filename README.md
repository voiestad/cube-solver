# Cube Solver
The cube solver is a Haskell program that generates a PDF solving manual from a Rubik's cube scramble.
This is a base solver and it is used in my server and bluetooth versions, but can also be used as a standalone application.

## Other versions
- [Server](https://github.com/voiestad/cube-solver-server): Starts an API that takes a scramble and gives a PDF solution as Base64 response.
- [Bluetooth](https://github.com/voiestad/cube-solver-bluetooth): Connects to a GAN bluetooth cube and gives live update of the PDF solution.

## Before running
- Create a `scramble.in` file in the project directory containing a scramble using the template below. The orientation of the cube should be green in the front and white on the top. NOTE: This will not work with cubes that do not follow the standard color scheme.

## Scramble input example file
### Notes 
- The parser is not case sensitive and will accept both lower and upper case.
- The file should always end with either the last color or white space.
- The spacing for the white and yellow faces can be present and is recommended for manual input, but is not necessary.
### Face color to letter mapping
| Color   | Letter |
|---------|--------|
| White   | W      |
| Orange  | O      |
| Green   | G      |
| Red     | R      |
| Blue    | B      |
| Yellow  | Y      |
### Solved cube
```
   WWW
   WWW
   WWW
OOOGGGRRRBBB
OOOGGGRRRBBB
OOOGGGRRRBBB
   YYY
   YYY
   YYY

```
### Scrambled cube
```
   YBR
   RWR
   OYB
GYGWBOWGWGWR
OOGOGRWRGYBW
GYOYWWBOBYBO
   BGR
   OYB
   YRR

```

## How to run
```
cabal run
```

## Credit
- ["Rubik's Cube: Why are some cases impossible to solve?" - by Dylan Wang AKA "JPerm" on YouTube](https://youtu.be/o-RxLzRe2YE?si=PNoy7rsajMeGU8o2)
- [PLL: E perm and Z perm from SpeedCubeDB](https://speedcubedb.com/a/3x3/PLL)
- [Names of OLL cases from jperm.net](https://jperm.net/algs/2look/oll)
- [OLL algorithms from jperm.net](https://jperm.net/algs/oll)
