# 回到12歲

| Info | Value |
| :--- | :-----: |
| Categories | #★★☆☆☆ #MISC |
| Score | 200 |
| Total Solve (Rate) | 86/240 (35.8%) |

## Description

If you can beat me in the game I'll give you the flag!

https://scratch.mit.edu/projects/596813541/

## School Solves
| Overall Order | School Order | Name | Solved at |
| :-: | :-: | :-: | :-: |
| 54 | 1 |  S0092 - Immaculate Heart of Mary College | 2021-11-13 23:46:48.728 |
| - | - |  S0090 - Immaculate Heart of Mary College | Unsolved |
| - | - | S0091 - Immaculate Heart of Mary College | Unsolved |
| - | - | S0096 - Immaculate Heart of Mary College | Unsolved |

Total: 1/4 (25%)

## Writeup
First off, open the scratch project. Upon checking the code, we know we need to win it in order to solve the challenge. We forced our way through to win the game by adding the block
```
set globalCurrentPlayer to X
```
and spamming it manually to win. Then we got a prompt that checks our flag. By checking the codes again, and removing the sticky note that hiding the code in Title object, we know that our input will be shifted by this line o f code:
```
set result to join result item item # of letter i of item 10 of globalGameState in chars + 18 mod length of chars + 1 of chars
```
Then we entered alphabets to try how many characters it shifted and logged it in a [spreadsheet](https://docs.google.com/spreadsheets/d/1fkpd4ReVCNndQRLFGAph-XBYUIU9Gf4RlK83OJX4ZTE/edit). As I am lazy, I used `VLOOKUP`, `SPLIT` and `CONCATENATE` function to reduce a little time, which returns me the flag.

## Flag
`hkcert21{hello_caesar_cipher}`