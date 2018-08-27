:Author: Justin Perona

Credit for the course layout and some of the content is given to Jason Lowe-Power of UC Davis.
Credit for a significant portion of the content is given jointly to Sean Davis and Matthew Farrens of UC Davis.

Content is licensed under CC BY 4.0.
See the LICENSE file for more information.

.. _Canvas: https://canvas.ucdavis.edu/courses/283740
.. _Github: https://github.com/jlperona-teaching/ecs154a-ssii18
.. _Gradescope: https://gradescope.com/courses/20711
.. _Piazza: https://piazza.com/class/jjmd3q6esw46c
.. _schedule: https://github.com/jlperona-teaching/ecs154a-ssii18/blob/master/syllabus/schedule.csv

================================
ECS 154A - Computer Architecture
================================

Class and People
----------------

Lectures and Discussions
~~~~~~~~~~~~~~~~~~~~~~~~

*Monday, Tuesday, Wednesday*: 14:10 - 15:50, 250 Olson

*Thursday*: 14:10 - 15:50, 118 Olson

Discussions are held in the second half of lectures on Wednesdays.

Instructor
~~~~~~~~~~

**Justin Perona** (jlperona at ucdavis dot edu)

Emails to me about the course should have the tag **[ECS 154A]** (including the brackets) in the title.

*Afternoon Office Hours*: MT 16:30 - 18:00

*Afternoon Office Hours Location*: 3039 Kemper

*Evening Office Hours*: W 19:00 - 20:00

*Evening Office Hours Location*: Old Teahouse (or outside on the patio), University Mall, 825 Russell Boulevard #22

Other office hours by appointment.
Email me to schedule an appointment.

Teaching Assistant
~~~~~~~~~~~~~~~~~~

**Yuan Pan** (yapan at ucdavis dot edu)

*Office Hours*: R 09:30 - 11:30

*Office Hours Location*: 53 Kemper

Description
~~~~~~~~~~~

Introduction to digital design.
Interrupts and interconnection hardware.
Caching and memory hierarchy design.
Hardware support for operating systems software (virtual memory).

Prerequisites
~~~~~~~~~~~~~

(ECS 50) or (EEC 70) or the equivalent.

Websites
--------

Github
~~~~~~

We will use Github_ as the main website for the course.
It will also contain all of the documents for the course, such as labs and homework (and the syllabus you're currently reading).

The versions of documents found on Github are the canonical versions of all documents.
Other downloaded versions of documents may become out of date.
If I make changes to those documents, they will appear first on Github.

Canvas
~~~~~~

We will be using Canvas_ for assignment submission and grade distribution.

Gradescope
~~~~~~~~~~

We will use Gradescope_ for returning quizzes, the midterm, and the final.
Gradescope gives you a graded PDF version of your test, along with a rubric, immediately after we're done grading.
You will receive an email from Gradescope to make your account after we grade the first quiz.

Piazza
~~~~~~

We will use Piazza_ for class discussions outside of the classroom.
Odds are, you've used Piazza for another class, but it will serve as the discussion board.
Both the TA and I will be on Piazza to answer questions.

It's best to ask your questions on Piazza.
That way, all of your classmates can see the answer instead of emailing the TA or me.
Additionally, you may get a faster response from one of your classmates.

Through asking and answering questions on Piazza, you improve your understanding of the material, and improve other students' understanding as well.
As an incentive to answer other students' questions and participate, I will drop your lowest quiz score if you consistently participate on Piazza.
I will check Piazza participation, determine the cutoff, and drop the lowest score at the end of the quarter.

In the spirit of the above, please ask questions as public questions on Piazza, if possible.
This way, your question, and the answer to your question, can help somebody else who might have the same question.
We will change questions asked privately to public, if we deem it appropriate.
If your question involves code you've written, or is about a personal issue, we will leave those private.
The same applies to emailed questions - we will redirect you to Piazza if appropriate.

Other Important Information
---------------------------

Regrade Requests
~~~~~~~~~~~~~~~~

Regrade requests must be made within one week of the return of the assignment or test.

Accommodations
~~~~~~~~~~~~~~

The exam schedule is available on the schedule_.
Per `official UC Davis policy`_, if you have an accommodation request from the `Student Disability Center`_, or have any conflicts with exam times for religious observances, you must notify me by the **fifth class, Monday, 2018-08-13**.

.. _official UC Davis policy: http://academicsenate.ucdavis.edu/bylaws_and_regulations/regulations.cfm?#538-
.. _Student Disability Center: https://sdc.ucdavis.edu/

Academic Misconduct
~~~~~~~~~~~~~~~~~~~

Academic misconduct is a serious issue.
You can find the official UC Davis policy on the `Office of Student Support and Judicial Affairs`_ website.

You are expected to *cite all of the work you reference*.
Any ideas that are not specifically yours or generally known (e.g., caches hold data) should have a citation.
When in doubt, cite.

The labs will be partner assignments.
Feel free to share ideas with other groups.
You may not share code or circuits, however.
If you're looking at another group's code or circuits, odds are that you've gone past simply sharing ideas.

Any violations of this policy will result in reporting the violating student(s) to the Office of Student Support and Judicial Affairs.

.. _`Office of Student Support and Judicial Affairs`: http://sja.ucdavis.edu/

Assignments and Tests
---------------------

Grading Breakdown
~~~~~~~~~~~~~~~~~

============ ===
Labs (5x)    30%

Quizzes (3x) 20%

------------ ---

Midterm      20%

Final        30%
============ ===

Labs
~~~~

You will complete four lab assignments throughout this course.
The labs can found via the links below.
All together, the labs are worth 30% of your final grade, though some labs may be weighted more than others.

Labs are due at 09:00 on the date specified.
The dates below are tentative.

* `Lab 1`_. Due 2018-08-15.
* `Lab 2`_. Due 2018-08-27.
* `Lab 3`_. Due 2018-09-04.
* `Lab 4`_. Due 2018-09-13. (You may not turn this lab in late, its due date is absolute.)

For all labs, you may (and are suggested to) work with a partner.
You do not have to keep the same partner throughout the whole quarter; you can change who you work with.
I suggest using Piazza to find partners.

.. _Lab 1: https://github.com/jlperona-teaching/ecs154a-ssii2018/blob/master/lab1/lab1.rst
.. _Lab 2: https://github.com/jlperona-teaching/ecs154a-ssii2018/blob/master/lab2/lab2.rst
.. _Lab 3: https://github.com/jlperona-teaching/ecs154a-ssii2018/blob/master/lab3/lab3.rst
.. _Lab 4: https://github.com/jlperona-teaching/ecs154a-ssii2018/blob/master/lab4/lab4.rst

Late Assignments
~~~~~~~~~~~~~~~~

If you turn in a lab late, you will lose points.
The percentage of points you will lose is given by the equation below.
This will give you partial points up to 48 hours after the due date.
This system penalizes you less the earlier you turn it in, versus a straight-linear drop-off.

    fraction of points = 1 - (hours late)^2/48^2

This does not apply for Lab 4, since I cannot have an assignment due after the start of the final.
Lab 4's due date is absolute.

Quizzes
~~~~~~~

There will be quizzes on Thursday for some weeks.
Check the schedule_ for the dates.

The quizzes themselves will be in a similar style to the midterm and final, except for their length (25 minutes versus 100 minutes).
However, the quizzes will be open-book and open-note.
No asking your neighbors for help, and no electronic devices.

Midterm: Thursday, 2018-08-24 14:10
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The midterm covers content through 2018-08-21.
It will be 100 minutes long.

No asking your neighbors for help, and no electronic devices.
You are allowed to bring one US letter (8.5" x 11") sheet of *handwritten* notes.
Otherwise, the midterm is closed-book and closed-note.

Final: Thursday, 2018-09-13 14:10
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The final is cumulative.
It will be 100 minutes long.

No asking your neighbors for help, and no electronic devices.
You are allowed to bring one US letter (8.5" x 11") sheet of *handwritten* notes.
Otherwise, the final is closed-book and closed-note.

Reading List and Schedule
-------------------------

Textbook
~~~~~~~~

We will be using the following textbooks:

* *Computer Organization and Architecture* by William Stallings.
* *Digital McLogic Design* by Bryan Mealy and James Mealy.

The Stallings book is the main book that we will be using.
Either the 9th edition or 10th edition is fine.
I will post chapters to read for both editions.

The Mealy and Mealy book serves as the main source for the digital logic content in the course.
The Stallings book contains some, but not all, of the information that I'd like to cover.
You can find a copy of *Digital McLogic Design* on Canvas_.

See the schedule_ for reading dates.

Schedule
~~~~~~~~

See the official schedule_ on Github.
