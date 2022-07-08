# STLC Parser

An implementation of parsing for a Simply TypeTerm Lambda Calculus (STLC) grammar:

```

Expr ::= Const | Variable | Abstr | Appl | Cond

Const    ::= unit | true | false | <numeral> | add | mul | or | and
Variable ::= Var | "(" Var ")"
Abstr    ::= "\" VarAnn "." Expr | "(" "\" VarAnn "." Expr ")"
Appl     ::= "(" Expr "$" Args ")"
Cond     ::= "(" Expr "?" Expr "::" Expr ")"

Args ::= Term | Term "$" Args

Term ::= Expr | TypeTag "=" Expr

Var    ::= <lowercase>
VarAnn ::= Var ":" TypeTerm

TypeTerm ::= TypeExpr | TypeTag "'" TypeExpr

TypeTag ::= <lowercase>

TypeExpr ::= TypeConst | TypeVar | TypeFunction

TypeConst    ::= Unit | Bool | Int
TypeVar      ::= <capitalized>
TypeFunction ::= "(" Froms "->" TypeExpr ")"

Froms ::= TypeTerm | TypeTerm "->" Froms
```

(Whitespace is entirely ignored)
