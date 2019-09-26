# Automated-theorem-prover-for-propositional-logic
Automated theorem prover for propositional logic which uses sequent calculus. Written in MAXIMA.

As a research assistant in Tampere University I was tasked with creating moodle exercises using the STACK environment for
courses in propositional logic and first-order logic. To be able to do that I had to learn the programming language MAXIMA. 
This code is one of the projects that I did with MAXIMA while trying to learn it.

As the description states this is an automated theorem prover for propositional logic. As an input it is given two sets
of sentences of propositional logic A and B. The program tries to check whether or not A => B holds, or in other words, if we write
A = {A_1,...,A_n}, B = {B_1,...,B_m}, whether or not (A_1 and ... and A_n) => (B_1 or ... or B_m). The program starts by eliminating
implications and equivalences from the sentences by replacing them with AND, OR and NOT. Then it applies the rules of
sequent calculus to reduce the complexity of the formulas and it checks whether it will only end up with formulas of the form A_i => A_i
which are tautologies. If it does, then the sentence is tautology, and otherwise it is not.

In my understanding Hao Wang was the first one to introduce this sort of automated theorem prover for propositional logic, or at least
it is often discussed as Hao Wangs algorithm.

The program will print out what rules it is applying and what are the results of applying those rules. The code also contains
a simple algorithm for generating random instances of sentences of propositional logic. Calling Prove_using_Wang(x,m,n) will generate
x random sentences with m connectives and n negations, and the algorithm will check for each of them whether or not they are a tautology.
