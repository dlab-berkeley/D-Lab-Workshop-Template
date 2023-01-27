# General style for Jupyter Notebooks


## Markdown

- Keep narrative text limited!
- Avoid discussion of edge cases or caveats.
- Use colloquial languague and minimal jargon; if you need it, explain it.
- Use **boldface** to highlight key concepts and important terms, but use it sparingly.
- Don't use italics.
- Use en-dash for lists.
- Use `code font` for anything in code like variables, functions, and packages.
- Use `cont font` for menu items (like `Restart Kernel`), and data frame rows/columns.
- When discussing functions, include the trailing parentheses (e.g. `print()`).
- When discussing methods, include the dot (e.g. `.sum()`).
- Consistently use emoji for relevant sections. See below for some examples.


## Python style

We follow [PEP](https://peps.python.org/pep-0008). This guide summarizes some of what's in there.


### Indentation

```
# Correct:

# Aligned with opening delimiter.
foo = long_function_name(var_one, var_two,
                         var_three, var_four)

# Add 4 spaces (an extra level of indentation) to distinguish arguments from the rest.
def long_function_name(
        var_one, var_two, var_three,
        var_four):
    print(var_one)

# Hanging indents should add a level.
foo = long_function_name(
    var_one, var_two,
    var_three, var_four)
```

### Imports

Imports are always put at the top of the cell. Imports should usually be on separate lines:

```
# Correct:
import os
import sys
# Wrong:
import sys, os
```


### Strings

In Python, single-quoted strings and double-quoted strings are the same. We do
not make a recommendation for this. Pick a rule and stick to it. When a string
contains single or double quote characters, however, use the other one to avoid
backslashes in the string. It improves readability.


### Whitespace

Avoid extraneous whitespace in the following situations:

- Immediately inside parentheses, brackets or braces:

```
# Correct:
spam(ham[1], {eggs: 2})
# Wrong:
spam( ham[ 1 ], { eggs: 2 } )
```

- Between a trailing comma and a following close parenthesis:

```
# Correct:
foo = (0,)
# Wrong:
bar = (0, )
```

- Immediately before a comma, semicolon, or colon:

```
# Correct:
if x == 4: print(x, y); x, y = y, x
# Wrong:
if x == 4 : print(x , y) ; x , y = y , x
```

Always surround these binary operators with a single space on either side:
assignment (=), augmented assignment (+=, -= etc.), comparisons
(==, <, >, !=, <>, <=, >=, in, not in, is, is not), Booleans (and, or, not).


### Comments

Comments that contradict the code are worse than no comments. Always make a
priority of keeping the comments up-to-date when the code changes!

Comments should be complete sentences. The first word should be capitalized,
unless it is an identifier that begins with a lower case letter (never alter
the case of identifiers!).

Block comments generally consist of one or more paragraphs built out of complete
sentences, with each sentence ending in a period.

Don't use inline comments.
