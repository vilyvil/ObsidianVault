---
summary: Explanation of connectives, which connect atomic sentences to each other
tags:
  - coursenote
---
^ [[Formal Language (Sentential Logic)]] |

# Connectives
as their name implies, connectives connect atomic sentences together to allow for the creation of complex molecular sentences in sentential logic.
##### Truth-Functionality
- Connectives are considered truth-functional if the ==truth value== of the ==result==ing sentence is ==entirely dependent== on the truth-values ==of the connected sentences==
- ie. Bill is from Toronto and Sarah is from Montreal
		- "and" is truth-functional because the full sentence is only true if Bill is from Toronto AND Sarah is from Montreal

# List of Connectives
| Symbol | Function                        | Explanation                   |
| ------ | ------------------------------- | ----------------------------- |
| &      | [Conjunction](#Conjunction)     | Both \_ and _                 |
| V      | [Disjunction](#Disjunction)     | Either \_ or _ (at least one) |
| ⊃      | [Conditional](#Conditional)     | If \_ then _                  |
| ~      | [Negation](#Negation)           | Not \_                        |
| ≡      | [Biconditional](#Biconditional) | If \_ and only if _ , then    |
## Explanations in More Depth
### Conjunction
```
B = Bill is from Toronto
S = Sarah is from Montreal

B & S
```
The sentences being connected by a conjunction are ==called conjuncts==
- Molecular sentence is only True if ==both B & S are True==
### Disjunction
```
D = Harry is a Doctor
L = Harry is a Lawyer

D V L
```
Sentences being connected by a disjunction are called disjuncts
- Works like ==OR operator== in programming languages
- If at least one is True, then output is True
- If both are False, then output is False
### Conditional
```
W = I work hard
P = I get promoted

W ⊃ P
```
Antecedent ⊃ Consequent
Output of conditional is True ==as long as the condition is not broken==.
ie.
- If antecedent is True, then the consequent MUST be True
- False ⊃ True is still True because the definition of conditional doesn't say "ONLY" if, but just if.
### Negation
```
B = The sky is blue

~B
```
Reverses the input's truth value
### Biconditional
```
W = Our team wins
P = Smith makes this basket

P ≡ W
Our team wins if and ONLY if Smith makes this basket
```
name ≡ name
Output is similar to conjunction
- True when both are True or both are False