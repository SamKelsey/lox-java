This is Lox, a language taken curated in the book "Crafting interpreters".

The Lox Grammar is as follows:

```markdown
expression  &rarr; ternary ;                                                                |   Lowest
ternary     &rarr; ( expression "?" expression ":" expression ) | equality ;               |      &darr;
equality    &rarr; comparison ( ( "!=" | "==" ) comparison )* ;                              |      &uarr;
comparison  &rarr; term ( ( ">" | ">=" | "<" | "<=" ) term )* ;                              |           
term        &rarr; factor ( ( "-" | "+" ) factor )* ;                                        |  Precedence
factor      &rarr; unary ( ( "/" | "*" ) unary )* ;                                          |      
unary       &rarr; ( "!" | "-" ) unary | primary ;                                           |
primary     &rarr; NUMBER | STRING | "true" | "false" | "nil" | "(" expression ")" ;         |   Highest
```

