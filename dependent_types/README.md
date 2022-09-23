# Dependent Types Tutorials

These are only beginner level references (I put here what I find useful).

## Background Readings

+ **Constructive Mathematics and Computer Programming** explains very well the rationale for dependent types, and is super super readable - it is awesome when reading stuff firsthand is feasible :)

+ **An introduction to Generalized Type Systems** has 'tutorial' vibes and makes notation very clear. It presents hte lambda cube (extensions of the simply typed lambda calculus with functions from types to types, types to values and values to types).

+ **Dependent Types at Work** shows how to formalize simple properties of some common algebraic datatypes in Agda. Software Foundations is (in my opinion) better in terms of amount / type of exercises, but this article is still useful. To me the best part is that it spells out in detail the inference rules for logic connectives as Agda types, and explains concisely and from first principles the propositions-as-types interpretation. I don't think any of the other references does that so well.

+ **An Introduction to the Calculus of Inductive Constructions** is not very orderly, but it describes very precisely the 'core nature' of inductive proofs, and each paragraph contains lots of examples wwhich make you feel 'oh, right - I get this now'. Having the natural numbers as the first example was very helpful to me.

## Notes / What I got so fat

* The calculus of inductive constructions adds datatypes to CoC (the one from Berandregt's paper), and has one separate sort (Prop) for the types of formulae.

* When writing an inductive definition of a relation, what one does is 'build the whole set', in such a way that, if for each constructor I provide a map for elements of that constructor to some other type, exhaustively, I can always go from terms of the former type to the later. If that later type happens to be some Prop, then that's effectively a procedure converting terms of a given type to statements about those terms. 

* A proof object is a term of the proposition one wants.

* 'Exists' is simply `Exists A (phi : A -> Prop) := some : Forall x. (P x) -> Exists A P` (clever). That is, an inductive datatype (belonging to Prop) whose only constrctor takes whatever function P from A (every / any A) to Prop you have (you *have* to have one first, that's why you know it exists), and there, I can give you a function from P x to Exists A P. Now, this means that, to have your 'Exists A P', you'll have to give me some a : A, so once we have that a, we'll take (P a) and use it to compute exists (P a), which will be of type (Exists A P).


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
