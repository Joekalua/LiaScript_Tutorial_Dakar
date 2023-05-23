<!--
author:   André Dietrich & Sebastian Zug

email:    LiaScript@mail.org

version:  0.0.1

language: en

narrator: US English Female

comment:  Short Introduction on LiaScript.

import:   https://raw.githubusercontent.com/LiaTemplates/algebrite/0.2.1/README.md
          https://raw.githubusercontent.com/LiaTemplates/ABCjs/0.0.2/README.md
          https://raw.githubusercontent.com/liaTemplates/TextAnalysis/main/README.md

notranslate: <span class="notranslate">(@0)</span>

-->

# LiaScript

              --{{0}}--
Hi, I am LiaScript a Markup language and interpreter for educational content.
The goal of my developers was to create a open and easy to use way to develop and distribute educational content.

![eLearning Africa Logo](https://www.elearning-africa.com/conference2023/ressources/banner/2023/social_1200_630.png)

## Features

Markdown is intended to be as easy-to-read and easy-to-write as is feasible, but unfortunately for static content only.
LiaScript is based on Markdown and extends it in various ways.


                      {{1}}
***********************************************************

__Quizzes & Surveys__

                    --{{1}}--
To our knowledge, there is no simpler way of creating quizzes and questionnaires.

Weird German articles, guess the right one for "Mädchen", which means girl:

- [( )]  male   @notranslate(der)
- [( )]  female @notranslate(die)
- [(X)]  neuter @notranslate(das)

***********************************************************


                      {{2}}
***********************************************************

__Interactive Coding__

The original goal was to create coding courses fast.
But the same principals can be used to teach writing, mathematics, and music-theory too.

```
Playing games has always been thought to be important to
the development of well-balanced and creative children;
however, what part, if any, they should play in the lives
of adults has never been researched that deeply. I believe
that playing games is every bit as important for adults
as for children. Not only is taking time out to play games
with our children and other adults valuable to building
interpersonal relationships but is also a wonderful way
to release built up tension.
```
@Textanalysis.FULL


-------------------------------------------------

```
(3 * x - 5x)^3 * (x + x)

60!
```
@Algebrite.eval


-------------------------------------------------

``` abc
% channel: 0
% autoplay: true
X:353
T: GLUECK AUF DER STEIGER KOEMMT
N: E1512
O: Europa, Mitteleuropa, Deutschland
R: Staende -, Bergmanns - Lied
M: 4/4
L: 1/16
K: G
 | G8F4A4 | G8z8 |
B8A4c4 | B8z4
G2A2 | B4B4B4A2B2 | c4A3AA4
A2B2 | c4c4c4B2c2 | d4B3BB4
A4 | G8F8 | G4e4d4
c2A2 | B8A8 | G8z8
```
@ABCJS.eval

-------------------------------------------------


***********************************************************


                      {{3}}
***********************************************************

__Multimedia__

Of course you can add any kind of multimedia content and content from other sites as well.

![Portrait of a lady](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Leonardo_da_Vinci_%28attrib%29-_la_Belle_Ferroniere.jpg/723px-Leonardo_da_Vinci_%28attrib%29-_la_Belle_Ferroniere.jpg "La Belle Ferronnière, c. 1490–1498")
!?[Fun with Tables](https://www.youtube.com/watch?v=Y_7q9T5jYHo)
??[Beating heart](https://sketchfab.com/3d-models/beating-heart-d9845afb1ee64ad094adc96320c67d98 "'Beating Heart' (https://skfb.ly/owVVo) by Dreamwasabducted")


***********************************************************


                      {{4}}
***********************************************************

__Animations & TextToSpeach__

                    --{{4}}--
One document can be presented in various ways.
You can use it for presentations with animation steps, read it like a textbook, or use it like an interactive screen-cast.
Just click on the presentation button to switch between modes.

***********************************************************

## Vision

The idea is simple, make engaging educational content easy to write and create.
Distribute it via different sources using the latest Web 3.0 technologies, (no central server required).

https://liascript.github.io/LiveEditor/?/show/file/https://raw.githubusercontent.com/LiaPlayground/LiaScript_Tutorial_Dakar/main/01_Introduction.md

## Survey

### 1. What do you expect from this tutorial?

- [[ideas]]         Ideas for own courses
- [[collaboration]] Understanding processes for collaborative course development
- [[technologies]]  Overview on web technologies / eduTech
- [[sharing]]       Methods for sharing content for free
- [[markdown]]      Get to know Markdown
- [[i18n]]          Internationalization

### 2. What tools / systems (LMS) did you use prior to create learning materials?

Separate them by comma.

   [[___]]

### 3. How would you rate your knowledge related to

Please chose a "1" for novice and "5" for expert!

   [(1)(2)(3)(4)(5)]
   [               ] Markdown
   [               ] Web development
   [               ] Git/Github
   

### 5. How many online course have you designed?

- [(none)] None so far
- [(< 5)]  Less than 5
- [(< 10)] Less than 10
- [(more)] More than 10