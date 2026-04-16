# MobileKey Cipher

A simple encoding stuff I came up with while bored in Roblox Studio and Discord

## What is it?
MobileKey Cipher is a substitution cipher inspired by the symbol layer 
of a mobile keyboard, where each letter maps to the symbol or number 
you'd find on a phone's keyboard.

Think of it like leet speak, but instead of random substitutions, 
every mapping follows the logic of what's physically on your mobile keyboard.

- It converts this:
<img width="706" height="428" alt="image" src="https://github.com/user-attachments/assets/51190b2b-8e7e-4ae0-8176-c244f0dcf9d4" />

- into this:
<img width="706" height="508" alt="image" src="https://github.com/user-attachments/assets/e2598d2c-7987-4628-bad4-8cf7a0456b03" />

- im not sure if this is the correct type of image to be showing but yeah, kindof like it.

## Note
The mapping table is based on the symbol layer of a standard 
QWERTY mobile keyboard. Or morely my keyboard lmao
Different phones or keyboard apps may organize symbols differently.

Punctuations are currently encoded into random symbols i came up with, so you can fuck around with it or keep it in for fun :)

# Mapping Table
| Letter | Encoded |
|--------|---------|
| q | 1 |
| w | 2 |
| e | 3 |
| r | 4 |
| t | 5 |
| y | 6 |
| u | 7 |
| i | 8 |
| o | 0 |
| p | / |
| a | @ |
| s | # |
| d | $ |
| f | _ |
| g | & |
| h | - |
| j | + |
| k | ( |
| l | ) |
| z | * |
| x | " |
| c | ' |
| v | : |
| b | ; |
| n | ! |
| m | ? |

## Punctuations (my version)
| Symbol | Encoded |
|--------|---------|
|  | ~ |
| , | > |
| ! | < |
| ' | ^ |
| = | = |

## Example
Encoding `"Hello, World!"`:
H → -
e → 3
l → )
l → )
o → 0
, → >
→ ~
W → 2
o → 0
r → 4
l → )
d → $
! →
Result: -3))0>~204)$

## Usage (LuaU)
Encoding:
MobileKey:encode("Hello, World!")  --> -3))0>~204)$

Decoding:
MobileKey:decode("-3))0>~204)$<")  --> hello, world!

## Limitations
- Decoding restores text in **lowercase** since the cipher is case-insensitive
- Characters not in the mapping table pass through unchanged
- Not cryptographically secure, I use this for Lore, Character stuffs, and ARG's (most reccomended as this is an unknown type of Ciphering)

## License
MIT, do whatever you want with it! Even add your own symbols!
