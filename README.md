#Prog Lang HW2

Elijah Abney and Daniel Gay

##General:
Our program uses salsa to implement this actor simulation.
Our program *DOES GET CORRECT OUTPUT:*
  -Please see below, the second part of the Distributed section.

Our program takes advantage of the actor model. Our supervisor class,
  Run.salsa, simply initializes all actors (Dude.salsa), and calls
  the first Dude's consider(), which starts the first campaign selection.
  From there, our actors only communicate with eachother, no longer requiring
  communication with the supervisor. In this way, our solution utilizes the
  actor model fully.


##Concurrent:
Our concurrent fully works. It terminates and gives the
desired output.


##Distributed:
Our distributed program also gives the correct and desired output.
However, there are a few caveats:
  -Our program hangs upon completion. This is because "implements ActorService",
    which disables garbage collection, is expected to cause the program to hang.
    This is expected and desired output for this approach.
  -Our program still gives NullPointerException on our machines, despite disabling
    garbage collection. This seems unusual, but we still get the correct output,
    despite this, so please keep that in mind.
