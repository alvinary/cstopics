# Relational Learning

# Symbolic and Statistical Relational Learning

These articles exemplify symbolic approaches to relational learning, mostly.

Authors in the statistical relational learning community are interested
in obtaining ML models for relational data: if you can drop in
an SQL table holding data for a network of social network users with
their posts and predict 'social unrest' some months in advance, or
reliably discriminate between some classes of users, you can declare
yourself happy.

Their main concern is statisticial inference and their 'complexity boom'
comes from large graphical models, or not-so-tractable cases of maximum
likelihood estimation and the like.

Authors in the symbolic relational learning community come from the 'Logic
gang' (not so much the 'mainstream ML gang').

There are, of course, hybrid approaches, mostly from 2016 on.

Some people have tried applying Deep Learning as a black-box magic
oracle guiding search - everything works as if you had relational data,
no graph/relation embeddings anywhere in your data, reasoning, and so on,
but there is a deep learning model trying to get search where it should
be using the usual tools.

There's also stuff like delta prolog (I think that was the name), which
is differentiable logic programming.

# Main Issues (the insurmountable hurdles)

+ Brittleness (you can use fuzzy, many-valued, soft, etc. truth values to overcome this)
+ Intractability (most ILP setups are way above NP. Exponential is commonplace)

# Main 'Contingent' Issues 

+ Ecosystem (not a lot of software, not very usable)

# Secondary Issues (the stuff people can work on)

+  Predicate invention ('What if my data is missing a useful relation? Can I discover it by composing the ones I have?')
+  External atoms ('Can I fruitfully mix my ASP / logic engine with some imperative code? Mostly to compute some functions that
   respect a relational specification but could take prolog / clingo / etc a load of resources just to get sth that would
   be very easy to compute if I threw in some python/lua code...')
+  Implicit computation ('Can I lazily unfold my problem instance, instead of filling 32GB ram with cnf clauses?')
