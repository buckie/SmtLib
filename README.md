# SmtLib
SMTLib2 parsers.

A library with SMTLib2 syntax and parsers for commands and their responses.

How to parse a smtlib2 file:
```Haskell
import SmtLib.Parsers.CommandsParsers
import SmtLib.Syntax.Syntax
import Text.ParserCombinators.Parsec

parseFile :: FilePath -> IO (Either ParseError Source)
parseFile x = parse parseSource "" <$> readFile x
```
