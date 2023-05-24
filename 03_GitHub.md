<!--

author:   Sebastian Zug, André Dietrich 
email:    sebastian.zug@informatik.tu-freiberg.de
version:  0.0.2

language: en
narrator: US English Female

icon: https://upload.wikimedia.org/wikipedia/commons/d/de/Logo_TU_Bergakademie_Freiberg.svg

import: https://raw.githubusercontent.com/liascript-templates/plantUML/master/README.md

-->

[![LiaScript](https://raw.githubusercontent.com/LiaScript/LiaScript/master/badges/course.svg)](https://LiaScript.github.io/course/?https://raw.githubusercontent.com/LiaPlayground/LiaScript_Tutorial_Dakar/main/03_GitHub.md)

# How to handle different versions - Github Introduction

Motivation
========================

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


                         {{1-2}}
***************************************************************************

>  **Open Courseware / Open Educational Resources** ... teaching, learning and
> research materials in any medium, digital or otherwise,that reside in the
> **public domain** or have been released under an open license that permits
> no-cost access, use, **adaptation** and **redistribution** by others with no or 4
> limited restrictions. Open licensing is built within the existing framework of
> intellectual property rights as defined by relevant international conventions
> and respects the authorship of the work
>
> -- UNESCO 2002 Forum on the Impact of Open Courseware for Higher Education in Developing Countries [(Link)](https://unesdoc.unesco.org/ark:/48223/pf0000128515)


| requirement       | txt |                                                         |
| ----------------- | --- | ------------------------------------------------------- |
| `storing/copying` | ++  | advantageous because of small size                      |
| `use`             | ++  | analog / digital distribution to students uncomplicated |
| `process`         | ++  | processable without additional software                 |
| `adapting/mixing` | ++  | simple combination of text fragments via copy&paste     |
| `disseminate`     | ++  | easily exportable                                       |

***************************************************************************

### Version management - Intuitive Approach

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

###  Version management - Wikipedia Approach

> Can Wikipedia be the inspiration for Versionmanagment?

![Wikipedia History](images/VersionenVonVersionsverwaltung.png "Versions of the article version management on the Wikipedia website")

| Aspect     | Wikipedia - Solution                                                             | Disadvantage                                                             |
| ---------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| search     | one instance of an article directly retrievable                                  | no different expressions possible for one topic.                         |
| tools      | integrated editor based on a Markdown dialect                                    | strong limitation of possibilities to structured texts, formulas, images |
| quality    | sophisticated review system with experts, version data collection and comparison |                                                                          |
| visibility | authorship visible in version history                                            |                                                                          |


## Version management

> Definition: A version management is a system used to record changes to documents or files. All versions are saved in an archive with a time stamp and user ID and can be restored later. Version management systems are typically used in software development to manage source code.

Features:

+ Logging of changes: It can be traced at any time who changed what and when.
+ Restoration of old states of individual files: Thus, accidental changes can be undone at any time.
+ Archiving of individual statuses of a project: This makes it possible to access all versions at any time.
+ Coordination of shared access to files by several developers.
+ Simultaneous development of several development branches of a project, which must not be confused with the fork of another project.

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

## GitHub

GitHub is a platform that offers online Git version management and adds it to a project management. Besides coordinating the versions, they can be linked to tasks, milestones can be checked and certain tasks can be executed automatically.

![alt-text](images/ScreenshotTutorialSeite.png)

> Let's take a closer view and generate your first Github project.