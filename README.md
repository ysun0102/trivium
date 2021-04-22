# Cube attack on Trivium
This is the repository for the paper "An efficient algorithm of searching cubes for attacking Trivium".

## Contents

1. [Code for verifying part of the super polynomial for 843-round Trivium]: trivium_verify.cpp.
2. [Monomials in the super polynomial of the cube {0, 1, ..., 79}/{30, 76}]: superpoly/raw_monomials, superpoly/super_poly_monomials.
3. [Logs for computed results]: log/.

 ## Usage of the Codes

### Dependencies

Please first install [Gurobi solver](https://www.gurobi.com) and set a proper license. 

### Compile 

Please edit "Makefile" according to your configuration. Then type 

`make`

to compile the codes.

### Run the program

After you compile the code, please type 

`./trivium_verify [ROUND] [INDEX] [KEY_INDEX]`  

for run.

The possible combinations of (ROUND, INDEX, KEY_INDEX) are listed as follows, 
1. ROUND = 843, INDEX = 1, KEY_INDEX = 0:
    Recover part of the super polynomial for the cube {0,1,...,79}/{30, 76} of 843-round Trivium, which consists of all monomials involving k0.

2. ROUND = 843, INDEX = 1, KEY_INDEX = 2:
    Recover part of the super polynomial for the cube {0,1,...,79}/{30, 76} of 843-round Trivium, which consists of all monomials involving k2. The output should be a single monomial "k2", which means no other monomials in the super polynomial contain the variable k2, so this super polynomial is a balance polynomial.
