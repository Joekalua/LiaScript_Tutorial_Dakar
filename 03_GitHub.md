<!--

author:   Sebastian Zug, André Dietrich 
email:    sebastian.zug@informatik.tu-freiberg.de
version:  0.0.2

language: en
narrator: US English Female

icon: https://upload.wikimedia.org/wikipedia/commons/d/de/Logo_TU_Bergakademie_Freiberg.svg

import: https://raw.githubusercontent.com/liascript-templates/plantUML/master/README.md

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://LiaScript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/LiaScript_Tutorial_Kigali/main/C-GitHub_Tutorial.md)

# Github Introduction

Let's start!

## Version management - Why?

                                   {{0-2}}
******************************************************************************

What was the largest document you have worked on so far? How did you organize your progress?

1. in the worst case you didn't think about it at all and wrote into the same document over and over again.
2. a touch better is the idea of making new copies of the folder weekly and naming them something like this:

```console
▶ ls
myProject
myProject_test
myProject_newTest
myProject_Moms_corrections
...
```

3. If you "had a plan", you made a copy of all files in a folder every day and named them systematically.

```console
▶ ls
myProject_01042021
myProject_02042021
myProject_03042021
...
```

******************************************************************************


                          {{1-2}}
******************************************************************************

Briefly consider how to find answers to the following questions:

* "When was the last state of file x.y deleted?"
* "In which version did I make the adjustment to the headings?"
* "How can I undo this despite other changes made in the meantime?"
* "Why didn't I make a copy of this?"
* "..."

In any case, a lot of manual work ...

******************************************************************************

                          {{2-3}}
> In software development, this problem is solved by version management systems. We want to apply the existing methods for this to OER.

## Version management

> Definition: A version management is a system used to record changes to documents or files. All versions are saved in an archive with a time stamp and user ID and can be restored later. Version management systems are typically used in software development to manage source code.

                                {{1-2}}
******************************************************************************

Example - Wikipedia version management system

![Wikipedia History](images/VersionenVonVersionsverwaltung.png "Versions of the article version management on the Wikipedia website")

Features:

+ Logging of changes: It can be traced at any time who changed what and when.
+ Restoration of old states of individual files: Thus, accidental changes can be undone at any time.
+ Archiving of individual statuses of a project: This makes it possible to access all versions at any time.
+ Coordination of shared access to files by several developers.
+ Simultaneous development of several development branches of a project, which must not be confused with the fork of another project.

******************************************************************************

## Git

The development history of git is connected to the Linux kernel with thousands of contributors

| year | method of version control                                      |
| ---- | -------------------------------------------------------------- |
| 1991 | Changes to the Linux kernel via patches and archive files      |
| 2002 | Linux kernel managed with the BitKeeper tool                   |
| 2005 | Break between the distributing company and the Linux community |
| 2021 | The current version is 2.31.1                                  |

In 2005 a list of requirements for a new development was defined. It was emphasized that it must be able to support especially very large projects (number of developers, features and lines of code, files). From this `Git` was developed as free software for distributed version management of files.

> Git dominates software development either as a single installation or embedded in various development platforms!

### State model of a file in Git

Files can have different states with which they are marked in Git repositories.

                       {{0-1}}
********************************************************************************

```text @plantUML.png
@startuml
hide empty description
[*] --> Untracked : Generation of a file
Untracked --> Staged : Added to repository
Unmodified --> Modified : Adaptations
Modified --> Staged : Attributed as a new version
Staged --> Unmodified : Accepted 
Unmodified --> Untracked : Deleted from repository
@enduml
```

********************************************************************************

### Basic usage

The state model of a file results in three levels on which we can classify a file in Git perspective - working directory, stage and repository.

```ascii
                     local                           remote
  ---------------------------------------------  --------------
  Working         "Staging"        local          remote
  copy                             repository     repository
                       |               |
                       |               |
                       |               |
       +-+- - - - - - -|- - - - - - - -|
       | | Adaptations |               |
       | |             |               |
       +-+             |               |
        |   git add    |               |
        |------------->|  git commit   |
        |              |-------------->|
       +-+             |               |
       | | further     |               |
       | | Adaptations |               |
       +-+             |               |
        |   git add    |               |
        +------------->|  git commit   |
                       |-------------->|
                       |               |                                           .
```

### Distributed Version Management

```ascii
                      local                           remote
   ---------------------------------------------  --------------
   Working         "Staging"        local          remote
   copy                             repository     repository
                       |               |                 |
                       |               |    git clone    |
                       |               |<----------------|
       +-+- - - - - - -|- - - - - - - -|                 |
       | | Adaptations |               |                 |
       | |             |               |                 |
       +-+             |               |                 |
        |   git add    |               |                 |
        |------------->|  git commit   |                 |
        |              |-------------->|                 |
       +-+             |               |                 |
       | | further     |               |                 |
       | | Adaptations |               |                 |
       +-+             |               |                 |
        |   git add    |               |                 |
        +------------->|  git commit   |                 |
                       |-------------->|   git push      |
                       |               |---------------->|
                       |               |                 |                     .
```


### Working with Branches

The organization of versions in different branches is a central element of working with git.
element of working with git. Branches are branches of code that encapsulate specific development
development goals.

![Git version tree](img/git.png)

A branch in Git is simply a pointer to a commit. The central branch is usually referred to as `master` (old name) or `main` (new name).

## GitHub

GitHub is a platform that offers online Git version management and adds it to a project management. Besides coordinating the versions, they can be linked to tasks, milestones can be checked and certain tasks can be executed automatically.

![alt-text](images/ScreenshotTutorialSeite.png)

> Let's take a closer view and generate your first Github project.




### Perfect OER Material - a text file

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii

Version 1.0                           Version 1.1
+---------------------------+          +---------------------------+
| Course  German Literatur  |          | Course  German Literature |
| Authors John Muster       | "Error"  | Authors John Muster       |
|                           |------->  |         Angelika Maier    |----->
|~~~~~~~~~~~~~~~~~~~~~~~~~~~|          |~~~~~~~~~~~~~~~~~~~~~~~~~~~|
| In 1756 Goethe visited    |---.      | In 1786 Goethe visited    |--.
| Italy ...                 |   |      | Italy ...                 |  |
                                |                                     |
                                |                                     |    +----------------------------+
                                |                                     |    | Course  Deutsche Literatur |
                                |                                     |    | Authors John Muster        |
                                |                                     .--> |         Angelika Maier     |
                                |                                          |         Steve Gray         |
                                |                                          |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|
                                |                                          | 1786 reiste Goethe nach    |
                                |                                          | Italien ...                |
                                |       Version 1.0
                                |      +---------------------------+
                                |      | Course  Goethe & Schiller |
                                |      | Authors John Muster       |
                                .-->   |         Angelika Maier    |----->
                                       |~~~~~~~~~~~~~~~~~~~~~~~~~~~|
                                       | The correspondence during |
                                       | the Italian journey ...   |
```
*Versions of the teaching content of a course and its reuse in other courses*.

{{0-1}}
********************************************************************************

| requirement       | txt |                                                         |
| ----------------- | --- | ------------------------------------------------------- |
| `storing/copying` | ++  | advantageous because of small size                      |
| `use`             | ++  | analog / digital distribution to students uncomplicated |
| `process`         | ++  | processable without additional software                 |
| `adapting/mixing` | ++  | simple combination of text fragments via copy&paste     |
| `disseminate`     | ++  | easily exportable                                       |

> **A pure text file can cover all ideas of OER? Obviously our list of requirements is not complete.**

********************************************************************************

                    {{1-2}}
********************************************************************************

the 5V definition ...

> _1. ... focuses on the Open in OER but leaves aside the Education._
>
> _2. ... ignores the need for a version management system._
>
> _3. ... does not consider the findability of OER content._

| requirement                                   | txt                           |                                                         |
| --------------------------------------------- | ----------------------------- | ------------------------------------------------------- |
| `storing/copying`                             | ++                            | advantageous because of small size                      |
| `use`                                         | +                             | analog / digital distribution to students uncomplicated |
| `process`                                     | ++                            | processable without additional software                 |
| `adapting/mixing`                             | ++                            | simple combination of text fragments via copy&paste     |
| `disseminate`                                 | ++                            | easily exportable                                       |
| <!-- Style="color:green" --> manage / version | <!-- Style="color:red" --> ?? |                                                         |
| <!-- Style="color:green" --> motivate         | <!-- Style="color:red" --> -- | no contemporary formats and interactive content         |

> __Obviously, we need formats that cover the extended set of requirements in addition to the positive aspects of text representations.__

********************************************************************************



### Comparison with Wikipedia

> Can Wikipedia be the inspiration for OER?

| Aspect     | Wikipedia - Solution                                                             | Disadvantage                                                             |
| ---------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| search     | one instance of an article directly retrievable                                  | no different expressions possible for one topic.                         |
| tools      | integrated editor based on a Markdown dialect                                    | strong limitation of possibilities to structured texts, formulas, images |
| quality    | sophisticated review system with experts, version data collection and comparison |                                                                          |
| visibility | authorship visible in version history                                            |                                                                          |


### OER in reality

                {{0-1}}
********************************************************************************

Types of files labeled with "OER" on TU Bergakademie's servers:

<!--
data-title="Ratio of formats within the OPAL LMS in Saxony"
data-transpose
-->
| Datatype | Amount |
| -------- | -----: |
| `pdf`    |   5242 |
| `jpg`    |   1040 |
| `mkv`    |    873 |
| `mp4`    |    586 |
| `png`    |    494 |
| `zip`    |    443 |
| `html`   |    387 |
| `docx`   |    376 |
| `pptx`   |    245 |
| `xlsx`   |    191 |


The materials in OPAL come predominantly without licenses and as closed file format.
A reuse is accordingly only with difficulty possible.

********************************************************************************

                 {{1-2}}
********************************************************************************


| Level                               | Core Statement                                                                   |
| ----------------------------------- | -------------------------------------------------------------------------------- |
| Emotional classification            | "_Everyone can use my work for themselves!_"                                     |
|                                     | "_Anyone can control me!_"                                                       |
| Legal Challenges                    | "_I use a lot of graphics whose copyright I am unsure of at best!_"              |
| Findability                         | "_I can't find content that I can profitably integrate into my teaching!_"       |
| <!-- style="color:red" --> Effort   | <!-- style="color:red" --> "_You must have studied computer science!_"           |
| <!-- style="color:red" --> Coverage | <!-- style="color:red" --> "_But there are missing interfaces for my tools XY!_" |

********************************************************************************

### Vision

OER Materials must ...

> 1. be transformable to enable reuse. (_Process/Use/Disseminate_).
> 2. contain metadata to be discoverable. (_Disseminate_)
> 3. embed an systematic version history (_Manage_).

<!--
style="width: 100%; max-width: 860px; display: block; margin-left: auto; margin-right: auto;"
-->
```ascii           Transformation of OER materials for use in various LMSs.
   +---------------------+
   | # Digital Systems V1|\
 +--------------------+  +-+
 | # Digital Systems  |\
+------------------+  +-+
| # Digital Systems|\                                      .-----------.
| (SoSe 2021)      +-+                              ╔══════|   LMS  X  |══════╗
|                    |  --------------------------> ║      '-----------'      ║
| ## Task 1          |                              ║ Digital Systems 2021    ║
|                    |                              ║                         ║
| + Implement ...    | --------------+              ║ import numpy as np      ║
|                    |    Trans-     |              ║ ...                     ║
|                    |    formation  |              ╚═════════════════════════╝
+--------------------+               v
                                .-,(   ),-.                .-----------.
License: ...                 .-(           )-.      ╔══════|   LMS  Y  |══════╗
Content: ...                (    OER Cloud    )     ║      '-----------'      ║
Author: ...                  '-(           )-'  +-->║ Digital Systems 2021    ║
Versions: ...                   '-.(   ).-'     |   ║                         ║
                                     |          |
                                     +----------+          .-----------.
                                                |   ╔══════|  Webapp   |══════╗
                                                |   ║      '-----------'      ║
                                                +-->║ Digital Systems 2021    ║
                                                    ║                         ║
```


### Experiences with the use of OER

-> Course overview of the _Software Development and Robotics_ working group on [GitHub](https://github.com/TUBAF-IfI-LiaScript).

Results:

1. a "we" idea emerges from collaboration on materials in the context of a core team.
2. bugs are weeded out much faster than in years past. "Short-term" quality increases.
3. interaction between teachers and students increases - *"Shouldn't we explain it better this way... "*.
4. the understanding about distributed development develops very positively, even the non-computer science students are able to deal with the methods.
