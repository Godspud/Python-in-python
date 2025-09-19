# Python-in-python

# to do
1. Built-ins

 Implement all Python built-in functions:

I/O: print(), input()

Type constructors: int(), str(), list(), dict(), tuple(), set(), frozenset(), float(), bool(), complex(), range()

Iterables: enumerate(), zip(), reversed(), iter(), next()

Logic / math: all(), any(), sum(), min(), max(), abs(), divmod(), pow(), round()

Reflection: id(), type(), callable(), getattr(), setattr(), hasattr(), delattr(), isinstance(), issubclass(), dir(), globals(), locals(), vars()

Execution: eval(), exec(), compile()

 Implement all standard exception classes internally

 No use of __import__ or external modules

2. Environment / Scope

 Implement Environment class

 Store variables, functions, classes

 Handle nested scopes (local/global)

 Provide lookup(name), assign(name, value), push_scope(), pop_scope()

 Keep single global environment for the file

3. AST Nodes

 Implement ASTNode base class with eval(env)

 Implement all node types:

Expressions: Number, String, Variable, BinaryOp, UnaryOp, Call

Statements: Assign, If, While, For, Break, Continue, Return

Functions: FunctionDef

Classes: ClassDef, Attribute, MethodCall

Exceptions: Raise, TryExcept, Finally

 No separate module AST nodes (multi-file handled internally in single file)

4. Lexer

 Implement Lexer class

 Tokenize Python keywords, identifiers, literals, operators, punctuation

 Handle indentation / dedentation

 Handle strings, numbers, comments

 Provide next_token() and peek_token()

5. Parser

 Implement Parser class

 Convert tokens to AST nodes

 Grammar rules for:

Expressions (+, -, *, /, logical, comparisons)

Statements (if, while, for, break, continue, return)

Functions (def, parameters, return)

Classes (class, methods, __init__)

Exception handling (try/except/finally, raise)

 Each parser method returns ASTNode objects

6. Interpreter / Evaluator

 Implement Interpreter class

 Execute AST nodes via eval(env)

 Handle:

Expressions and arithmetic

Statements and control flow

Function calls

Class instantiation

Exception handling

 Use single global environment and built-ins

7. Module / Multi-File Support (Internal Only)

 Since imports are disabled:

 Implement a module registry inside the file: module_name -> code string

 Allow referencing other “modules” in the same file

 Execute module code in its own environment

 Link top-level definitions to the main environment if needed
