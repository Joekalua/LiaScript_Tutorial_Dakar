# Tutorial

Keyboard shortcut: Compile - <kbd>Ctrl</kbd> + <kbd>S</kbd>

Snippets: start typing

* lia ... for LiaScript related issues
* voice ... for text to speech voices
* hili ... programming languages

## 1. Markdown

Headers

By now you should have noticed, that # (hash-tags) are used to structure your content.
The number of # defines the header-type and indentation.

------------------------

Task:

Try to structure the document according to:


<!-- style="max-width: 300px; width: 100%" -->
`````````````````````````````````````
Tutorial
|
O----- 1. Markdown
|      |
|      O---- Paragraphs
|      |
|      O---- Lists
|      |     |
|      |     o--- Numbered Lists
|      |
|      O---- Formatting
|      |
|      O---- Block-quotes
|      |
|      O---- Links & References
|      |     |
|      |     O--- Images
|      |
|      O---- Tables
|
O----- 2. LiaScript
`````````````````````````````````````

# Paragraphs

A paragraph and other markdown-blocks, that we will get to know, are separated visually from each other by empty lines.
These lines are thus interpreted as one single paragraph.

---

Task:

Add two more paragraphs and try out, if the number of empty lines in between has an effect on the representation of the content.

# Lists

Bullet points in an unordered list indicated by starting *, -, or + and require indentation (2 spaces):

* A list always starts with the first bullet point
* A bullet point can consist of multiple parts.

  The only thing you will have to keep in mind is the correct indentation.

* A list can also contain further lists:

  + These do not necessarily have to start with an asterisks
  + But it is good practice if you use different symbols for different nesting

------------------------

Task:

Add some more bullet points the list, where you write down some comments your experiences with indentation.

# Numbered Lists

Markdown has also support for numbered lists, which can be used in combination with "unordered" lists.


1. First
2. Second
3. ...

------------------------

Task:

Write some useful comments on the usage of numbered lists
and create an example, where you combine numbered and not numbered bullet points.

# Formatting

Highlighting peaces of the text with only a text-editor might seem tricky at first.
But, you can use different elements to tag your content.

* `code`: this type is required if you want to highlight elements as code, the markdown interpreter will leave everything as it is (including Markdown syntax)

* italic: surround the word or the text with either `*` or  `_`.

* bold: think of two times as important as italic, thus it is surround by two `**` or `__`.

* bold and italic: how would you now try to define this and try out some nested combinations.

* Task: If you are using WhatsApp, you could write some messages with this formatting.
  WhatsApp has support for some pieces of markdown-syntax.

* crossed out: if you use `~` similarly to bold and italic, you will get a similar effect.

* underlined: ???

* crossed out and underlined: follow the markdown idea ;-)

* superscript: it is not Markdown but LiaScript, but you can use `^` to surround superscript elements

# Block-quotes

> If you want to highlight an entire text as important, then add a `> ` to the the beginning of every line.
> Early emails were an inspiration for this notation.
>
> **Within the following parts, we will use this syntax to mark tasks**

---

Question: Can blockquotes be nested?

# Links & References

Nothing within the Internet works without links. You can use them everywhere within the document, but Markdown has also support for named and internal links.

https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md#1

The syntax for named links is: `[name](url)`

> **Task 1:** Try to write the previous link as a named link.
>
> **Task 2:** Try to highlight your new link as bold.

---

Internal links follow a similar pattern, but instead of URLs you will have to reference the section title, starting with a hash-tag and with a title where spaces are replaced by dashes:

`#Title-Without-Spaces`

> **Task:** Create an internal link to the (Numbered lists) section.

# Images

Images are a special case of links, which you want to embed into your document and not only reference. Thus, these are important links, which are highlighted by a starting `!`.

> **Task 1:**  Change the link below to an image.
>
> Try to change the image URL and see the result.
>
> __Every part is important__

[Markdown logo](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)

---

> **Task 2:** Add a title to your link/image and see what happens --> `![alt-text](url "title")`
>
> Does markdown work too?

liatablediar


# Tables

Tables are self explaining as we hope. The first row is the head, the second one defines the orientation of the columns based on the position of the colons. And the rest is just data.


| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | 1600$ |
| col 2 is      | centered      |   12$ |
| zebra stripes | are neat      |    1$ |

> __Task:__ Add a space between the number and the dollar sign within the last row and checkout what happens.


## 2. LiaScript

### Multimedia

From links to ! images --> ? audio --> !? video --> ?? anything else:

* Audio: `?[alt-info](url)`
* Video: `!?[alt-info](url)`
* Anything else: `??[alt-info](url)`

> Task1: Embed the links below as audio content

[singing birds](https://bigsoundbank.com/UPLOAD/mp3/1068.mp3)

[soundcloud](https://soundcloud.com/glennmorrison/beethoven-moonlight-sonata)

> Task2: Go to youtube and add some video content

> Task3: Embed the content of the link below into your course


??[Piggy Bank](https://sketchfab.com/3d-models/horizontal-and-vertical-planing-machine-4cb50841dd6e42938b3bc098bff92423 "Horizontal and Vertical Planing Machine")

??[A circuit simulator](https://www.falstad.com/circuit/circuitjs.html)


### Galleries

> **Galleries are simply paragraphs with only multimedia content!**

![Portrait of a lady](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Leonardo_da_Vinci_%28attrib%29-_la_Belle_Ferroniere.jpg/723px-Leonardo_da_Vinci_%28attrib%29-_la_Belle_Ferroniere.jpg "La Belle Ferronnière, c. 1490–1498")


![Lady with an Ermine](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Lady_with_an_Ermine_-_Leonardo_da_Vinci_-_Google_Art_Project.jpg/761px-Lady_with_an_Ermine_-_Leonardo_da_Vinci_-_Google_Art_Project.jpg "Lady with an Ermine, c. 1489–1491, Czartoryski Museum, Kraków, Poland")


![Mona Lisa](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg/687px-Mona_Lisa%2C_by_Leonardo_da_Vinci%2C_from_C2RMF_retouched.jpg "Mona Lisa or La Gioconda c. 1503–1516, Louvre, Paris")


![Virgin and Child ](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Leonardo_da_Vinci_-_Virgin_and_Child_with_St_Anne_C2RMF_retouched.jpg/764px-Leonardo_da_Vinci_-_Virgin_and_Child_with_St_Anne_C2RMF_retouched.jpg "The Virgin and Child with Saint Anne, c. 1501–1519, Louvre, Paris")


![The Death of Leonardo da Vinci](https://upload.wikimedia.org/wikipedia/commons/thumb/8/8a/Francois_Ier_Leonard_de_Vinci-Jean_Auguste_Dominique_Ingres.jpg/1276px-Francois_Ier_Leonard_de_Vinci-Jean_Auguste_Dominique_Ingres.jpg "The Death of Leonardo da Vinci, by Ingres, 1818")

> **Task1:** Make a gallery
>
> **Task2:** Add some movies and other elements to the gallery.

### Quizzes `[[ ]]`

It is proven that students perform better, when they have the possibility to reflect.
Quizzes are an ideal way to check the understanding.
LiaScript currently has support for different types of quizzes, with the possibility to tweak them.

#### Text-input

A text input is simply a filed that follows after your question.
The solution is placed within a stylized input field.
In LiaScript quizzes are always associated with double brackets.

    `[[Solution]]`

> **Task:** Remove the backtics, change the solution and add your questions.

#### Selection

A selection is a quiz with multiple options separated by `|` and where the solution is put in parenthesis:

    `[[ This is not right | (**This is correct**) | This is another wrong option]]`

> **Task:** Remove the backtics, change the solution and add your questions.

##### Gap Text

Combining text inputs and selections:

The film that I saw [[(that)|those|these|then]] night wasn’t very good.
It was all [[ about ]] a man [[ who ]] built a
time machine so he [[ could ]] travel back in time.
It took him ages and ages [[ to ]] build the machine.

#### Single Choice

If you want to create a single choice quiz, for which commonly radio-buttons are used, would you use a similar syntax?

    [( )] No
    [(X)] <-- **YES of course**
    [( )] I would use H5P

> **Task:** Add some more options and try out, what happens, when multiple `X` are used.

#### Multiple Choice

If we stick to this metaphor, checkboxes can be defined with the following syntax:

    [[X]] <-- right
    [[ ]] wrong
    [[ ]] <-- right
    [[X]] wrong

> **Task:** Adapt the quiz above, such that the solution represents the defined options.
> Add and remove some Xs, see what happens when no X is defined.

#### Matrix

A matrix is basically a 2D representation multiple horizontal vectors.
The first row only defines the head of this quiz type.

    [ [head1] [ ;-) ] [ Option3 ] ]
    [   ( )     ( )       (X)     ]  <-- Single Choice
    [   [ ]     [X]       [X]     ]  <-- Multiple Choice

#### Tweaks

> You can use multiple tweaks when dealing with quizzes.
>
> 1. Hints
> 2. Solutions
> 3. Scripting

##### Hints

We stuck to the double brackets notation and simply include `?` to mark a hint.
Add as much hints to every quiz type.

What is the name of the Markdown dialect we are using?

    [[LiaScript]]
    [[?]] You have to use the correct writing
    [[?]] The solutions starts with Lia.....

> **Task:** Try to add some hints to other quizzes. 

##### Solutions

With the help of two horizontal lines, based on asterisk you can define a block that may contain a couple of different Markdown-blocks.
Solutions are only revealed, when the quiz is solved or when the user gives up.

---

What is the name of the Markdown dialect we are using?

    [[LiaScript]]
    [[?]] You have to use the correct writing
    [[?]] The solutions starts with Lia.....
    **************************************************
    
    LiaScript is an interactive extension to Markdown,
    which allows to develop free and open online course.
    More information can be found at:

    https://LiaScript.github.io

                    Just a diagram
    1.9 |
        |                 ***
      y |               *     *
      - | r r r r r r r*r r r r*r r r r r r r
      a |             *         *
      x |            *           *
      i | B B B B B * B B B B B B * B B B B B
      s |         *                 *
        |**  * *                       * *   *
     -1 +------------------------------------
        0              x-axis               1

    **************************************************

### Surveys

Surveys are basically the little sister of a quiz, the syntax is the same but instead of `X| ` you provide options:

Comma separated word-cloud:

[[___]]

---

Text inputs with multiple lines:

[[___ ___ ___]]

---

How do you rate LiaScript so far?

- [(poor)]      Not that good 
- [(ok)]        It is okay, but I expected more
- [(good)]      I like the approach
- [(excellent)] Extremely good... 


---

What are your favorite colors?

- [[red]] red
- [[blue]] blue
- [[green]] green
- [[yellow]] yellow
- [[something else]] other colors are fine too

### Animations & Presentations


> Your user can decide, which presentation mode is used.
> We currently support Textbook, Slides, and Presentation.

You can use these curly braces to let blocks appear and disappear.
Simply add these points the the beginning of your block.

* fade-in: `{{2}}`
* fade-in and out: `{{1-3}}`

> **Task:** Add some animations to the content below.

Let me appear at first.
And disappear at step 2.

| let    | me        |
| :----- | :-------- |
| appear | at step 2 |

> As the the last and final quote.
> I wanted to be displayed at the very end.

#### Text to Speech


The currently used default language is `UK English Female`.
LiaScript uses the browser TTS-API and as a fallback responsive:

https://responsivevoice.org 

You can use more voices, simply by typing "voice".


With this notation `--{{1}}--` you can add some more explanation that will be spoken out loud to animation-step 1.
You can also change the voice for per comment `--{{2 US English Male}}--`.

> **Task:** Add some comment tags to the head of the paragraphs below and change their voices.
> 
> Try to add some examples of your mother tongue.

The entire ***Markdown*** paragraph right below the effect definition in double minus notation is sent to responsivevoice to speak the text out loud.
If you click on the ear button at the navigation panel, then this paragraph gets rendered at the place where it is defined.

Der Ganze Satz sollte deutsch ausgesprochen werden!

#### Combine Animations and TTS

> __Task:__ Create some examples by your own, where you combine the animation steps with the spoken output ...
