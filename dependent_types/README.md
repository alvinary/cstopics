# Dependent Types Tutorials

These are only beginner level references (I put here what I find useful).

## Background Readings

+ **Constructive Mathematics and Computer Programming** explains very well the rationale for dependent types, and is super super readable - it is awesome when reading stuff firsthand is feasible :)

+ **An introduction to Generalized Type Systems** has 'tutorial' vibes and makes notation very clear. It presents hte lambda cube (extensions of the simply typed lambda calculus with functions from types to types, types to values and values to types).

+ **Dependent Types at Work** shows how to formalize simple properties of some common algebraic datatypes in Agda. Software Foundations is (in my opinion) better in terms of amount / type of exercises, but this article is still useful. To me the best part is that it spells out in detail the inference rules for logic connectives as Agda types, and explains concisely and from first principles the propositions-as-types interpretation. I don't think any of the other references does that so well.

## Practical Aspects of Coq

### Small

+ [Basic predicate logic](https://coq.inria.fr/tutorial/1-basic-predicate-calculus) - it's supposed to be outdated, but it worked great for me.
+ [Cornell Tactics Cheatsheet](https://www.cs.cornell.edu/courses/cs3110/2018sp/a5/coq-tactics-cheatsheet.html)
+ Pierce is a very good speaker, and if you need to make a presentation or something on dependent types, [these slides](https://www.seas.upenn.edu/~sweirich/plmw12/Slides/plmw12-Pierce.pdf) use a good strategy you can copy. He introduces types as the most widely applied, automatic and robust formal method, and notes you have a trade-off between automation and expressive power (proof assistants > model checking > static analysis of types). That fits very well with 'Usable tools are used by everyone because you don't need to be an expert'.

### Books

+ [Software Foundations](https://softwarefoundations.cis.upenn.edu/) - The first volume is great to get started quickly and has a very
  pragmatic pacing (each chapter is short and has several exercises. Having a clear correspondence between expected work time and 'syntactic'
  chapter breaks is super useful for me).

## Using typed lambda calculi and related formalisms to represent program behavior

+ Types and Programming Languages (A very good and readable book, which unfortunately is still too much for my current amount of patience)
