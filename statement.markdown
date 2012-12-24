% Statement of Research
% Arash Rouhani
%

This document is written by Arash Rouhani, a CS student at Georgia Tech with
the intention of pursuing a research project in the Golems Humanoid Robotics
Lab.

# Project goals

The student shall be working in the *Motion Grammar* group at the Golems lab.
One of the main goals is for the student to work on arbitrary tasks of the
Motion Grammar project, initially most of the work should be done closely with
the other members of the Motion Grammar project. This will ensure a reasonable
learning curve in the first spans of the project. The student will learn
what day to day work on the Motion Grammar involves and get confidence to
work more independently as will be required in the project's later stages.

In order for the student to eventually be able to implement his results on an actual
robot, the student will be part of the initial setup of the `LWA4` robot that
arrived very recently to the Golems lab. The goal here is for the student to
gain confidence with that robot platform.

In addition to fulfilling the aforementioned learning related goals, the
student should also be pursuing some theoretical research related to parsers.

## Theoretical problem statement

One of the components in the motion grammar is the parser. Most computer
scientists will know that grammars and parsers are a quite well studied
topic and that they are used for everyday tasks for the computer
programmer in the form of interpreting and compiling source code. But the
application of parsers in the Motion Grammar project differ in one essential
aspect, the parser is run live on a time-based physical system. There is a
formal definition for the Motion Grammar (in sense of it being a grammar, not a
project title) and we'll call a parser recognizing a Motion Grammar language a
*Motion Parser*.

An Motion Parser is of practical use because it can be used as an observation
to action converter. Currently the Motion Grammar Toolkit
generates a LL(1) parser.  If we could find a way to create more powerful
parsers, say something corresponding to the power of LALR, more robot programs
could be built and have the same guarantees as the current Motion Parser
provides.

# Solution Proposal to Improving LL(1)

A linguistic analysis is done in the paper *The Motion Grammar -- Linguistic
Perception, Planning, and Control*. The paper includes a couple of interesting
future work ideas. One is to further explore what's possible beyond LL(1) given
the situation of parsing in the Motion Grammar.

Theoretically we know that any Motion Parser can't be better than a class
called *semantically LL(1)*, meaning that the parser is allowed more than one
look ahead granted that it will not back track. Intuitively this corresponds to
that in the real world a robot can't undo a physical action. One idea of
improving over regular LL(1) is to try to take advantage of that you may look
ahead further, as long as all the rules you're considering have the same
semantic action associated with it. That is, either construct a semantically
LL(1) parser or something in between that and regular LL(1).

# Schedule of Work

The project span is the spring 2013 semester. Check up meetings will be held
weekly during the semester to ensure steady progress. The student should
ideally have a spread out usage of his 150-180 minimum working hours and will
work more than that if so is required. This project is worth 3 credits.

# Deliverables

* Implementation of a parser generator that is more powerful than the current
  LL(1) algorithm.
* Demonstrate the new parser running on the actual `LWA4` robot platform,
  parsing a grammar not possible before.
* An article for publication.

[Motion Grammar Project]: http://www.golems.org/node/1224
