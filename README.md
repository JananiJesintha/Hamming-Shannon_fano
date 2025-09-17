# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:

colab

# Program:
```
# Huffman coding

import math

# Probabilities given
p = [0.4, 0.19, 0.16, 0.15, 0.15]

# Corresponding Huffman/Shannon-Fano code lengths
lk = [1, 3, 3, 3, 3]

n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")

# Shannon_fano

import math

# Probabilities given
p = [0.4, 0.19, 0.16, 0.15, 0.15]

# Corresponding Huffman/Shannon-Fano code lengths
lk = [1, 3, 3, 3, 3]

n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency & Redundancy
eff = round(hs / L, 3)
red = round(1 - eff, 3)

# Variance of codeword length
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}") 
```
# Calculation:
```
Compare the manually calculated value and the observed practical value.
```
# Output:

Huffman:
Average Codeword Length is : 2.35
Entropy is : 2.228
Efficiency is : 94.8%
Redundancy is : 0.052
Variance is : 1.004

Shannon_fano:
Average Codeword Length is : 2.35
Entropy is : 2.228
Efficiency is : 94.8%
Redundancy is : 0.052
Variance is : 1.004

# Results:
Thus, the Huffman and Shannon-fano code is written and executed successfully.
