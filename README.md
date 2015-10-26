#Introduction to Programming

##Practical 2

###Instructions

BlueJ is available on the CIS machines in the laboratories and you can also install it on your own machines by downloading it from 

<http://www.bluej.org>.

You will also need to complete Practical 1 first, you will use those files in this practical.

###Level 1: Adding More Interaction
So far, the operations we have seen have involved numerical values. We can
instead use existing variables

```
int x = 4;
int y = 5;
int z = x + y;
```

Continuing on from the exercises you did last time:

1. In the _Picture_ project, you drew your own picture of a house, possibly
including a sunset that moved the sun across the sky. Here we would like you
to move the steps for performing the sunset (or add some) into a separate
method in the _Picture_ class that can be called when required, and another for
sunrise. This way you can control the passing of the days.
__Hint:__ To get the sun to move more slowly, you can use the
`slowMoveHorizontal(int distance)` and
`slowMoveVertical(int distance)` methods.
Try adding a tree with some fruit on it, and a method that drops the fruit to the
ground.
2. Using the _Turtle_ project, add methods to draw pentagons and hexagons inside the
_PictureMaker_ class, with a parameter specifying the length of sides. 
Try changing the colour of the pen doing the drawing. You can add a set of
methods to the _PictureMaker_ class to choose a colour, or a single method that
takes a _Color_ object as a parameter. A selection of possible colours are
listed in the _Color_ class
__Hint:__ Java was produced by an American company, so American spellings
such as “color” are used, e.g. for a turtle called fred, the code to change
colour would be: `fred.setColor(Color.blue);`

3. In the Lab-Classes Project, add a method to _LabClass_, based on the
`printList` method, that prints out the credits for each student.
__Hint:__ The `printList` method shows how to access all the students in the
list of enrolled students.
When a student enrols into the lab-class, they are given a set number of
credits to start with, and have some existing credits from previous courses.
These should be entered when the student enrols, so extend the
`enrollStudent` method to add these credits.
Over the course of the lab-classes, students can gain and lose credits. Try
adding in a way of handling this.

###Level 2: Calling our own Methods

To call a method that is within the same class definition, all we need to do is use the method name and any parameters. For example, in the
_PictureMaker_ class in the Turtle Project, if we wanted to call the
`drawInitials` method from the display method, all we have to add
inside the `{ }` for the display method, is a line with the instruction:
`drawInitials();`

1. In the _Picture project_, the tree grows fruit very rapidly, so when the sun
sets, the fruit falls off the tree, and when it rises, the fruit re-grows. Add
lines to your sunrise and sunset methods, to call the methods making the
fruit drop off the tree and re- grow.
Add a method that moves the whole picture around by a specified amount.
With multiple instances of the picture class, you can then lay out a street of
houses.
__Extra:__ Add a method for drawing the house that takes two numbers as
parameters to give the dimensions of the picture. Make sure your house
fits inside these dimensions, you may want to move the objects around a
bit as you resize the different parts.

2. In the Turtle project, add another method to the
_PictureMaker_ class, based on the `drawInitials`
method, that calls the methods for drawing 
polygons with different numbers of sides. In between drawing the polygons,
change the colour of the pen using the method(s) you defined earlier, so each
polygon is a different colour.

3. In the Lab-Classes Project, we want to know how well the class is doing
over all, as well as what the average mark of all the students enrolled is. To
find this out, add a method to calculate the average score for the students
enrolled in the class, and print out the result.
__Hint:__ Create a variable before you start looping through the list of students,
and add the credits to this variable as you go through the list. This can then
be averaged and printed out when you have finished.

###Level 3: Further Modelling

At this point, we would like you to have a go at starting to model a slightly
more complicated program based on The Botanic Gardens scenario.
Some suggested steps and aspects to consider are described below.

The University Botanic Gardens need a computer system for maintaining
information on stocks of flower seeds and plantings. They will use the system
to determine such things as when to order new stocks, when to sow seeds, in
which beds seeds have been sown, and when they are expected to bloom.

####Step 1: Modelling Types of Flower

The system must maintain information on all the species of flowering plant in
the gardens. The data for a species consists of its name, its genus and its
family, the best month for sowing seeds, and an estimate of the time it takes
from sowing to bloom. Assuming that a species data type is required, propose
a name for the class, propose suitable fields, propose methods for reporting
their values (give the method signatures and brief notes on behaviour).

####Step 2: Modelling Flower Beds

Information needs to be stored on flower beds. A bed has a size, usually
expressed in square metres and an alphanumeric identity such as "bed15".
Often a bed is not used in its entirety so the actual area in use has to be
recorded. When seeds or seedlings have been planted this figure must be
updated. Assuming that a flower bed data type is required:

1. propose a name for the class,
2. propose suitable fields,
3. propose likely methods for manipulating the data (in each case give the
signature and note the behaviour).

####Step 3: Stock Records
The system must keep track of the quantities of seeds in stock. Each stock
record consists of the quantity, the species, and a best before date. Records
are updated when seeds are sown. Your challenge is as with the earlier
exercises. A point to note for this one is that, you can assume the existence of
other data types to make the task easier.

####Step 4: Planting Records
A planting record is used to keep track of what seeds have been planted
where and when. In more detail, a planting occurs in a particular bed and it
comprises a certain quantity of a particular species of flowering plant. The
date of planting is required so the date for the first blooms can be estimated.
See what you can figure for fields and methods. This exercise definitely draws
on the data types from the earlier exercises.