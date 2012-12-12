% Statement of Research
% Arash Rouhani
%

This document is written by Arash Rouhani, a CS student at georgia tech with
the intention of pursuing a research project in the Golems Humanoid Robotics
Lab. The advisor will be professor **Mike Stilman**. Since the student will be
working with the [Motion Grammar Project] which is mainly developed by Ph.D.
candidate **Neil Dantam**, so most of the off schedule interactions will
probably be between the student and Neil.

# Problem Statement

Here's the overview description of the motion grammar, quoted from the project
web site.

> The Motion Grammar is a powerful new representation for task decomposition,
> perception, planning, and hybrid control that provides a computationally
> tractable way to control robots in uncertain environments with guarantees on
> correctness and completeness. The grammar represents a policy for the task
> which is parsed in real-time based on perceptual input. [...]

One of the components in the motion grammar is the parser. Most computer
scientists will know that the grammars and parsers are a quite well studied
topic and that they are used for the day to day tasks for the computer
programmer in the form of interpreting and compiling source code. But the
application of parsers in the Motion Grammar project differ in one essential
aspect, the parser is run live on a time-based physical system. There is a
formal definition for the Motion Grammar (in sense of it being a grammar, not a
project title) and we'll call a parser recognizing a Motion Grammar language a
*Motion Parser*.

An Motion Parser is of practical use because it can be used as an observation
to action converter (basically a brain). However the project will not concern
that part, instead it will be about the power of the Motion Parsers we can
generate today. Currently the Motion Grammar Toolkit generates a LL(1) parser.
If we could find a way to create more powerful parsers, say something
corresponding to the power of LALR, more robot programs could be built and
still have the same guarantees as the current Motion Parser provides.

# Solution Proposal

A linguistic analysis is done in the paper *The Motion Grammar -- Linguistic
Perception, Planning, and Control*. The paper includes a couple of interesting
feature work ideas. One is to further explore what's possible beyond LL(1)
given the situation of parsing in the Motion Grammar.

Theoretically we know that any Motion Parser can't be better than a class
called *semantically LL(1)*, meaning that you're allowed more than one look
ahead granted that you know you're not gonna back track, since in reality you
can't "undo" a physical action. One idea of improving over regular LL(1) is to
try to take advantage of that you may look ahead further, as long as all the
rules you're considering have the same semantic action associated with it. That
is, either construct a semantically LL(1) parser or something inbetween that
and regular LL(1).

# Schedule of Work

The project span is the spring 2013 semester. Check up meetings will be held
weekly during the semester to ensure steady progress. The student should
ideally have a spread out usage of his 150-180 minimum working hours and will
work more than that if so is required. This project is worth 3 credits.

# Deliverables

* An article for publication created jointly with Neil Dantam and Mike Stilman.
* Implementation of a parser generator that is more powerful than the current
  LL(1) algorithm.

[Motion Grammar Project]: http://www.golems.org/node/1224
