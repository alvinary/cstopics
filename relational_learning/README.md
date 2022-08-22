# Relational Learning

## Inductive Logic Programming and Statistical Relational Learning

Authors in the statistical relational learning community are interested
in obtaining ML models for relational data: if you can drop in
an SQL table holding data on social network users and their
content and predict 'social unrest' some months in advance, or
reliably discriminate between some classes of users, you can declare
yourself happy.

Their main concern is statisticial inference and their 'complexity boom'
comes from large graphical models, or not-so-tractable cases of maximum
likelihood estimation and the like.

Authors in the symbolic relational learning community come from the 'Logic
gang' (not so much the 'mainstream ML gang'). They are concerned with different
kinds of problems (learning sets of prolog-style rules that describe
some class of objects, and program synthesis). Their 'special case' of
relational learning is inductive logic programming (instead of saying
'it is a swan, therefore it is white', you want to say 'this is a swan
and it is white... this other swan is white too... ok, all swans are
white'). Less informally, if you have a set of positive and negative
examples described as relational data, you want to obtain a logical
theory of which all positive observations are examples, and no negative
examples are (your theory characterizes all the examples in the target
category).

There are, of course, hybrid approaches, mostly from 2016 on.

Some people have tried applying Deep Learning as a black-box magic
oracle guiding search - everything works as if you had relational data,
no graph/relation embeddings anywhere in your data, reasoning, and so on,
but there is a deep learning model trying to get search where it should
be using the usual tools.

There's also stuff like delta prolog (I think that was the name), which
is differentiable logic programming.

I grouped these two approaches because there is some degree of integration between
the two communities, and some authors are "both" (Pedro Domingos, Cohen, DeRaedt,
and a couple more).

### Main Issues with Symbolic Relational Learning (the insurmountable hurdles)

+ Brittleness (you can use fuzzy, many-valued, soft, etc. truth values to overcome this)
+ Intractability (most ILP setups are way above NP. Exponential is commonplace)

### Main 'Contingent' Issues 

+ Ecosystem (not a lot of software, not very usable)

### Secondary Issues (the stuff people can work on)

+  Predicate invention ('What if my data is missing a useful relation? Can I discover it by composing the ones I have?')
+  External atoms ('Can I fruitfully mix my ASP / logic engine with some imperative code? Mostly to compute some functions that
   respect a relational specification but could take prolog / clingo / etc a load of resources just to get sth that would
   be very easy to compute if I threw in some python/lua code...')
+  Implicit computation ('Can I lazily unfold my problem instance, instead of filling 32GB ram with cnf clauses?')
+  Reducing the search space with some ad-hoc trick

## Knowledge Representation

Until very recently their beef was exclusively with semantic web technologies,
sensor data, industrially labeled data and ontology/terminology induction, but
these few last years they have been getting some vectors into their datasets and
testing their approach with more 'vanilla' classification tasks in mind.
