---
summary: Introduction to sentences, arguments, and types of args
tags:
  - coursenote
---
# Main Idea
## Sentences
are the basic structure and object of analysis in Logic 1.
This is different from a sentence of normal language.

Sentences ==in our class== are statements that must have a truth-value.
This means that it is objectively *true* or *false*.

## Examples
```
X Open the door.
O It is snowing today.
O John's car is red.
X Stop doing that.
X Spinach is delicious.
```

Sentences have ==3 different levels of classification== which each come after one another:
1. Argument
2. Deductively Valid Argument
3. Deductively Sound Argument

---
## Arguments
An argument is a set of multiple sentences.
One is the ==conclusion== and the others are ==premises==.

```
Chris is either alive or dead.
Chris is not alive.
------------------- (Therefore)
Chris is dead.
```

This is an example of an argument in ==Standard Form==.
The premises assert the conclusion. They go above the line.
The conclusion is under the line.


```
All cats are mammals.
All mammals are animals.
------------------------ (Therefore)
All cats are animals.
```

==Not all arguments have to be "good" or "relevant"==.

```
Snow is white.
-------------- (Therefore)
Snow is white.
```
By definition, this is still considered an argument.

```
Trees have leaves.
------------------ (Therefore)
Fish have gills.
```
This is also an argument by definition.

---
## Deductive Validity
Arguments are deductively valid ==only== if the conclusion ==MUST== be true if all of the premises are true.
In other words, when the conclusion is false, at least one premise must also be false.

Arguments are ==deductively invalid== if they are not deductively valid.

So, to be valid, an argument doesn't have to:
- have premises with anything to do with the conclusion
- have actually, practically, true premises

```
1 + 1 = 2
3 + 6 = -15
------------
0 = 8
```
This is a valid argument because 3 + 6 will never equal -15. There is no way you could conceptually imagine a world in which 3 + 6 equals -15. There is ==no set of coincidences== that could occur to cause 3 + 6 to equal -15. Therefore, 3 + 6 = -15 is a ==false statement==, and this argument is valid, even if the conclusion is ==always false==.

---
## Deductive Soundness
A sound argument is one that is deductively valid and that has true premises in the real world.

Arguments are deductively unsound only if they are not deductively sound.

```
Steve is younger than Carl
Carl is the same age as Janice
------------------------------
Steve is younger than Janice
```
O Argument
O Valid
? Sound (Only if the premises are true)

```
Berlin is in Germany
Germany is in Europe
--------------------
Berlin is in Europe
```
O Argument
O Valid
O Sound (we KNOW the premises are true)