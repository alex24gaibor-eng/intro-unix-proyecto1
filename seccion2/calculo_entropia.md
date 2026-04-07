Section 2: Manual Entropy Calculations

This document explains how to calculate the entropy of a password using the formula proposed by Claude Shannon:

H=L×log2(N)


This formula allows us to estimate how secure a password is depending on its length and the number of possible characters it can contain.

Example 1: Numeric PIN

Alphabet (N): 10 (numbers from 0 to 9).

Length (L): 8 characters.

Calculation:

H=8×log2(10)≈8×3.3219=26.57bits

This result shows that a PIN, even with several digits, offers limited security due to the small variety of characters.

Example 2: Password of only lowercase letters

Alphabet (N): 26 (letters from 'a' to 'z').

Length (L): 14 characters.

Calculation:

H=14×log2(26)≈14×4,700=65.80bits

In this case, the password is more secure than the PIN, since the number of possible combinations increases.

Example 3: Strong Password (Generated in KeePassXC)

Alphabet (N): 94 (uppercase letters, lowercase letters, numbers, and symbols).

Length (L): 16 characters.

Calculation:

H=16×log2(94)≈16×6.5545=104.87 bits

This type of password has a very high entropy, which makes it much more secure and difficult to crack.
