Jacob Hebert

CSCI 4957/5957 – Wireless & Mobile Networks
HW # 3- Fall 2024
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Instruction: Write clearly and give full justification to your answers. Show all your working and claims with clear abstraction or citation. Homework is due on 09/24/2024 in class. Late work will not be accepted.  Max points 20
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Page # 110 - 112
Problem # 4.5, 4.6, 4.7, 4.18, 4.19


P 4.5: The following matrix represents a generator matrix for a (7,4) block code.

| 1 | 0 | 0 | 0 | 1 | 1 | 0 |
| 0 | 1 | 0 | 0 | 0 | 1 | 1 |
| 0 | 0 | 1 | 0 | 1 | 1 | 1 |
| 0 | 0 | 0 | 1 | 1 | 0 | 1 |


What is the corresponding check matrix?

This matrix is made of a 4x4 information segment then the 3x4 parity portion.

P, the parity section is 

| 1 | 1 | 0 |
| 0 | 1 | 1 |
| 1 | 1 | 1 |
| 1 | 0 | 1 |

The transposition of P, P^T is:

| 1 | 0 | 1 | 1 |
| 1 | 1 | 1 | 0 |
| 0 | 1 | 1 | 1 |

In order to get the parity check, we need to add a 3x3 identity patrix to P^T

| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 0 | 0 | 1 |

P^T + 3x3 identity matrix

| 1 | 1 | 0 | 1 | 0 | 1 | 0 |
| 1 | 0 | 1 | 1 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 | 1 | 1 | 1 |
