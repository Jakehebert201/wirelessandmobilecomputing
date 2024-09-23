Jacob Hebert

CSCI 4957/5957 – Wireless & Mobile Networks
HW # 3- Fall 2024
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Instruction: Write clearly and give full justification to your answers. Show all your working and claims with clear abstraction or citation. Homework is due on 09/24/2024 in class. Late work will not be accepted.  Max points 20
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Page # 110 - 112
Problem # 4.5, 4.6, 4.7, 4.18, 4.19


### P 4.5: The following matrix represents a generator matrix for a (7,4) block code.

| 1 | 0 | 0 | 0 | 1 | 1 | 0 |
|---|---|---|---|---|---|---|
| 0 | 1 | 0 | 0 | 0 | 1 | 1 |
| 0 | 0 | 1 | 0 | 1 | 1 | 1 |
| 0 | 0 | 0 | 1 | 1 | 0 | 1 |


What is the corresponding check matrix?

This matrix is made of a 4x4 information segment then the 3x4 parity portion.

P, the parity section is 

| 1 | 1 | 0 |
|---|---|---|
| 0 | 1 | 1 |
| 1 | 1 | 1 |
| 1 | 0 | 1 |

The transposition of P, P^T is:

| 1 | 0 | 1 | 1 |
|---|---|---|---|
| 1 | 1 | 1 | 0 |
| 0 | 1 | 1 | 1 |

In order to get the parity check, we need to add a 3x3 identity patrix to P^T

| 1 | 0 | 0 |
|---|---|---|
| 0 | 1 | 0 |
| 0 | 0 | 1 |

P^T + 3x3 identity matrix

| 1 | 1 | 0 | 1 | 0 | 1 | 0 |
|---|---|---|---|---|---|---|
| 1 | 0 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 1 | 1 | 1 |


### P 4.6 Find the linear block code generator matrix **G**, if the code generator polynomial is g(x) = 1 + x^2 + x^3 for a (7,4) code.

g(x) = 1 + (0*X) + (1 * X^2) + (1 * X^3) = 

| 1 | 0 | 1 | 1 |
|---|---|---|---|

We need to use the polynomial in the first line of the generator matrix, then right shifting by one for each subsequent row
row 1 : 1,0,1,1,0,0,0

| 1 | 0 | 1 | 1 | 0 | 0 | 0 |
|---|---|---|---|---|---|---|
| 0 | 1 | 0 | 1 | 1 | 0 | 0 |
| 0 | 0 | 1 | 0 | 1 | 1 | 0 |
| 0 | 0 | 0 | 1 | 0 | 1 | 1 |
>



### P 4.7 Repeat p4.6 if g(x) = 1+x^3 for a (7,4) code

g(x) = 1 = x^3 => 1, 0, 0, 1

| 1 | 0 | 0 | 1 | 0 | 0 | 0 |
|---|---|---|---|---|---|---|
| 0 | 1 | 0 | 0 | 1 | 0 | 0 |
| 0 | 0 | 1 | 0 | 0 | 1 | 0 |
| 0 | 0 | 0 | 1 | 0 | 0 | 1 |


### P 4.18 Polynomial 1+x^7 can be factored into 3 irreducible polynomials (1+x)(1+x+x^3)(1+x^2+x^3) with (1+x^2+x^3) and (1+x+x^3) as primitive polynomials. Using 1 + x + x^3 as generator polynomial, calculate the (7,4) cyclic code word for given message sequence 1010

g(x) = 1 + x + x^3

message sequence = 1010, m(x) = 1x^3 + x

The generator matrix is: 

| 1 | 1 | 0 | 1 | 0 | 0 | 0 |
|---|---|---|---|---|---|---|
| 0 | 1 | 1 | 0 | 1 | 0 | 0 |   
| 0 | 0 | 1 | 1 | 0 | 1 | 0 |
| 0 | 0 | 0 | 1 | 1 | 0 | 1 |

We need to multiply the message by the generator matrix

G * 1010

The product of the above is 
| 1 | 1 | 1 | 0 | 0 | 1 | 0 |
|---|---|---|---|---|---|---|

This is the codeword for 1010 using the given polynomial

### P.4.19 Repeat 4.18 with 1 + x^2 + x^3 as g(x)

1 0 1 1

| 1 | 0 | 1 | 1 | 0 | 0 | 0 |
|---|---|---|---|---|---|---|
| 0 | 1 | 0 | 1 | 1 | 0 | 0 |   
| 0 | 0 | 1 | 0 | 1 | 1 | 0 |
| 0 | 0 | 0 | 1 | 0 | 1 | 1 |

Multiply by 1010

Product = 
| 1 | 0 | 0 | 1 | 1 | 1 | 0 |
|---|---|---|---|---|---|---|

1001110 is the result of the product of 1011. Compared to the previous answer, 1110010, we can see that with a different generator polynomial, we will get a different code word for the same message. This is expected as it goes through a different matrix to be multiplied across.