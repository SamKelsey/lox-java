This is Lox, a language taken curated in the book "Crafting interpreters".

The Lox Grammar is as follows:

```markdown
expression  &rarr; equality ;                                                                |   Lowest
equality    &rarr; comparison ( ( "!=" | "==" ) comparison )* ;                              |      &uarr;
comparison  &rarr; term ( ( ">" | ">=" | "<" | "<=" ) term )* ;                              |           
term        &rarr; factor ( ( "-" | "+" ) factor )* ;                                        |  Precedence
factor      &rarr; unary ( ( "/" | "*" ) unary )* ;                                          |      
unary       &rarr; ( "!" | "-" ) unary | primary ;                                           |      &darr;
primary     &rarr; NUMBER | STRING | "true" | "false" | "nil" | "(" expression ")" ;         |   Highest
```

