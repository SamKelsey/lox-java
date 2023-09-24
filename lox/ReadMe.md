This is Lox, a language taken curated in the book "Crafting interpreters".

The Lox Grammar is as follows:

```markdown
expression  &rarr; equality ;
equality    &rarr; comparison ( ( "!=" | "==" ) comparison )* ;
comparison  &rarr; term ( ( ">" | ">=" | "<" | "<=" ) term )* ;
term        &rarr; factor ( ( "-" | "+" ) factor )* ;
factor      &rarr; unary ( ( "/" | "*" ) unary )* ;
unary       &rarr; ( "!" | "-" ) unary | primary ;
primary     &rarr; NUMBER | STRING | "true" | "false" | "nil" | "(" expression ")" ;
```