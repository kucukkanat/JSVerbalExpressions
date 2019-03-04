Whole methods should "quote" value expecting "add". Use regex method to quote if your language gives it. If not, you must find a way to quote values before to be added in compilable expression.

Those methods should be implemented:
## add
Append a transformed value to internal expression that will be compiled.

As possible, this method should be "private".

## startOfLine

append "^" at start of expression

## endOfLine 
append "$" at end of expression

## find

    "(?:" + value + ")"

## then (shorthand for find)

see "find" method

## maybe

0 or 1 times

    "(?:" + value + ")?"

## anything
Matches everything

    (?:.*)

## anythingBut
Matches everything excepting letter in given value

    "(?:[^" + value + "]*)"

## something
Matches at least one char

    (?:.+)

## somethingBut
Matches at least one char not in value

    "(?:[^" + value + "]+)"

## replace
Return replaced string

## lineBreak
Matches any linebreak

    "(?:(?:\n)|(?:\r\n))"

## br (shorthand for lineBreak)
see lineBreak

## tab
Should match tab char

    "\t"

## word
Matches at least one word

     "\w+"

## anyOf
Matches any char in value

     "(?:[" + value + "])"

## any (shorthand for anyOf)
see AnyOf

## range
To be discuss

## withAnyCase
Append modifier "i"

## stopAtFirst
Remove modifier "g" if "true", else append modifier "g"

## searchOneLine
If true, remove modifier "m"

## multiple
to be discuss => issue #2

## or
Split expression with "|", to be discuss

## beginCapture
Initiate capture

## endCapture
Stop capturing elements

## whitespace
Matches whitespace `\\s`.

## oneOrMore
Repeats the previous at least once.
