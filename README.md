# STLC Parser

An implementation of parsing for a Simply Type Lambda Calculus (STLC) grammar:

```
Expr ::= Const | Variable | Abstr | Appl | Cond

Const    ::= unit | true | false | <numeral> | add | mul | or | and
Variable ::= Var | '(' Var ')'
Abstr    ::= '\' VarAnn '.' Expr | '(' '\' VarAnn '.' Expr ')'
Appl     ::= '(' Expr '$' Expr ')'
Cond     ::= '(' Expr '?' Expr '::' Expr ')'

Var    ::= <lowercase>
VarAnn ::= Var : Type

Type ::= TypeTag '~' TypeExpr | TypeExpr

TypeTag ::= '\'' <lowercase>

TypeExpr ::= TypeConst | TypeVar | TypeFunction

TypeConst    ::= Unit | Bool | Int
TypeVar      ::= <capitalized>
TypeFunction ::= '(' Type '->' Type ')'
```

(Whitespace is entirely ignored)
