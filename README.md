# Curriculum Vitae as a Postcript Quine

Why write your CV in a word processor or generate it with a markup language if you could just have the real deal and write a Postscript file that parses and displays itself, as a [quine](https://en.wikipedia.org/wiki/Quine_(computing))?

`ps.cv` is a Postscript file that does exactly this. It parses the CV at the beginning of the file, renders it in a way that copying and pasting the contents from the displayed file retains all the markup information and adds a footer with all the roughly 100 lines of Postscript code necessary to parse the markup and display itself.

## Example CV

The Postscript file in this repository contains the CV of the fictional author [Herbert Quine](https://en.wikipedia.org/wiki/An_Examination_of_the_Work_of_Herbert_Quain). The file [cv.ps](cv.ps) displayed as a PDF looks like [cv.pdf](cv.pdf) and is based on the following CV markup (with the formatting being arbitrary, all the newlines and multiple spaces could be replaced with a single space each):

```
    ~ Herbert
    ~ Quine
- email@example.com, github.com/fkettelhoit
- Roscommon, Ireland

    ~ About Me

/ Writer of experimental fiction
- I am like Cowley's odes, I belong not to art but to the history of art
- I deploy the servile, stubborn preservation of past and bygone books
- There is no European man or woman that's not a writer, potentially or in fact

    ~ Publications

/ Statements (1939)
- 8 stories, each prefiguring a good plot
- Each plot is then intentionally frustrated by the author

/ The Secret Mirror (1937)
- Two-act comedy, with the first act as the work of a character in the second act
- First act takes place in the country home of General Thrale
- Characters of the first act reappear in the second, under different names

/ April March (1936)
- Novel with nine different beginnings, trifurcating backwards in time
- "Regressive, ramifying fiction"
- "I have reclaimed for this novel the essential features of every game"

/ The God of the Labyrinth (1933)
- Detective story in which the solution given is wrong
- But this fact is not immediately obvious
- Incomprehensible murder in the early pages of the book
- Slow discussion in the middle
- Solution of the crime toward the end
- "Everyone believed that the chessplayer had met accidentally."

    ~ About this CV

/ A Postscript quine & markup parser
- This Postscript file is a quine, including and displaying its own code
- Copy all the text on this page, then paste it in a new file with a .ps extension
- The resulting .ps file will display the same CV with all of the code
- The CV is parsed as a whitespace-insensitive custom markup language
- Newlines and other whitespace can be used interchangeably
- The data for the CV is fully contained in the displayed CV
- The footer only contains the non-CV code
```

The above CV will be displayed as the following [PDF](cv.pdf):

<img width="521" alt="CV output as PDF" src="https://user-images.githubusercontent.com/358580/127316278-5a636b21-d5c7-4719-9494-62233cb62391.png">
