# GREP Styling Rules for InDesign
Making InDesign to things it probably wasn't designed to do.

I found this GREP cheat sheet very useful: [http://www.ericagamet.com/wp-content/uploads/2016/04/Erica-Gamets-GREP-Cheat-Sheet.pdf](http://www.ericagamet.com/wp-content/uploads/2016/04/Erica-Gamets-GREP-Cheat-Sheet.pdf)

## GREP rules for Python syntax highlighting
Inspired by the answer to this stack exchange question: [https://graphicdesign.stackexchange.com/questions/6996/indesign-and-syntax-highlighting](https://graphicdesign.stackexchange.com/questions/6996/indesign-and-syntax-highlighting)

*Please note that the order of the rules is important, becuase some have priority over others, particularly the comma rule!*

You can either type things into the GREP section of a paragraph style, or copy and paste the text box from the .indd file in this repository.

Keyword Agument - `(\w*)(?=\=)`

Parameter - `(def \w*\()\K(.|)(?=\))`

String - `("|').("|')`

Commas - `,`

Numbers - `(?<!\w)\d+`

Keywords - `(?<!\w)(try|continue|for|finally|is|return|from|nonlocal|while|and|del|global|not|with|as|elif|if|or|yield|assert|else|import|pass|break|except|in|raise)(?!\w)`

Operators - `\=|\+|\-|\/|\*`

Boolean - `True|False|None`

Comment - `(#.*|("""|''').*("""|'''))`

Defining - `(def|class|lambda)(?!\w)`

Defined name - `\w+?(?=\()`

Definition name - `(def|class) \K\w*`
