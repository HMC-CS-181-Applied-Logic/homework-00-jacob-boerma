## Part a

### Describe what the code in `z3-test.py` is doing in a paragraph or two.

The program starts off by creating booleans and integers a, b, x and y. It then defines a constraint 

not(a) ^ b ^ (x > 0) ^ (x < 100) ^ (x < y).

Then the code adds this constraint to a constraint-solver, and prints the result. 

Then the program adds the constraint 

(y < 1) 

to the problem, and then prints the result. 


The solver was able to satisfy the original constraints. It printed "sat" to indicate satisfiability, and came up with the example 

[And(Not(a), b, x > 0, x < 100, x < y)].

However, adding the second constraint (y < 1) breaks things, since x needs to be less than y as well as greater than zero. This is impossible, so the program printed "unsat" to indicate unsatisfiability. 