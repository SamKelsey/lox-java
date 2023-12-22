This is Lox, a language taken curated in the book "Crafting interpreters".

The Lox Grammar is as follows:

```markdown
expression  &rarr; ternary ;                                                                 |   Lowest
ternary     &rarr; equality ( "?" equality ":" equality )* ;                       |      &uarr;
equality    &rarr; comparison ( ( "!=" | "==" ) comparison )* ;                              |
comparison  &rarr; term ( ( ">" | ">=" | "<" | "<=" ) term )* ;                              |  Precedence         
term        &rarr; factor ( ( "-" | "+" ) factor )* ;                                        |  
factor      &rarr; unary ( ( "/" | "*" ) unary )* ;                                          |      
unary       &rarr; ( "!" | "-" ) unary | primary ;                                           |      &darr;
primary     &rarr; NUMBER | STRING | "true" | "false" | "nil" | "(" expression ")" ;         |   Highest
```

