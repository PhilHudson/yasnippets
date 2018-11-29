# yasnippets
# Phil Hudson's custom yasnippet snippets.

## Smart, cool snippets (I hope)
These snippets make use of a lot of tab-navigation placeholders containing smaller nested placeholders, wherever there's something optional that you might not want to have to fill in. The idea is, if you don't need the optional things (for instance the optional arguments to `autoload`) you just hit `C-d` to remove (in this case) both of them, otherwise you tab again to get "inside" the group and edit the first one -- in this case, presumably, to specify `'interactive`.

Easier to demo than explain:

    (autoload #'FUNCTION FILE &optional "DOCSTRING" INTERACTIVE TYPE)

has the following tab-navigation placeholders, which you can just tab to and type to replace:

1. `FUNCTION`
2. `FILE`

then:

3. Everything after `FILE`, including the space character before `&optional`. Tab to this and hit `C-d` if you want to just remove all the optional stuff (the most common use case).
4. Alternatively, tab "in" to select "` &optional`", and hit `C-d` to delete it, then tab again to select `"DOCSTRING"` (including the quotes).
5. Now, either type `nil` to replace `"DOCSTRING"`, meaning no documentation string is specified, or tab "in" to select `DOCSTRING` (without the quotes) and type your documentation string.
6. Tab again. Again, you can now delete the remaining parameters with `C-d`. Or tab "in" to select `INTERACTIVE`. Choose from the interactive menu, in this case offering you the choice of `nil` or `'interactive`.
7. Tab again. Again, you can delete the last parameter with C-d. Or tab "in" to select `TYPE` and choose from the interactive menu offering you `nil`, `'keymap`, or `'macro`.

## Idiosyncratic Elisp formatting
I use C-style outdenting. That's right: closing parens on their own lines. Block structuring, visually represented. The [AST](https://en.wikipedia.org/wiki/Abstract_syntax_tree "Abstract syntax tree"), visually represented. [Sexp](https://en.wikipedia.org/wiki/S-expression "Symbolic expression") nesting, visually represented. The right way, I claim. Making the most of the visual real estate available on a great big portrait display, which I highly recommend to any serious coder.

If you hate it, I understand. Why not fork this repo? If you do, please keep me posted, and I'll link to you.

## Pull requests
All other PRs *very* gratefully received.
