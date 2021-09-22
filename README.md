This repository will be used as the website for Functional Programming CS-210. It will be updated weekly throughout the semester. This README contains general information about the class.

- [previous-exams](previous-exams) contains PDFs for the previous exams.
- [exercises](exercises) contains markdown documents for the exercise sessions and solutions.
- [slides](slides) contains the slides presented in class (also attached or respective videos).
- [labs](labs) contains markdown documents for the labs.

We will use GitLab's issue tracker as a discussion forum. Feel free to [open an issue](https://gitlab.epfl.ch/lamp/cs210/issues/new) if you have any comments or questions

# First-week Tasks

1. [Join the Discord](https://discord.gg/UqzqX2wTWW).
2. [Log into EPFL's GitLab](https://gitlab.epfl.ch/users/sign_in).
3. Fill in [this table](https://docs.google.com/spreadsheets/d/12KvfD_jN5AcApmWhCz7xZmln48fctQOa984RPWrqRkY/edit#gid=0) with your GASPAR and SCIPER number to initialize your GitLab repository for the course (login with your `@epfl.ch` address to have write access).
4. Choose a group for the exercises (recitation sessions) by answering [this Doodle](https://doodle.com/poll/4k7gkxiv9hdxzivk).
5. Follow the [Tools Setup](labs/tools-setup.md) page.
6. Do the [example lab](labs/example-lab.md).
7. Do the [first graded lab](labs/lab-1.md).

## Grading

The grading of the course is divided between labs (30%), a midterm exam (20%) and a final exam (50%).

## Staff

| Role        | People |
| :---        | :--- |
| Professors  | [Martin Odersky](https://people.epfl.ch/martin.odersky), [Viktor Kunčak](https://people.epfl.ch/viktor.kuncak) |
| TAs         | [Dragana Milovancevic](https://people.epfl.ch/dragana.milovancevic), [Ergys Dona](https://people.epfl.ch/ergys.dona), [Jean-Baptiste Cordonnier](https://people.epfl.ch/jean-baptiste.cordonnier), [Matthieu Bovel](https://people.epfl.ch/matthieu.bovel) |
| Student TAs | [Joshua Bernimoulin](https://people.epfl.ch/joshua.bernimoulin), [Mohamed Yassine Boukhari](https://people.epfl.ch/mohamed.boukhari), [Hind El Bouchrifi ](https://people.epfl.ch/hind.elbouchrifi), [Luca Giordano](https://people.epfl.ch/lucas.giordano), [Mohamed Hichem Hadhri](https://people.epfl.ch/mohamed.hadhri), [Salim Najib](https://people.epfl.ch/salim.najib), [Arthur Vignon](https://people.epfl.ch/arthur.vignon) |

## Lecture Schedule

<!-- date -d "30/09/2019 364 days" +"%d.%m.%Y" -->

Lectures are prerecorded and published below. This class is given in a [_flipped classrom_](https://en.wikipedia.org/wiki/Flipped_classroom) format, meaning that you should watch the videos by yourself _before_ the indicated date. You will then have the occasion to test and perfect your knowledge during the [exercises (recitation sessions)](#user-content-exercise-recitation-session-schedule) on Wednesday afternoons, and [labs](#user-content-lab-schedule) on Friday mornings.

**Note**: In some lectures, worksheets are used to present code. To learn how to
use worksheets yourselves, please follow the [Tools
Setup](labs/tools-setup.md) and [example lab](labs/example-lab.md). To create a
new empty project to experiment with worksheets, you can clone the following
repository and run `code . ` inside as usual: [`git clone https://gitlab.epfl.ch/lamp/cs210-worksheets`](https://gitlab.epfl.ch/lamp/cs210-worksheets)

| Week | Date        | Topic                                       | Videos & Slides              |
| :--  | :--         | :--                                         | :--                |
| 1    | 22.09.2021  | Intro class                                 | Introduction ([Video][Video 1.1.1], [Slides][Slides 1.1.1])<br/>Elements of programming ([Video][Video 1.1.2], [Slides][Slides 1.1.2])<br/>Evaluation strategies and termination ([Video][Video 1.1.3], [Slides][Slides 1.1.3])<br/>Value Definitions and Conditionals ([Video][Video 1.1.4], [Slides][Slides 1.1.4])<br/>Square Roots with Newtons Methods ([Video][Video 1.1.5], [Slides][Slides 1.1.5])<br/>Blocks and lexical scopes ([Video][Video 1.1.6], [Slides][Slides 1.1.6])<br/>Tail Recursion ([Video][Video 1.1.7], [Slides][Slides 1.1.7]) |
| 2    | 29.09.2021  | Recursion / Function values | Higher-Order Functions ([Video][Video 1.2.1], [Slides][Slides 1.2.1])<br/>Currying ([Video][Video 1.2.2], [Slides][Slides 1.2.2])<br/>Finding FixedPoints ([Video][Video 1.2.3], [Slides][Slides 1.2.3])<br/>Scala Syntax Summary ([Video][Video 1.2.4], [Slides][Slides 1.2.4])<br/>Functions and Data ([Video][Video 1.2.5], [Slides][Slides 1.2.5])<br/>Data Abstraction ([Video][Video 1.2.6], [Slides][Slides 1.2.6])<br/>Evaluation and Operators ([Video][Video 1.2.7], [Slides][Slides 1.2.7]) |
| 3    | 06.09.2021  | Classes                                     | Class Hierarchies ([Video][Video 1.3.1], [Slides][Slides 1.3.1])<br/>How Classes are Organized ([Video][Video 1.3.2], [Slides][Slides 1.3.2])<br/>Polymorphism ([Video][Video 1.3.3], [Slides][Slides 1.3.3])<br/>Objects Everywhere ([Video][Video 1.3.4], [Slides][Slides 1.3.4])<br/>Functions as Objects ([Video][Video 1.3.5], [Slides][Slides 1.3.5]) |
| 4    | 13.10.2021  | Classes                                     | Decomposition ([Video][Video 1.4.1], [Slides][Slides 1.4.1])<br/>Pattern Matching ([Video][Video 1.4.2], [Slides][Slides 1.4.2])<br/>Lists ([Video][Video 1.4.3], [Slides][Slides 1.4.3])<br/>Enums ([Video][Video 1.4.4], [Slides][Slides 1.4.4])<br/>Subtyping and Generics ([Video][Video 1.4.5], [Slides][Slides 1.4.5])<br/>Variance ([Video][Video 1.4.6], [Slides][Slides 1.4.6])                   |
| 5    | 20.10.2021  | List                                        | A closer look at lists ([Video][Video 1.5.1], [Slides][Slides 1.5.1])<br/>Tuples and generic methods ([Video][Video 1.5.2], [Slides][Slides 1.5.2])<br/>Higher order list functions ([Video][Video 1.5.3], [Slides][Slides 1.5.3])<br/>Reduction of lists ([Video][Video 1.5.4], [Slides][Slides 1.5.4])<br/>Reasoning about lists ([Video][Video 1.5.5], [Slides][Slides 1.5.5])                   |
| 6    | 27.10.2021  | Collection                                  | Other Collections ([Video][Video 1.6.1], [Slides][Slides 1.6.1])<br/>Combinatorial Search and For-Expressions ([Video][Video 1.6.2], [Slides][Slides 1.6.2])<br/>Combinatorial Search Example ([Video][Video 1.6.3], [Slides][Slides 1.6.3])<br/>Maps ([Video][Video 1.6.4], [Slides][Slides 1.6.4])<br/>Putting the Pieces Together ([Video][Video 1.6.5], [Slides][Slides 1.6.5]) |
| 7    | 03.11.2021  | Monads                                      | Recap ([Video][Video 2.1.1], [Slides][Slides 2.1.1])<br/>Queries with for ([Video][Video 2.1.2], [Slides][Slides 2.1.2])<br/>Translation of for ([Video][Video 2.1.3], [Slides][Slides 2.1.3])<br/>Functional Random Generators ([Video][Video 2.1.4], [Slides][Slides 2.1.4])<br/>Monads ([Video][Video 2.1.5], [Slides][Slides 2.1.5])<br/>Exceptional Monads ([Video][Video 2.1.6], [Slides][Slides 2.1.6])                   |
| 8    | 10.11.2021  | **Midterm exam**                            | -        |
| 9    | 17.11.2021  | Lazy evaluation                             | Structural Induction on Trees ([Video][Video 2.2.1], [Slides][Slides 2.2.1])<br/>Lazy Lists ([Video][Video 2.2.2], [Slides][Slides 2.2.2])<br/>Lazy Evaluation ([Video][Video 2.2.3], [Slides][Slides 2.2.3])<br/>Infinite Sequences ([Video][Video 2.2.4], [Slides][Slides 2.2.4])<br/>Case Study ([Video][Video 2.2.5], [Slides][Slides 2.2.5])                   |
| 10   | 24.11.2021  | Type-directed computation                   | Contextual abstraction ([Video][Video 2.3.1], [Slides][Slides 2.3.1])<br/>Using clauses and given instances ([Video][Video 2.3.2], [Slides][Slides 2.3.2])<br/>Type classes ([Video][Video 2.3.3], [Slides][Slides 2.3.3])<br/>Abstract algebra and type classes ([Video][Video 2.3.4], [Slides][Slides 2.3.4])<br/>Context passing ([Video][Video 2.3.5], [Slides][Slides 2.3.5])<br/>Implicit function types ([Video][Video 2.3.6], [Slides][Slides 2.3.6])                   |
| 11   | 01.12.2021  | State                                       | Functions and state ([Video][Video 2.4.1], [Slides][Slides 2.4.1])<br/>Identity and change ([Video][Video 2.4.2], [Slides][Slides 2.4.2])<br/>Loops ([Video][Video 2.4.3], [Slides][Slides 2.4.3])<br/>Discrete Event Simulation ([Video][Video 2.4.4], [Slides][Slides 2.4.4])                  |
| 12   | 08.12.2021  | Interpreter I                               | Interpreter for Arithmetic ([Video][Video 3.1.1], [Slides][Slides 3.1.1])<br/>Substitution Interpreter for Recursive Functions ([Video][Video 3.1.2], [Slides][Slides 3.1.2])<br/>Environment Instead of Substitutions ([Video][Video 3.1.3], [Slides][Slides 3.1.3])<br/>Higher-Order Functions Using Naive Substitutions ([Video][Video 3.1.4], [Slides][Slides 3.1.4])<br/>Avoiding Variable Capture ([Video][Video 3.1.5], [Slides][Slides 3.1.5])<br/>Higher-Order Functions Using Environments ([Video][Video 3.1.6], [Slides][Slides 3.1.6])<br/>Nested Recursive Definitions ([Video][Video 3.1.7], [Slides][Slides 3.1.7])   |
| 13   | 15.12.2021  | Parsing with Combinators / Lambda Calculus  | Parsing with Combinators ([Video][Video 3.2.1])<br/>Recursion as Self-Application ([Video][Video 3.2.2])<br/>Church Numerals and Conditionals ([Video][Video 3.2.3]) |
| 14   | 22.12.2021  | **Final exam**                              | -        |

## Exercise (Recitation Session) Schedule

Exercises (aka recitation sessions) take place on Wednesdays from 13:15 to 15:00.

| Title                                          | Handout Released | Session (Wednesdays 13:15 to 15:00) | Solution Released |
| :--                                            | :--              | :--                     | :--              |
| First week tasks                               | -                | 22.09.2021              | -                |
| Exercise Session 1                             | -                | 29.09.2021              | 04.10.2021       |
| Exercise Session 2                             | 04.10.2021       | 06.10.2021              | 11.10.2021       |
| Exercise Session 3                             | 11.10.2021       | 13.10.2021              | 18.10.2021       |
| Exercise Session 4                             | 18.10.2021       | 20.10.2021              | 25.10.2021       |
| Exercise Session 5                             | 25.10.2021       | 27.10.2021              | 01.11.2021       |
| Exercise Session 6                             | 01.11.2021       | 03.11.2021              | 08.11.2021       |
| **Midterm exam**                               | -                | 10.11.2021              | -                |
| Exercise Session 7                             | 15.11.2021       | 17.11.2021              | 22.11.2021       |
| Exercise Session 8                             | 22.11.2021       | 24.11.2021              | 29.11.2021       |
| Exercise Session 9                             | 29.11.2021       | 01.12.2021 & 08.12.2021 | 13.12.2021       |
| Exercise Session 10                            | 06.12.2021       | 08.12.2021 & 15.12.2021 | 20.12.2021       |
| **Final exam**                                 | -                | 22.12.2021              | -                |

Exercises are pen and paper style questions that will prepare you for the final exam.
Exercises should be done in groups.

## Lab Schedule

Lab sessions take place on Fridays from 10:15 to 12:00.

| Title                             | Start Date | Session (Fridays 10:15 to 12:00) | Due Date ([AoE](https://en.wikipedia.org/wiki/Anywhere_on_Earth)) |
| :--                               | :--        | :--                     | :--        |
| Recursion                         | 22.09.2021 | 24.09.2021              | 03.10.2021 |
| Functional Sets                   | 29.09.2021 | 01.10.2021              | 07.10.2021 |
| Object-Oriented Sets              | 06.09.2021 | 08.09.2021              | 14.10.2021 |
| Huffman Coding                    | 13.10.2021 | 15.10.2021 & 22.10.2021 | 28.10.2021 |
| Anagrams                          | 27.10.2021 | 29.10.2021              | 11.11.2021 |
| Quickcheck                        | 03.11.2021 | 05.11.2021              | 18.11.2021 |
| Bloxorz                           | 10.11.2021 | 12.11.2021 & 19.11.2021 | 25.11.2021 |
| Codecs                            | 24.11.2021 | 26.11.2021 & 03.12.2021 | 09.12.2021 |
| Interpreter                       | 08.12.2021 | 10.12.2021 & 17.12.2021 | 23.12.2021 |

Labs are individual assignments where you get to write Scala programs using the concepts learned during lectures.
Labs are submitted by pushing your code on GitLab, see details in the [grading and submission](labs/grading-and-submission.md) page.

## Exam Schedule

The midterm exam will be on 10.11.2021.

The final exam will be on 22.12.2021.

Information about exam organization will be communicated by email a few days before the exam.


[Video 1.1.1]: https://tube.switch.ch/videos/7ed71e65
[Video 1.1.2]: https://tube.switch.ch/videos/eefaaa33
[Video 1.1.3]: https://tube.switch.ch/videos/7ec55c9c
[Video 1.1.4]: https://tube.switch.ch/videos/f8abe6bf
[Video 1.1.5]: https://tube.switch.ch/videos/1f8d3205
[Video 1.1.6]: https://tube.switch.ch/videos/9274e0f4
[Video 1.1.7]: https://tube.switch.ch/videos/1843caa3
[Slides 1.1.1]: ./slides/progfun1-1-1.pdf
[Slides 1.1.2]: ./slides/progfun1-1-2.pdf
[Slides 1.1.3]: ./slides/progfun1-1-3.pdf
[Slides 1.1.4]: ./slides/progfun1-1-4.pdf
[Slides 1.1.5]: ./slides/progfun1-1-5.pdf
[Slides 1.1.6]: ./slides/progfun1-1-6.pdf
[Slides 1.1.7]: ./slides/progfun1-1-7.pdf

[Video 1.2.1]: https://tube.switch.ch/videos/646cfe4f
[Video 1.2.2]: https://tube.switch.ch/videos/9e573d2f
[Video 1.2.3]: https://tube.switch.ch/videos/0e2be793
[Video 1.2.4]: https://tube.switch.ch/videos/ddcbb43f
[Video 1.2.5]: https://tube.switch.ch/videos/dec623bc
[Video 1.2.6]: https://tube.switch.ch/videos/6e8643cf
[Video 1.2.7]: https://tube.switch.ch/videos/p6uOZxpZO0
[Slides 1.2.1]: ./slides/progfun1-2-1.pdf
[Slides 1.2.2]: ./slides/progfun1-2-2.pdf
[Slides 1.2.3]: ./slides/progfun1-2-3.pdf
[Slides 1.2.4]: ./slides/progfun1-2-4.pdf
[Slides 1.2.5]: ./slides/progfun1-2-5.pdf
[Slides 1.2.6]: ./slides/progfun1-2-6.pdf
[Slides 1.2.7]: ./slides/progfun1-2-7.pdf

[Video 1.3.1]: https://tube.switch.ch/videos/56c88e00
[Video 1.3.2]: https://tube.switch.ch/videos/1c969056
[Video 1.3.3]: https://tube.switch.ch/videos/PE4EZHTXL1
[Video 1.3.4]: https://tube.switch.ch/videos/9081e1da
[Video 1.3.5]: https://tube.switch.ch/videos/e409b899
[Slides 1.3.1]: ./slides/progfun1-2-1.pdf
[Slides 1.3.2]: ./slides/progfun1-3-2.pdf
[Slides 1.3.3]: ./slides/progfun1-3-3.pdf
[Slides 1.3.4]: ./slides/progfun1-3-4.pdf
[Slides 1.3.5]: ./slides/progfun1-3-5.pdf

[Video 1.4.1]: https://tube.switch.ch/videos/f5879da4
[Video 1.4.2]: https://tube.switch.ch/videos/e7df77e5
[Video 1.4.3]: https://tube.switch.ch/videos/978832a8
[Video 1.4.4]: https://tube.switch.ch/videos/xmEdj2V0Xh
[Video 1.4.5]: https://tube.switch.ch/videos/9a844297
[Video 1.4.6]: https://tube.switch.ch/videos/35c4e417
[Slides 1.4.1]: ./slides/progfun1-4-1.pdf
[Slides 1.4.2]: ./slides/progfun1-4-2.pdf
[Slides 1.4.3]: ./slides/progfun1-4-3.pdf
[Slides 1.4.4]: ./slides/progfun1-4-4.pdf
[Slides 1.4.5]: ./slides/progfun1-4-5.pdf
[Slides 1.4.6]: ./slides/progfun1-4-6.pdf

[Video 1.5.1]: https://tube.switch.ch/videos/8e9cf6a5
[Video 1.5.2]: https://tube.switch.ch/videos/40edd184
[Video 1.5.3]: https://tube.switch.ch/videos/af626839
[Video 1.5.4]: https://tube.switch.ch/videos/e0e380fe
[Video 1.5.5]: https://tube.switch.ch/videos/9ebad679
[Slides 1.5.1]: ./slides/progfun1-5-1.pdf
[Slides 1.5.2]: ./slides/progfun1-5-2.pdf
[Slides 1.5.3]: ./slides/progfun1-5-3.pdf
[Slides 1.5.4]: ./slides/progfun1-5-4.pdf
[Slides 1.5.5]: ./slides/progfun1-5-5.pdf

[Video 1.6.1]: https://tube.switch.ch/videos/58a6fe2a
[Video 1.6.2]: https://tube.switch.ch/videos/a09a7679
[Video 1.6.3]: https://tube.switch.ch/videos/7f2fcf99
[Video 1.6.4]: https://tube.switch.ch/videos/a4519732
[Video 1.6.5]: https://tube.switch.ch/videos/30005570
[Slides 1.6.1]: ./slides/progfun1-6-1.pdf
[Slides 1.6.2]: ./slides/progfun1-6-2.pdf
[Slides 1.6.3]: ./slides/progfun1-6-3.pdf
[Slides 1.6.4]: ./slides/progfun1-6-4.pdf
[Slides 1.6.5]: ./slides/progfun1-6-5.pdf
[Slides 1.6.6]: ./slides/progfun1-6-6.pdf

[Video 2.1.1]: https://tube.switch.ch/videos/680a1d2a
[Video 2.1.2]: https://tube.switch.ch/videos/935b0da5
[Video 2.1.3]: https://tube.switch.ch/videos/2ac4c232
[Video 2.1.4]: https://tube.switch.ch/videos/f9c5677b
[Video 2.1.5]: https://tube.switch.ch/videos/DJmNHpUHba
[Video 2.1.6]: https://tube.switch.ch/videos/fdfb0609
[Slides 2.1.1]: ./slides/progfun2-1-1.pdf
[Slides 2.1.2]: ./slides/progfun2-1-2.pdf
[Slides 2.1.3]: ./slides/progfun2-1-3.pdf
[Slides 2.1.4]: ./slides/progfun2-1-4.pdf
[Slides 2.1.5]: ./slides/progfun2-1-5.pdf
[Slides 2.1.6]: ./slides/progfun2-1-6.pdf

[Video 2.2.1]: https://tube.switch.ch/videos/0accfa13
[Video 2.2.2]: https://tube.switch.ch/videos/fbd7e361
[Video 2.2.3]: https://tube.switch.ch/videos/8506774b
[Video 2.2.4]: https://tube.switch.ch/videos/7064a6b1
[Video 2.2.5]: https://tube.switch.ch/videos/889a5305
[Slides 2.2.1]: ./slides/progfun2-2-1.pdf
[Slides 2.2.2]: ./slides/progfun2-2-2.pdf
[Slides 2.2.3]: ./slides/progfun2-2-3.pdf
[Slides 2.2.4]: ./slides/progfun2-2-4.pdf
[Slides 2.2.5]: ./slides/progfun2-2-5.pdf

[Video 2.3.1]: https://tube.switch.ch/videos/d5df9a21
[Video 2.3.2]: https://tube.switch.ch/videos/xRHmz1nTpz
[Video 2.3.3]: https://tube.switch.ch/videos/XNgbIOT2Yb
[Video 2.3.4]: https://tube.switch.ch/videos/FnmJTs1Vqu
[Video 2.3.5]: https://tube.switch.ch/videos/pWXI0T9FtX
[Video 2.3.6]: https://tube.switch.ch/videos/NKZ0IVR9Yi
[Slides 2.3.1]: ./slides/progfun2-3-1.pdf
[Slides 2.3.2]: ./slides/progfun2-3-2.pdf
[Slides 2.3.3]: ./slides/progfun2-3-3.pdf
[Slides 2.3.4]: ./slides/progfun2-3-4.pdf
[Slides 2.3.5]: ./slides/progfun2-3-5.pdf
[Slides 2.3.6]: ./slides/progfun2-3-6.pdf

[Video 2.4.1]: https://tube.switch.ch/videos/f32bc013
[Video 2.4.2]: https://tube.switch.ch/videos/7bf009ce
[Video 2.4.3]: https://tube.switch.ch/videos/zEyrIXFFPV
[Video 2.4.4]: https://tube.switch.ch/videos/CvuKzoNjRg
[Slides 2.4.1]: ./slides/progfun2-4-1.pdf
[Slides 2.4.2]: ./slides/progfun2-4-2.pdf
[Slides 2.4.3]: ./slides/progfun2-4-3.pdf
[Slides 2.4.4]: ./slides/progfun2-4-4.pdf

[Video 2.5.1]: https://tube.switch.ch/videos/5ca69d05
[Video 2.5.2]: https://tube.switch.ch/videos/700fc8b5
[Video 2.5.3]: https://tube.switch.ch/videos/d93a3d12
[Slides 2.5.1]: ./slides/progfun2-5-1.pdf
[Slides 2.5.2]: ./slides/progfun2-5-2.pdf
[Slides 2.5.3]: ./slides/progfun2-5-3.pdf

[Video 3.1.1]: https://tube.switch.ch/videos/b053ad9d
[Video 3.1.2]: https://tube.switch.ch/videos/59b7ae00
[Video 3.1.3]: https://tube.switch.ch/videos/0ccb68d7
[Video 3.1.4]: https://tube.switch.ch/videos/0de70fa1
[Video 3.1.5]: https://tube.switch.ch/videos/94bc1565
[Video 3.1.6]: https://tube.switch.ch/videos/6d332501
[Video 3.1.7]: https://tube.switch.ch/videos/18ba7117
[Slides 3.1.1]: ./slides/progfun3-1-1.pdf
[Slides 3.1.2]: ./slides/progfun3-1-2.pdf
[Slides 3.1.3]: ./slides/progfun3-1-3.pdf
[Slides 3.1.4]: ./slides/progfun3-1-4.pdf
[Slides 3.1.5]: ./slides/progfun3-1-5.pdf
[Slides 3.1.6]: ./slides/progfun3-1-6.pdf
[Slides 3.1.7]: ./slides/progfun3-1-7.pdf

[Video 3.2.1]: https://tube.switch.ch/videos/d08dd17f
[Video 3.2.2]: https://tube.switch.ch/videos/17841152
[Video 3.2.3]: https://tube.switch.ch/videos/f203e6a9
[Slides 3.2.1]: ./slides/progfun3-2-1.pdf
[Slides 3.2.2]: ./slides/progfun3-2-2.pdf
[Slides 3.2.3]: ./slides/progfun3-2-3.pdf