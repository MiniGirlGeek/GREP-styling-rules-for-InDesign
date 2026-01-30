<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />All the work in this repository is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

# GREP Styling Rules for InDesign
Making InDesign do things it probably wasn't designed to do. These GREP styling rules allow you to have python syntax highlighting as a paragraph style. 

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
