# Dissertation

These are the algorithms I used for the computations in my PhD research on Littlewood's conjecture (in simultaneous Diophantine approximation).

LW.nb is a Mathematica (version 8.0) notebook. I've been rewriting these algorithms in Python, and when I'm finished with that I'll put it up here too.

# Notes

The first few functions (mod1, LWNorm, LWProd, SqrtMod1) are for calculations related to Littlewood's conjecture.

The rest are functions that set up a number field K=Q(theta) (represented by a matrix ring of the form Q[T] for a special matrix T), perform arithmetic in K using matrix operations, or are related to simultaneous approximations of powers of theta.

# Instructions

Say theta is an algebraic number that solves

x^n = c_(n-1) * x ^ (n-1) + ... c_1 * x + c_0.

We represent this polynomial by 

poly = {c_0, c_1, ... , c_(n-1)},

and then

NFInit[poly]

sets up the field (which we implement as a matrix ring) and defines some constants. We represent numbers

a_0 + a_1 * theta + a_2 * theta^2 + ... + a_(n-1) * theta^(n-1)

by vectors

{a_0, a_1, ... , a_(n-1)}.

We add and subtract component-wise. We multiply and divide with KMul and KDiv. Exponentiation by an integer is done by KExp.
