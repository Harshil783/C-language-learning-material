# The GNU C Reference Manual

- [The GNU C Reference Manual](#the-gnu-c-reference-manual)
  - [Table of Contents](#table-of-contents)
- [The GNU C Reference Manual](#the-gnu-c-reference-manual-1)
  - [Preface](#preface)
    - [Credits](#credits)
  - [1 Lexical Elements](#lexical-elements)
    - [1.1 Identifiers](#identifiers)
    - [1.2 Keywords](#keywords)
    - [1.3 Constants](#constants)
    - [1.4 Operators](#operators)
    - [1.5 Separators](#separators)
    - [1.6 White Space](#white-space)
  - [2 Data Types](#data-types)
    - [2.1 Primitive Data Types](#primitive-data-types)
    - [2.2 Enumerations](#enumerations)
    - [2.3 Unions](#unions)
    - [2.4 Structures](#structures)
    - [2.5 Arrays](#arrays)
    - [2.6 Pointers](#pointers)
    - [2.7 Incomplete Types](#incomplete-types)
    - [2.8 Type Qualifiers](#type-qualifiers)
    - [2.9 Storage Class Specifiers](#storage-class-specifiers)
    - [2.10 Renaming Types](#renaming-types)
  - [3 Expressions and Operators](#expressions-and-operators)
    - [3.1 Expressions](#expressions)
    - [3.2 Assignment Operators](#assignment-operators)
    - [3.3 Incrementing and
      Decrementing](#incrementing-and-decrementing)
    - [3.4 Arithmetic Operators](#arithmetic-operators)
    - [3.5 Complex Conjugation](#complex-conjugation)
    - [3.6 Comparison Operators](#comparison-operators)
    - [3.7 Logical Operators](#logical-operators)
    - [3.8 Bit Shifting](#bit-shifting)
    - [3.9 Bitwise Logical Operators](#bitwise-logical-operators)
    - [3.10 Pointer Operators](#pointer-operators)
    - [3.11 The sizeof Operator](#the-sizeof-operator)
    - [3.12 Type Casts](#type-casts)
    - [3.13 Array Subscripts](#array-subscripts)
    - [3.14 Function Calls as
      Expressions](#function-calls-as-expressions)
    - [3.15 The Comma Operator](#the-comma-operator)
    - [3.16 Member Access Expressions](#member-access-expressions)
    - [3.17 Conditional Expressions](#conditional-expressions)
    - [3.18 Statements and Declarations in
      Expressions](#statements-and-declarations-in-expressions)
    - [3.19 Operator Precedence](#operator-precedence)
    - [3.20 Order of Evaluation](#order-of-evaluation)
  - [4 Statements](#statements)
    - [4.1 Labels](#labels)
    - [4.2 Expression Statements](#expression-statements)
    - [4.3 The `if` Statement](#the-if-statement)
    - [4.4 The `switch` Statement](#the-switch-statement)
    - [4.5 The `while` Statement](#the-while-statement)
    - [4.6 The `do` Statement](#the-do-statement)
    - [4.7 The `for` Statement](#the-for-statement)
    - [4.8 Blocks](#blocks)
    - [4.9 The Null Statement](#the-null-statement)
    - [4.10 The `goto` Statement](#the-goto-statement)
    - [4.11 The `break` Statement](#the-break-statement)
    - [4.12 The `continue` Statement](#the-continue-statement)
    - [4.13 The `return` Statement](#the-return-statement)
    - [4.14 The `typedef` Statement](#the-typedef-statement)
  - [5 Functions](#functions)
    - [5.1 Function Declarations](#function-declarations)
    - [5.2 Function Definitions](#function-definitions)
    - [5.3 Calling Functions](#calling-functions)
    - [5.4 Function Parameters](#function-parameters)
    - [5.5 Variable Length Parameter
      Lists](#variable-length-parameter-lists)
    - [5.6 Calling Functions Through Function
      Pointers](#calling-functions-through-function-pointers)
    - [5.7 The `main` Function](#the-main-function)
    - [5.8 Recursive Functions](#recursive-functions)
    - [5.9 Static Functions](#static-functions)
    - [5.10 Nested Functions](#nested-functions)
  - [6 Program Structure and Scope](#program-structure-and-scope)
    - [6.1 Program Structure](#program-structure)
    - [6.2 Scope](#scope)
  - [7 A Sample Program](#a-sample-program)
    - [7.1 `hello.c`](#hello.c)
    - [7.2 `system.h`](#system.h)
  - [Appendix A Overflow](#appendix-a-overflow)
    - [A.1 Basics of Integer Overflow](#a.1-basics-of-integer-overflow)
    - [A.2 Examples of Code Assuming Wraparound
      Overflow](#a.2-examples-of-code-assuming-wraparound-overflow)
    - [A.3 Optimizations That Break Wraparound
      Arithmetic](#a.3-optimizations-that-break-wraparound-arithmetic)
    - [A.4 Practical Advice for Signed Overflow
      Issues](#a.4-practical-advice-for-signed-overflow-issues)
    - [A.5 Signed Integer Division and Integer
      Overflow](#a.5-signed-integer-division-and-integer-overflow)
  - [GNU Free Documentation License](#gnu-free-documentation-license)
    - [ADDENDUM: How to use this License for your
      documents](#addendum-how-to-use-this-license-for-your-documents)
  - [Index](#index)

# The GNU C Reference Manual

<span id="SEC_Contents"></span>

## Table of Contents

<div class="contents">

- <a href="#Preface" id="toc-Preface-1">Preface</a>
  - <a href="#Credits" id="toc-Credits">Credits</a>
- <a href="#Lexical-Elements" id="toc-Lexical-Elements-1">1 Lexical
  Elements</a>
  - <a href="#Identifiers" id="toc-Identifiers-1">1.1 Identifiers</a>
  - <a href="#Keywords" id="toc-Keywords-1">1.2 Keywords</a>
  - <a href="#Constants" id="toc-Constants-1">1.3 Constants</a>
    - <a href="#Integer-Constants" id="toc-Integer-Constants-1">1.3.1 Integer
      Constants</a>
    - <a href="#Character-Constants" id="toc-Character-Constants-1">1.3.2
      Character Constants</a>
    - <a href="#Real-Number-Constants" id="toc-Real-Number-Constants-1">1.3.3
      Real Number Constants</a>
    - <a href="#String-Constants" id="toc-String-Constants-1">1.3.4 String
      Constants</a>
  - <a href="#Operators" id="toc-Operators-1">1.4 Operators</a>
  - <a href="#Separators" id="toc-Separators-1">1.5 Separators</a>
  - <a href="#White-Space" id="toc-White-Space-1">1.6 White Space</a>
- <a href="#Data-Types" id="toc-Data-Types-1">2 Data Types</a>
  - <a href="#Primitive-Types" id="toc-Primitive-Data-Types">2.1 Primitive
    Data Types</a>
    - <a href="#Integer-Types" id="toc-Integer-Types-1">2.1.1 Integer
      Types</a>
    - <a href="#Real-Number-Types" id="toc-Real-Number-Types-1">2.1.2 Real
      Number Types</a>
    - <a href="#Complex-Number-Types" id="toc-Complex-Number-Types-1">2.1.3
      Complex Number Types</a>
      - <a href="#Standard-Complex-Number-Types"
        id="toc-Standard-Complex-Number-Types-1">2.1.3.1 Standard Complex Number
        Types</a>
      - <a href="#GNU-Extensions-for-Complex-Number-Types"
        id="toc-GNU-Extensions-for-Complex-Number-Types-1">2.1.3.2 GNU
        Extensions for Complex Number Types</a>
  - <a href="#Enumerations" id="toc-Enumerations-1">2.2 Enumerations</a>
    - <a href="#Defining-Enumerations" id="toc-Defining-Enumerations-1">2.2.1
      Defining Enumerations</a>
    - <a href="#Declaring-Enumerations"
      id="toc-Declaring-Enumerations-1">2.2.2 Declaring Enumerations</a>
  - <a href="#Unions" id="toc-Unions-1">2.3 Unions</a>
    - <a href="#Defining-Unions" id="toc-Defining-Unions-1">2.3.1 Defining
      Unions</a>
    - <a href="#Declaring-Union-Variables"
      id="toc-Declaring-Union-Variables-1">2.3.2 Declaring Union Variables</a>
      - <a href="#Declaring-Union-Variables-at-Definition"
        id="toc-Declaring-Union-Variables-at-Definition-1">2.3.2.1 Declaring
        Union Variables at Definition</a>
      - <a href="#Declaring-Union-Variables-After-Definition"
        id="toc-Declaring-Union-Variables-After-Definition-1">2.3.2.2 Declaring
        Union Variables After Definition</a>
      - <a href="#Initializing-Union-Members"
        id="toc-Initializing-Union-Members-1">2.3.2.3 Initializing Union
        Members</a>
    - <a href="#Accessing-Union-Members"
      id="toc-Accessing-Union-Members-1">2.3.3 Accessing Union Members</a>
    - <a href="#Size-of-Unions" id="toc-Size-of-Unions-1">2.3.4 Size of
      Unions</a>
  - <a href="#Structures" id="toc-Structures-1">2.4 Structures</a>
    - <a href="#Defining-Structures" id="toc-Defining-Structures-1">2.4.1
      Defining Structures</a>
    - <a href="#Declaring-Structure-Variables"
      id="toc-Declaring-Structure-Variables-1">2.4.2 Declaring Structure
      Variables</a>
      - <a href="#Declaring-Structure-Variables-at-Definition"
        id="toc-Declaring-Structure-Variables-at-Definition-1">2.4.2.1 Declaring
        Structure Variables at Definition</a>
      - <a href="#Declaring-Structure-Variables-After-Definition"
        id="toc-Declaring-Structure-Variables-After-Definition-1">2.4.2.2
        Declaring Structure Variables After Definition</a>
      - <a href="#Initializing-Structure-Members"
        id="toc-Initializing-Structure-Members-1">2.4.2.3 Initializing Structure
        Members</a>
    - <a href="#Accessing-Structure-Members"
      id="toc-Accessing-Structure-Members-1">2.4.3 Accessing Structure
      Members</a>
    - <a href="#Bit-Fields" id="toc-Bit-Fields-1">2.4.4 Bit Fields</a>
    - <a href="#Size-of-Structures" id="toc-Size-of-Structures-1">2.4.5 Size
      of Structures</a>
  - <a href="#Arrays" id="toc-Arrays-1">2.5 Arrays</a>
    - <a href="#Declaring-Arrays" id="toc-Declaring-Arrays-1">2.5.1 Declaring
      Arrays</a>
    - <a href="#Initializing-Arrays" id="toc-Initializing-Arrays-1">2.5.2
      Initializing Arrays</a>
    - <a href="#Accessing-Array-Elements"
      id="toc-Accessing-Array-Elements-1">2.5.3 Accessing Array Elements</a>
    - <a href="#Multidimensional-Arrays"
      id="toc-Multidimensional-Arrays-1">2.5.4 Multidimensional Arrays</a>
    - <a href="#Arrays-as-Strings" id="toc-Arrays-as-Strings-1">2.5.5 Arrays
      as Strings</a>
    - <a href="#Arrays-of-Unions" id="toc-Arrays-of-Unions-1">2.5.6 Arrays of
      Unions</a>
    - <a href="#Arrays-of-Structures" id="toc-Arrays-of-Structures-1">2.5.7
      Arrays of Structures</a>
  - <a href="#Pointers" id="toc-Pointers-1">2.6 Pointers</a>
    - <a href="#Declaring-Pointers" id="toc-Declaring-Pointers-1">2.6.1
      Declaring Pointers</a>
    - <a href="#Initializing-Pointers" id="toc-Initializing-Pointers-1">2.6.2
      Initializing Pointers</a>
    - <a href="#Pointers-to-Unions" id="toc-Pointers-to-Unions-1">2.6.3
      Pointers to Unions</a>
    - <a href="#Pointers-to-Structures"
      id="toc-Pointers-to-Structures-1">2.6.4 Pointers to Structures</a>
  - <a href="#Incomplete-Types" id="toc-Incomplete-Types-1">2.7 Incomplete
    Types</a>
  - <a href="#Type-Qualifiers" id="toc-Type-Qualifiers-1">2.8 Type
    Qualifiers</a>
  - <a href="#Storage-Class-Specifiers"
    id="toc-Storage-Class-Specifiers-1">2.9 Storage Class Specifiers</a>
  - <a href="#Renaming-Types" id="toc-Renaming-Types-1">2.10 Renaming
    Types</a>
- <a href="#Expressions-and-Operators"
  id="toc-Expressions-and-Operators-1">3 Expressions and Operators</a>
  - <a href="#Expressions" id="toc-Expressions-1">3.1 Expressions</a>
  - <a href="#Assignment-Operators" id="toc-Assignment-Operators-1">3.2
    Assignment Operators</a>
  - <a href="#Incrementing-and-Decrementing"
    id="toc-Incrementing-and-Decrementing-1">3.3 Incrementing and
    Decrementing</a>
  - <a href="#Arithmetic-Operators" id="toc-Arithmetic-Operators-1">3.4
    Arithmetic Operators</a>
  - <a href="#Complex-Conjugation" id="toc-Complex-Conjugation-1">3.5
    Complex Conjugation</a>
  - <a href="#Comparison-Operators" id="toc-Comparison-Operators-1">3.6
    Comparison Operators</a>
  - <a href="#Logical-Operators" id="toc-Logical-Operators-1">3.7 Logical
    Operators</a>
  - <a href="#Bit-Shifting" id="toc-Bit-Shifting-1">3.8 Bit Shifting</a>
  - <a href="#Bitwise-Logical-Operators"
    id="toc-Bitwise-Logical-Operators-1">3.9 Bitwise Logical Operators</a>
  - <a href="#Pointer-Operators" id="toc-Pointer-Operators-1">3.10 Pointer
    Operators</a>
  - <a href="#The-sizeof-Operator" id="toc-The-sizeof-Operator-1">3.11 The
    sizeof Operator</a>
  - <a href="#Type-Casts" id="toc-Type-Casts-1">3.12 Type Casts</a>
  - <a href="#Array-Subscripts" id="toc-Array-Subscripts-1">3.13 Array
    Subscripts</a>
  - <a href="#Function-Calls-as-Expressions"
    id="toc-Function-Calls-as-Expressions-1">3.14 Function Calls as
    Expressions</a>
  - <a href="#The-Comma-Operator" id="toc-The-Comma-Operator-1">3.15 The
    Comma Operator</a>
  - <a href="#Member-Access-Expressions"
    id="toc-Member-Access-Expressions-1">3.16 Member Access Expressions</a>
  - <a href="#Conditional-Expressions"
    id="toc-Conditional-Expressions-1">3.17 Conditional Expressions</a>
  - <a href="#Statements-and-Declarations-in-Expressions"
    id="toc-Statements-and-Declarations-in-Expressions-1">3.18 Statements
    and Declarations in Expressions</a>
  - <a href="#Operator-Precedence" id="toc-Operator-Precedence-1">3.19
    Operator Precedence</a>
  - <a href="#Order-of-Evaluation" id="toc-Order-of-Evaluation-1">3.20 Order
    of Evaluation</a>
    - <a href="#Side-Effects" id="toc-Side-Effects-1">3.20.1 Side Effects</a>
    - <a href="#Sequence-Points" id="toc-Sequence-Points-1">3.20.2 Sequence
      Points</a>
    - <a href="#Sequence-Points-Constrain-Expressions"
      id="toc-Sequence-Points-Constrain-Expressions-1">3.20.3 Sequence Points
      Constrain Expressions</a>
    - <a href="#Sequence-Points-and-Signal-Delivery"
      id="toc-Sequence-Points-and-Signal-Delivery-1">3.20.4 Sequence Points
      and Signal Delivery</a>
- <a href="#Statements" id="toc-Statements-1">4 Statements</a>
  - <a href="#Labels" id="toc-Labels-1">4.1 Labels</a>
  - <a href="#Expression-Statements" id="toc-Expression-Statements-1">4.2
    Expression Statements</a>
  - <a href="#The-if-Statement" id="toc-The-if-Statement-1">4.3 The
    <code>if</code> Statement</a>
  - <a href="#The-switch-Statement" id="toc-The-switch-Statement-1">4.4 The
    <code>switch</code> Statement</a>
  - <a href="#The-while-Statement" id="toc-The-while-Statement-1">4.5 The
    <code>while</code> Statement</a>
  - <a href="#The-do-Statement" id="toc-The-do-Statement-1">4.6 The
    <code>do</code> Statement</a>
  - <a href="#The-for-Statement" id="toc-The-for-Statement-1">4.7 The
    <code>for</code> Statement</a>
  - <a href="#Blocks" id="toc-Blocks-1">4.8 Blocks</a>
  - <a href="#The-Null-Statement" id="toc-The-Null-Statement-1">4.9 The Null
    Statement</a>
  - <a href="#The-goto-Statement" id="toc-The-goto-Statement-1">4.10 The
    <code>goto</code> Statement</a>
  - <a href="#The-break-Statement" id="toc-The-break-Statement-1">4.11 The
    <code>break</code> Statement</a>
  - <a href="#The-continue-Statement" id="toc-The-continue-Statement-1">4.12
    The <code>continue</code> Statement</a>
  - <a href="#The-return-Statement" id="toc-The-return-Statement-1">4.13 The
    <code>return</code> Statement</a>
  - <a href="#The-typedef-Statement" id="toc-The-typedef-Statement-1">4.14
    The <code>typedef</code> Statement</a>
- <a href="#Functions" id="toc-Functions-1">5 Functions</a>
  - <a href="#Function-Declarations" id="toc-Function-Declarations-1">5.1
    Function Declarations</a>
  - <a href="#Function-Definitions" id="toc-Function-Definitions-1">5.2
    Function Definitions</a>
  - <a href="#Calling-Functions" id="toc-Calling-Functions-1">5.3 Calling
    Functions</a>
  - <a href="#Function-Parameters" id="toc-Function-Parameters-1">5.4
    Function Parameters</a>
  - <a href="#Variable-Length-Parameter-Lists"
    id="toc-Variable-Length-Parameter-Lists-1">5.5 Variable Length Parameter
    Lists</a>
  - <a href="#Calling-Functions-Through-Function-Pointers"
    id="toc-Calling-Functions-Through-Function-Pointers-1">5.6 Calling
    Functions Through Function Pointers</a>
  - <a href="#The-main-Function" id="toc-The-main-Function-1">5.7 The
    <code>main</code> Function</a>
  - <a href="#Recursive-Functions" id="toc-Recursive-Functions-1">5.8
    Recursive Functions</a>
  - <a href="#Static-Functions" id="toc-Static-Functions-1">5.9 Static
    Functions</a>
  - <a href="#Nested-Functions" id="toc-Nested-Functions-1">5.10 Nested
    Functions</a>
- <a href="#Program-Structure-and-Scope"
  id="toc-Program-Structure-and-Scope-1">6 Program Structure and Scope</a>
  - <a href="#Program-Structure" id="toc-Program-Structure-1">6.1 Program
    Structure</a>
  - <a href="#Scope" id="toc-Scope-1">6.2 Scope</a>
- <a href="#A-Sample-Program" id="toc-A-Sample-Program-1">7 A Sample
  Program</a>
  - <a href="#hello_002ec" id="toc-hello_002ec-1">7.1
    <code>hello.c</code></a>
  - <a href="#system_002eh" id="toc-system_002eh-1">7.2
    <code>system.h</code></a>
- <a href="#Overflow" id="toc-Overflow-1">Appendix A Overflow</a>
  - <a href="#Integer-Overflow-Basics"
    id="toc-Basics-of-Integer-Overflow">A.1 Basics of Integer Overflow</a>
  - <a href="#Signed-Overflow-Examples"
    id="toc-Examples-of-Code-Assuming-Wraparound-Overflow">A.2 Examples of
    Code Assuming Wraparound Overflow</a>
  - <a href="#Optimization-and-Wraparound"
    id="toc-Optimizations-That-Break-Wraparound-Arithmetic">A.3
    Optimizations That Break Wraparound Arithmetic</a>
  - <a href="#Signed-Overflow-Advice"
    id="toc-Practical-Advice-for-Signed-Overflow-Issues">A.4 Practical
    Advice for Signed Overflow Issues</a>
  - <a href="#Signed-Integer-Division"
    id="toc-Signed-Integer-Division-and-Integer-Overflow">A.5 Signed Integer
    Division and Integer Overflow</a>
- <a href="#GNU-Free-Documentation-License"
  id="toc-GNU-Free-Documentation-License-1">GNU Free Documentation
  License</a>
- <a href="#Index" id="toc-Index-1">Index</a>

</div>

<span id="Top"></span>

<div class="header">

Next: <a href="#Preface" accesskey="n" rel="next">Preface</a>, Up:
<a href="dir.html#Top" accesskey="u" rel="up">(dir)</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-GNU-C-Reference-Manual"></span>

# The GNU C Reference Manual

This is the GNU C reference manual.

|  |  |  |
|:---|----|:---|
| • <a href="#Preface" accesskey="1">Preface</a>: |    |  |
| • <a href="#Lexical-Elements" accesskey="2">Lexical Elements</a>: |    |  |
| • <a href="#Data-Types" accesskey="3">Data Types</a>: |    |  |
| • <a href="#Expressions-and-Operators" accesskey="4">Expressions and
Operators</a>: |    |  |
| • <a href="#Statements" accesskey="5">Statements</a>: |    |  |
| • <a href="#Functions" accesskey="6">Functions</a>: |    |  |
| • <a href="#Program-Structure-and-Scope" accesskey="7">Program Structure
and Scope</a>: |    |  |
| • <a href="#A-Sample-Program" accesskey="8">A Sample Program</a>: |    |  |
| • <a href="#Overflow" accesskey="9">Overflow</a>: |    |  |
| • [GNU Free Documentation License](#GNU-Free-Documentation-License): |    |  |
| • [Index](#Index): |    |  |

------------------------------------------------------------------------

<span id="Preface"></span>

<div class="header">

Next: <a href="#Lexical-Elements" accesskey="n" rel="next">Lexical
Elements</a>, Previous: <a href="#Top" accesskey="p" rel="prev">Top</a>,
Up: <a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Preface-1"></span>

## Preface

<span id="index-preface"></span>

This is a reference manual for the C programming language as implemented
by the GNU Compiler Collection (GCC). Specifically, this manual aims to
document:

- The 1989 ANSI C standard, commonly known as “C89”
- The 1999 ISO C standard, commonly known as “C99”, to the extent that
  C99 is implemented by GCC
- The current state of GNU extensions to standard C

This manual describes C89 as its baseline. C99 features and GNU
extensions are explicitly labeled as such.

By default, GCC will compile code as C89 plus GNU-specific extensions.
Much of C99 is supported; once full support is available, the default
compilation dialect will be C99 plus GNU-specific extensions. (Some of
the GNU extensions to C89 ended up, sometimes slightly modified, as
standard language features in C99.)

The C language includes a set of preprocessor directives, which are used
for things such as macro text replacement, conditional compilation, and
file inclusion. Although normally described in a C language manual, the
GNU C preprocessor has been thoroughly documented in The C Preprocessor,
a separate manual which covers preprocessing for C, C++, and Objective-C
programs, so it is not included here.

<span id="Credits"></span>

### Credits

Thanks to everyone who has helped with editing, proofreading, ideas,
typesetting, and administrivia, including: Diego Andres Alvarez Marin,
Nelson H. F. Beebe, Karl Berry, Robert Chassell, Hanfeng Chen, Mark de
Volld, Antonio Diaz Diaz, dine, Andreas Foerster, Denver Gingerich, Lisa
Goldstein, Robert Hansen, Jean-Christophe Helary, Mogens Hetsholm, Teddy
Hogeborn, Joe Humphries, J. Wren Hunt, Dutch Ingraham, Adam Johansen,
Vladimir Kadlec, Benjamin Kagia, Dright Kayorent, Sugun Kedambadi, Felix
Lee, Bjorn Liencres, Steve Morningthunder, Aljosha Papsch, Matthew
Plant, Jonathan Sisti, Richard Stallman, J. Otto Tennant, Ole Tetlie,
Keith Thompson, T.F. Torrey, James Youngman, and Steve Zachar. Trevis
Rothwell serves as project maintainer and, along with James Youngman,
wrote the bulk of the text.

Some example programs are based on algorithms in Donald Knuth’s The Art
of Computer Programming.

Please send bug reports and suggestions to <gnu-c-manual@gnu.org>.

------------------------------------------------------------------------

<span id="Lexical-Elements"></span>

<div class="header">

Next: <a href="#Data-Types" accesskey="n" rel="next">Data Types</a>,
Previous: <a href="#Preface" accesskey="p" rel="prev">Preface</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Lexical-Elements-1"></span>

## 1 Lexical Elements

<span id="index-lexical-elements"></span>

This chapter describes the lexical elements that make up C source code
after preprocessing. These elements are called *tokens*. There are five
types of tokens: keywords, identifiers, constants, operators, and
separators. White space, sometimes required to separate tokens, is also
described in this chapter.

|                                                         |     |     |
|:--------------------------------------------------------|-----|:----|
| • <a href="#Identifiers" accesskey="1">Identifiers</a>: |     |     |
| • <a href="#Keywords" accesskey="2">Keywords</a>:       |     |     |
| • <a href="#Constants" accesskey="3">Constants</a>:     |     |     |
| • <a href="#Operators" accesskey="4">Operators</a>:     |     |     |
| • <a href="#Separators" accesskey="5">Separators</a>:   |     |     |
| • <a href="#White-Space" accesskey="6">White Space</a>: |     |     |

------------------------------------------------------------------------

<span id="Identifiers"></span>

<div class="header">

Next: <a href="#Keywords" accesskey="n" rel="next">Keywords</a>, Up:
<a href="#Lexical-Elements" accesskey="u" rel="up">Lexical Elements</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Identifiers-1"></span>

### 1.1 Identifiers

<span id="index-identifiers"></span>

Identifiers are sequences of characters used for naming variables,
functions, new data types, and preprocessor macros. You can include
letters, decimal digits, and the underscore character ‘`_`’ in
identifiers.

The first character of an identifier cannot be a digit.

Lowercase letters and uppercase letters are distinct, such that `foo`
and `FOO` are two different identifiers.

When using GNU extensions, you can also include the dollar sign
character ‘`$`’ in identifiers.

------------------------------------------------------------------------

<span id="Keywords"></span>

<div class="header">

Next: <a href="#Constants" accesskey="n" rel="next">Constants</a>,
Previous:
<a href="#Identifiers" accesskey="p" rel="prev">Identifiers</a>, Up:
<a href="#Lexical-Elements" accesskey="u" rel="up">Lexical Elements</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Keywords-1"></span>

### 1.2 Keywords

<span id="index-keywords"></span>

Keywords are special identifiers reserved for use as part of the
programming language itself. You cannot use them for any other purpose.

Here is a list of keywords recognized by ANSI C89:

<div class="example">

``` example
auto break case char const continue default do double else enum extern
float for goto if int long register return short signed sizeof static
struct switch typedef union unsigned void volatile while
```

</div>

ISO C99 adds the following keywords:

<div class="example">

``` example
inline _Bool _Complex _Imaginary
```

</div>

and GNU extensions add these keywords:

<div class="example">

``` example
__FUNCTION__ __PRETTY_FUNCTION__ __alignof __alignof__ __asm
__asm__ __attribute __attribute__ __builtin_offsetof __builtin_va_arg
__complex __complex__ __const __extension__ __func__ __imag __imag__ 
__inline __inline__ __label__ __null __real __real__ 
__restrict __restrict__ __signed __signed__ __thread __typeof
__volatile __volatile__ 
```

</div>

In both ISO C99 and C89 with GNU extensions, the following is also
recognized as a keyword:

<div class="example">

``` example
restrict
```

</div>

------------------------------------------------------------------------

<span id="Constants"></span>

<div class="header">

Next: <a href="#Operators" accesskey="n" rel="next">Operators</a>,
Previous: <a href="#Keywords" accesskey="p" rel="prev">Keywords</a>, Up:
<a href="#Lexical-Elements" accesskey="u" rel="up">Lexical Elements</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Constants-1"></span>

### 1.3 Constants

<span id="index-constants"></span>

A constant is a literal numeric or character value, such as `5` or
`'m'`. All constants are of a particular data type; you can use type
casting to explicitly specify the type of a constant, or let the
compiler use the default type based on the value of the constant.

|  |  |  |
|:---|----|:---|
| • <a href="#Integer-Constants" accesskey="1">Integer Constants</a>: |    |  |
| • <a href="#Character-Constants" accesskey="2">Character Constants</a>: |    |  |
| • <a href="#Real-Number-Constants" accesskey="3">Real Number Constants</a>: |    |  |
| • <a href="#String-Constants" accesskey="4">String Constants</a>: |    |  |

------------------------------------------------------------------------

<span id="Integer-Constants"></span>

<div class="header">

Next: <a href="#Character-Constants" accesskey="n" rel="next">Character
Constants</a>, Up:
<a href="#Constants" accesskey="u" rel="up">Constants</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Integer-Constants-1"></span>

#### 1.3.1 Integer Constants

<span id="index-integer-constants"></span>
<span id="index-constants_002c-integer"></span>

An integer constant is a sequence of digits, with an optional prefix to
denote a number base.

If the sequence of digits is preceded by `0x` or `0X` (zero x or zero
X), then the constant is considered to be hexadecimal (base 16).
Hexadecimal values may use the digits from 0 to 9, as well as the
letters `a` to `f` and `A` to `F`. Here are some examples:

<div class="example">

``` example
0x2f
0x88
0xAB43
0xAbCd
0x1
```

</div>

If the first digit is 0 (zero), and the next character is not ‘`x`’ or
‘`X`’, then the constant is considered to be octal (base 8). Octal
values may only use the digits from 0 to 7; 8 and 9 are not allowed.
Here are some examples:

<div class="example">

``` example
057
012
03
0241
```

</div>

In all other cases, the sequence of digits is assumed to be decimal
(base 10). Decimal values may use the digits from 0 to 9. Here are some
examples:

<div class="example">

``` example
459
23901
8
12
```

</div>

There are various integer data types, for short integers, long integers,
signed integers, and unsigned integers. You can force an integer
constant to be of a long and/or unsigned integer type by appending a
sequence of one or more letters to the end of the constant:

`u`  
`U`  
Unsigned integer type.

`l`  
`L`  
Long integer type.

For example, `45U` is an `unsigned int` constant. You can also combine
letters: `45UL` is an `unsigned long int` constant. (The letters may be
used in any order.)

Both ISO C99 and GNU C extensions add the integer types `long long int`
and `unsigned long long int`. You can use two ‘`L`’s to get a
`long long int` constant; add a ‘`U`’ to that and you have an
`unsigned long long int` constant. For example: `45ULL`.

------------------------------------------------------------------------

<span id="Character-Constants"></span>

<div class="header">

Next:
<a href="#Real-Number-Constants" accesskey="n" rel="next">Real Number
Constants</a>, Previous:
<a href="#Integer-Constants" accesskey="p" rel="prev">Integer
Constants</a>, Up:
<a href="#Constants" accesskey="u" rel="up">Constants</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Character-Constants-1"></span>

#### 1.3.2 Character Constants

<span id="index-character-constants"></span>
<span id="index-constants_002c-character"></span>

A character constant is usually a single character enclosed within
single quotation marks, such as `'Q'`. A character constant is of type
`int` by default.

Some characters, such as the single quotation mark character itself,
cannot be represented using only one character. To represent such
characters, there are several “escape sequences” that you can use:

`\\`  
Backslash character.

`\?`  
Question mark character.

`\'`  
Single quotation mark.

`\"`  
Double quotation mark.

`\a`  
Audible alert.

`\b`  
Backspace character.

`\e`  
\<ESC\> character. (This is a GNU extension.)

`\f`  
Form feed.

`\n`  
Newline character.

`\r`  
Carriage return.

`\t`  
Horizontal tab.

`\v`  
Vertical tab.

`\o, \oo, \ooo`  
Octal number.

`\xh, \xhh, \xhhh, …`  
Hexadecimal number.

To use any of these escape sequences, enclose the sequence in single
quotes, and treat it as if it were any other character. For example, the
letter m is `'m'` and the newline character is `'\n'`.

The octal number escape sequence is the backslash character followed by
one, two, or three octal digits (0 to 7). For example, 101 is the octal
equivalent of 65, which is the ASCII character `'A'`. Thus, the
character constant `'\101'` is the same as the character constant `'A'`.

The hexadecimal escape sequence is the backslash character, followed by
`x` and an unlimited number of hexadecimal digits (0 to 9, and `a` to
`f` or `A` to `F`).

While the length of possible hexadecimal digit strings is unlimited, the
number of character constants in any given character set is not. (The
much-used extended ASCII character set, for example, has only 256
characters in it.) If you try to use a hexadecimal value that is outside
the range of characters, you will get a compile-time error.

------------------------------------------------------------------------

<span id="Real-Number-Constants"></span>

<div class="header">

Next: <a href="#String-Constants" accesskey="n" rel="next">String
Constants</a>, Previous:
<a href="#Character-Constants" accesskey="p" rel="prev">Character
Constants</a>, Up:
<a href="#Constants" accesskey="u" rel="up">Constants</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Real-Number-Constants-1"></span>

#### 1.3.3 Real Number Constants

<span id="index-floating-point-constants"></span>
<span id="index-constants_002c-floating-point"></span>
<span id="index-real-number-constants"></span>
<span id="index-constants_002c-real-number"></span>

A real number constant is a value that represents a fractional (floating
point) number. It consists of a sequence of digits which represents the
integer (or “whole”) part of the number, a decimal point, and a sequence
of digits which represents the fractional part.

Either the integer part or the fractional part may be omitted, but not
both. Here are some examples:

<div class="example">

``` example
double a, b, c, d, e, f;

a = 4.7;

b = 4.;

c = 4;

d = .7;

e = 0.7;
```

</div>

(In the third assignment statement, the integer constant 4 is
automatically converted from an integer value to a double value.)

Real number constants can also be followed by `e` or `E`, and an integer
exponent. The exponent can be either positive or negative.

<div class="example">

``` example
double x, y;

x = 5e2;   /* x is 5 * 100, or 500.0. */
y = 5e-2;  /* y is 5 * (1/100), or 0.05. */
```

</div>

You can append a letter to the end of a real number constant to cause it
to be of a particular type. If you append the letter F (or f) to a real
number constant, then its type is `float`. If you append the letter L
(or l), then its type is `long double`. If you do not append any
letters, then its type is `double`.

------------------------------------------------------------------------

<span id="String-Constants"></span>

<div class="header">

Previous:
<a href="#Real-Number-Constants" accesskey="p" rel="prev">Real Number
Constants</a>, Up:
<a href="#Constants" accesskey="u" rel="up">Constants</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="String-Constants-1"></span>

#### 1.3.4 String Constants

<span id="index-string-constants"></span>
<span id="index-string-literals"></span>

A string constant is a sequence of zero or more characters, digits, and
escape sequences enclosed within double quotation marks. A string
constant is of type “array of characters”. All string constants contain
a null termination character (`\0`) as their last character. Strings are
stored as arrays of characters, with no inherent size attribute. The
null termination character lets string-processing functions know where
the string ends.

Adjacent string constants are concatenated (combined) into one string,
with the null termination character added to the end of the final
concatenated string.

A string cannot contain double quotation marks, as double quotation
marks are used to enclose the string. To include the double quotation
mark character in a string, use the `\"` escape sequence. You can use
any of the escape sequences that can be used as character constants in
strings. Here are some example of string constants:

<div class="example">

``` example
/* This is a single string constant. */
"tutti frutti ice cream"

/* These string constants will be concatenated, same as above. */
"tutti " "frutti" " ice " "cream"

/* This one uses two escape sequences. */
"\"hello, world!\""
```

</div>

If a string is too long to fit on one line, you can use a backslash `\`
to break it up onto separate lines.

<div class="example">

``` example
"Today's special is a pastrami sandwich on rye bread with \
a potato knish and a cherry soda."
```

</div>

Adjacent strings are automatically concatenated, so you can also have
string constants span multiple lines by writing them as separate,
adjacent, strings. For example:

<div class="example">

``` example
"Tomorrow's special is a corned beef sandwich on "
"pumpernickel bread with a kasha knish and seltzer water."
```

</div>

is the same as

<div class="example">

``` example
"Tomorrow's special is a corned beef sandwich on \
pumpernickel bread with a kasha knish and seltzer water."
```

</div>

To insert a newline character into the string, so that when the string
is printed it will be printed on two different lines, you can use the
newline escape sequence ‘`\n`’.

<div class="example">

``` example
printf ("potato\nknish");
```

</div>

prints

<div class="example">

``` example
potato
knish
```

</div>

------------------------------------------------------------------------

<span id="Operators"></span>

<div class="header">

Next: <a href="#Separators" accesskey="n" rel="next">Separators</a>,
Previous: <a href="#Constants" accesskey="p" rel="prev">Constants</a>,
Up:
<a href="#Lexical-Elements" accesskey="u" rel="up">Lexical Elements</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Operators-1"></span>

### 1.4 Operators

<span id="index-operators-as-lexical-elements"></span>

An operator is a special token that performs an operation, such as
addition or subtraction, on either one, two, or three operands. Full
coverage of operators can be found in a later chapter. See [Expressions
and Operators](#Expressions-and-Operators).

------------------------------------------------------------------------

<span id="Separators"></span>

<div class="header">

Next: <a href="#White-Space" accesskey="n" rel="next">White Space</a>,
Previous: <a href="#Operators" accesskey="p" rel="prev">Operators</a>,
Up:
<a href="#Lexical-Elements" accesskey="u" rel="up">Lexical Elements</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Separators-1"></span>

### 1.5 Separators

<span id="index-separators"></span>

A separator separates tokens. White space (see next section) is a
separator, but it is not a token. The other separators are all
single-character tokens themselves:

<div class="example">

``` example
( ) [ ] { } ; , . :
```

</div>

------------------------------------------------------------------------

<span id="White-Space"></span>

<div class="header">

Previous: <a href="#Separators" accesskey="p" rel="prev">Separators</a>,
Up:
<a href="#Lexical-Elements" accesskey="u" rel="up">Lexical Elements</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="White-Space-1"></span>

### 1.6 White Space

<span id="index-white-space"></span>

White space is the collective term used for several characters: the
space character, the tab character, the newline character, the vertical
tab character, and the form-feed character. White space is ignored
(outside of string and character constants), and is therefore optional,
except when it is used to separate tokens. This means that

<div class="example">

``` example
#include <stdio.h>

int
main()
{
  printf( "hello, world\n" );
  return 0;
}
```

</div>

and

<div class="example">

``` example
#include <stdio.h> int main(){printf("hello, world\n");
return 0;}
```

</div>

are functionally the same program.

Although you must use white space to separate many tokens, no white
space is required between operators and operands, nor is it required
between other separators and that which they separate.

<div class="example">

``` example
/* All of these are valid. */

x++;
x ++ ;
x=y+z;
x = y + z ;
x=array[2];
x = array [ 2 ] ;
fraction=numerator / *denominator_ptr;
fraction = numerator / * denominator_ptr ;
```

</div>

Furthermore, wherever one space is allowed, any amount of white space is
allowed.

<div class="example">

``` example
/* These two statements are functionally identical. */
x++;

x
       ++       ;
```

</div>

In string constants, spaces and tabs are not ignored; rather, they are
part of the string. Therefore,

<div class="example">

``` example
"potato knish"
```

</div>

is not the same as

<div class="example">

``` example
"potato                        knish"
```

</div>

------------------------------------------------------------------------

<span id="Data-Types"></span>

<div class="header">

Next: <a href="#Expressions-and-Operators" accesskey="n"
rel="next">Expressions and Operators</a>, Previous:
<a href="#Lexical-Elements" accesskey="p" rel="prev">Lexical
Elements</a>, Up: <a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Data-Types-1"></span>

## 2 Data Types

<span id="index-data-types"></span> <span id="index-types"></span>

|                                                                   |     |     |
|:------------------------------------------------------------------|-----|:----|
| • <a href="#Primitive-Types" accesskey="1">Primitive Types</a>:   |     |     |
| • <a href="#Enumerations" accesskey="2">Enumerations</a>:         |     |     |
| • <a href="#Unions" accesskey="3">Unions</a>:                     |     |     |
| • <a href="#Structures" accesskey="4">Structures</a>:             |     |     |
| • <a href="#Arrays" accesskey="5">Arrays</a>:                     |     |     |
| • <a href="#Pointers" accesskey="6">Pointers</a>:                 |     |     |
| • <a href="#Incomplete-Types" accesskey="7">Incomplete Types</a>: |     |     |
| • <a href="#Type-Qualifiers" accesskey="8">Type Qualifiers</a>:   |     |     |
| • <a href="#Storage-Class-Specifiers" accesskey="9">Storage Class 
 Specifiers</a>:                                                    |     |     |
| • [Renaming Types](#Renaming-Types):                              |     |     |

------------------------------------------------------------------------

<span id="Primitive-Types"></span>

<div class="header">

Next: <a href="#Enumerations" accesskey="n" rel="next">Enumerations</a>,
Up: <a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Primitive-Data-Types"></span>

### 2.1 Primitive Data Types

<span id="index-primitive-data-types"></span>
<span id="index-data-types_002c-primitive"></span>
<span id="index-types_002c-primitive"></span>

|  |  |  |
|:---|----|:---|
| • <a href="#Integer-Types" accesskey="1">Integer Types</a>: |    |  |
| • <a href="#Real-Number-Types" accesskey="2">Real Number Types</a>: |    |  |
| • <a href="#Complex-Number-Types" accesskey="3">Complex Number Types</a>: |    |  |

------------------------------------------------------------------------

<span id="Integer-Types"></span>

<div class="header">

Next: <a href="#Real-Number-Types" accesskey="n" rel="next">Real Number
Types</a>, Up:
<a href="#Primitive-Types" accesskey="u" rel="up">Primitive Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Integer-Types-1"></span>

#### 2.1.1 Integer Types

<span id="index-integer-types"></span>
<span id="index-data-types_002c-integer"></span>
<span id="index-types_002c-integer"></span>

The integer data types range in size from at least 8 bits to at least 32
bits. The C99 standard extends this range to include integer sizes of at
least 64 bits. You should use integer types for storing whole number
values (and the `char` data type for storing characters). The sizes and
ranges listed for these types are minimums; depending on your computer
platform, these sizes and ranges may be larger.

While these ranges provide a natural ordering, the standard does not
require that any two types have a different range. For example, it is
common for `int` and `long` to have the same range. The standard even
allows `signed char` and `long` to have the same range, though such
platforms are very unusual.

- `signed char` <span id="index-signed-char-data-type"></span>  
  The 8-bit `signed char` data type can hold integer values in the range
  of -128 to 127.
- `unsigned char` <span id="index-unsigned-char-data-type"></span>  
  The 8-bit `unsigned char` data type can hold integer values in the
  range of 0 to 255.
- `char` <span id="index-char-data-type"></span>  
  Depending on your system, the `char` data type is defined as having
  the same range as either the `signed char` or the `unsigned char` data
  type (they are three distinct types, however). By convention, you
  should use the `char` data type specifically for storing ASCII
  characters (such as `` `m' ``), including escape sequences (such as
  `` `\n' ``).
- `short int` <span id="index-short-int-data-type"></span>  
  The 16-bit `short int` data type can hold integer values in the range
  of -32,768 to 32,767. You may also refer to this data type as `short`,
  `signed short int`, or `signed short`.
- `unsigned short int`
  <span id="index-unsigned-short-int-data-type"></span>  
  The 16-bit `unsigned short int` data type can hold integer values in
  the range of 0 to 65,535. You may also refer to this data type as
  `unsigned short`.
- `int` <span id="index-int-data-type"></span>  
  The 32-bit `int` data type can hold integer values in the range of
  -2,147,483,648 to 2,147,483,647. You may also refer to this data type
  as `signed int` or `signed`.
- `unsigned int` <span id="index-unsigned-int-data-type"></span>  
  The 32-bit `unsigned int` data type can hold integer values in the
  range of 0 to 4,294,967,295. You may also refer to this data type
  simply as `unsigned`.
- `long int` <span id="index-long-int-data-type"></span>  
  The 32-bit `long int` data type can hold integer values in the range
  of at least -2,147,483,648 to 2,147,483,647. (Depending on your
  system, this data type might be 64-bit, in which case its range is
  identical to that of the `long long int` data type.) You may also
  refer to this data type as `long`, `signed long int`, or
  `signed long`.
- `unsigned long int`
  <span id="index-unsigned-long-int-data-type"></span>  
  The 32-bit `unsigned long int` data type can hold integer values in
  the range of at least 0 to 4,294,967,295. (Depending on your system,
  this data type might be 64-bit, in which case its range is identical
  to that of the `unsigned long long int` data type.) You may also refer
  to this data type as `unsigned long`.
- `long long int` <span id="index-long-long-int-data-type"></span>  
  The 64-bit `long long int` data type can hold integer values in the
  range of -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807. You
  may also refer to this data type as `long long`,
  `signed long long int` or `signed long long`. This type is not part of
  C89, but is both part of C99 and a GNU C extension.
- `unsigned long long int`
  <span id="index-unsigned-long-long-int-data-type"></span>  
  The 64-bit `unsigned long long int` data type can hold integer values
  in the range of at least 0 to 18,446,744,073,709,551,615. You may also
  refer to this data type as `unsigned long long`. This type is not part
  of C89, but is both part of C99 and a GNU C extension.

Here are some examples of declaring and defining integer variables:

<div class="example">

``` example
int foo;
unsigned int bar = 42;
char quux = 'a';
```

</div>

The first line declares an integer named `foo` but does not define its
value; it is left uninitialized, and its value should not be assumed to
be anything in particular.

------------------------------------------------------------------------

<span id="Real-Number-Types"></span>

<div class="header">

Next:
<a href="#Complex-Number-Types" accesskey="n" rel="next">Complex Number
Types</a>, Previous:
<a href="#Integer-Types" accesskey="p" rel="prev">Integer Types</a>, Up:
<a href="#Primitive-Types" accesskey="u" rel="up">Primitive Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Real-Number-Types-1"></span>

#### 2.1.2 Real Number Types

<span id="index-real-number-types"></span>
<span id="index-floating-point-types"></span>
<span id="index-data-types_002c-real-number"></span>
<span id="index-data-types_002c-floating-point"></span>
<span id="index-types_002c-real-number"></span>
<span id="index-types_002c-floating-point"></span>

There are three data types that represent fractional numbers. While the
sizes and ranges of these types are consistent across most computer
systems in use today, historically the sizes of these types varied from
system to system. As such, the minimum and maximum values are stored in
macro definitions in the library header file `float.h`. In this section,
we include the names of the macro definitions in place of their possible
values; check your system’s `float.h` for specific numbers.

- `float` <span id="index-float-data-type"></span>  
  The `float` data type is the smallest of the three floating point
  types, if they differ in size at all. Its minimum value is stored in
  the `FLT_MIN`, and should be no greater than `1e-37`. Its maximum
  value is stored in `FLT_MAX`, and should be no less than `1e37`.
- `double` <span id="index-double-data-type"></span>  
  The `double` data type is at least as large as the `float` type, and
  it may be larger. Its minimum value is stored in `DBL_MIN`, and its
  maximum value is stored in `DBL_MAX`.
- `long double` <span id="index-long-double-data-type"></span>  
  The `long double` data type is at least as large as the `float` type,
  and it may be larger. Its minimum value is stored in `LDBL_MIN`, and
  its maximum value is stored in `LDBL_MAX`.

All floating point data types are signed; trying to use
`unsigned float`, for example, will cause a compile-time error.

Here are some examples of declaring and defining real number variables:

<div class="example">

``` example
float foo;
double bar = 114.3943;
```

</div>

The first line declares a float named `foo` but does not define its
value; it is left uninitialized, and its value should not be assumed to
be anything in particular.

The real number types provided in C are of finite precision, and
accordingly, not all real numbers can be represented exactly. Most
computer systems that GCC compiles for use a binary representation for
real numbers, which is unable to precisely represent numbers such as,
for example, 4.2. For this reason, we recommend that you consider not
comparing real numbers for exact equality with the `==` operator, but
rather check that real numbers are within an acceptable tolerance.

There are other more subtle implications of these imprecise
representations; for more details, see David Goldberg’s paper What Every
Computer Scientist Should Know About Floating-Point Arithmetic and
section 4.2.2 of Donald Knuth’s The Art of Computer Programming.

------------------------------------------------------------------------

<span id="Complex-Number-Types"></span>

<div class="header">

Previous:
<a href="#Real-Number-Types" accesskey="p" rel="prev">Real Number
Types</a>, Up:
<a href="#Primitive-Types" accesskey="u" rel="up">Primitive Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Complex-Number-Types-1"></span>

#### 2.1.3 Complex Number Types

<span id="index-complex-number-types"></span>
<span id="index-data-types_002c-complex-number"></span>
<span id="index-types_002c-complex-number"></span>

GCC introduced some complex number types as an extension to C89. Similar
features were introduced in
C99<a href="#FOOT1" id="DOCF1"><sup>1</sup></a>, but there were a number
of differences. We describe the standard complex number types first.

|  |  |  |
|:---|----|:---|
| • <a href="#Standard-Complex-Number-Types" accesskey="1">Standard Complex
Number Types</a>: |    |  |
| • <a href="#GNU-Extensions-for-Complex-Number-Types" accesskey="2">GNU
Extensions for Complex Number Types</a>: |    |  |

------------------------------------------------------------------------

<span id="Standard-Complex-Number-Types"></span>

<div class="header">

Next: <a href="#GNU-Extensions-for-Complex-Number-Types" accesskey="n"
rel="next">GNU Extensions for Complex Number Types</a>, Up:
<a href="#Complex-Number-Types" accesskey="u" rel="up">Complex Number
Types</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Standard-Complex-Number-Types-1"></span>

#### 2.1.3.1 Standard Complex Number Types

Complex types were introduced in C99. There are three complex types:

- `float _Complex`
- `double _Complex`
- `long double _Complex`

The names here begin with an underscore and an uppercase letter in order
to avoid conflicts with existing programs’ identifiers. However, the C99
standard header file `<complex.h>` introduces some macros which make
using complex types easier.

- `complex`  
  Expands to `_Complex`. This allows a variable to be declared as
  `double complex` which seems more natural.
- `I`  
  A constant of type `const float _Complex` having the value of the
  imaginary unit normally referred to as *i*.

The `<complex.h>` header file also declares a number of functions for
performing computations on complex numbers, for example the `creal` and
`cimag` functions which respectively return the real and imaginary parts
of a `double complex` number. Other functions are also provided, as
shown in this example:

<div class="example">

``` example
#include <complex.h>    
#include <stdio.h>  

void example (void) 
{    
  complex double z = 1.0 + 3.0*I; 
  printf ("Phase is %f, modulus is %f\n", carg (z), cabs (z));        
}  
```

</div>

------------------------------------------------------------------------

<span id="GNU-Extensions-for-Complex-Number-Types"></span>

<div class="header">

Previous: <a href="#Standard-Complex-Number-Types" accesskey="p"
rel="prev">Standard Complex Number Types</a>, Up:
<a href="#Complex-Number-Types" accesskey="u" rel="up">Complex Number
Types</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="GNU-Extensions-for-Complex-Number-Types-1"></span>

#### 2.1.3.2 GNU Extensions for Complex Number Types

GCC also introduced complex types as a GNU extension to C89, but the
spelling is different. The floating-point complex types in GCC’s C89
extension are:

- `__complex__ float`
- `__complex__ double`
- `__complex__ long double`

GCC’s extension allow for complex types other than floating-point, so
that you can declare complex character types and complex integer types;
in fact `__complex__` can be used with any of the primitive data types.
We won’t give you a complete list of all possibilities, but here are
some examples:

- `__complex__ float`  
  The `__complex__ float` data type has two components: a real part and
  an imaginary part, both of which are of the `float` data type.
- `__complex__ int`  
  The `__complex__ int` data type also has two components: a real part
  and an imaginary part, both of which are of the `int` data type.

To extract the real part of a complex-valued expression, use the keyword
`__real__`, followed by the expression. Likewise, use `__imag__` to
extract the imaginary part.

<div class="example">

``` example
__complex__ float a = 4 + 3i;

float b = __real__ a;          /* b is now 4. */
float c = __imag__ a;          /* c is now 3. */
```

</div>

This example creates a complex floating point variable `a`, and defines
its real part as 4 and its imaginary part as 3. Then, the real part is
assigned to the floating point variable `b`, and the imaginary part is
assigned to the floating point variable `c`.

------------------------------------------------------------------------

<span id="Enumerations"></span>

<div class="header">

Next: <a href="#Unions" accesskey="n" rel="next">Unions</a>, Previous:
<a href="#Primitive-Types" accesskey="p" rel="prev">Primitive Types</a>,
Up: <a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Enumerations-1"></span>

### 2.2 Enumerations

<span id="index-enumerations"></span>
<span id="index-types_002c-enumeration"></span>
<span id="index-data-types_002c-enumeration"></span>

An enumeration is a custom data type used for storing constant integer
values and referring to them by names. By default, these values are of
type `signed int`; however, you can use the `-fshort-enums` GCC compiler
option to cause the smallest possible integer type to be used instead.
Both of these behaviors conform to the C89 standard, but mixing the use
of these options within the same program can produce incompatibilities.

|  |  |  |
|:---|----|:---|
| • <a href="#Defining-Enumerations" accesskey="1">Defining Enumerations</a>: |    |  |
| • <a href="#Declaring-Enumerations" accesskey="2">Declaring
Enumerations</a>: |    |  |

------------------------------------------------------------------------

<span id="Defining-Enumerations"></span>

<div class="header">

Next:
<a href="#Declaring-Enumerations" accesskey="n" rel="next">Declaring
Enumerations</a>, Up:
<a href="#Enumerations" accesskey="u" rel="up">Enumerations</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Defining-Enumerations-1"></span>

#### 2.2.1 Defining Enumerations

<span id="index-defining-enumerations"></span>
<span id="index-enumerations_002c-defining"></span>

You define an enumeration using the `enum` keyword, followed by the name
of the enumeration (this is optional), followed by a list of constant
names (separated by commas and enclosed in braces), and ending with a
semicolon.

<div class="example">

``` example
enum fruit {grape, cherry, lemon, kiwi};
```

</div>

That example defines an enumeration, `fruit`, which contains four
constant integer values, `grape`, `cherry`, `lemon`, and `kiwi`, whose
values are, by default, 0, 1, 2, and 3, respectively. You can also
specify one or more of the values explicitly:

<div class="example">

``` example
enum more_fruit {banana = -17, apple, blueberry, mango};
```

</div>

That example defines `banana` to be -17, and the remaining values are
incremented by 1: `apple` is -16, `blueberry` is -15, and `mango` is
-14. Unless specified otherwise, an enumeration value is equal to one
more than the previous value (and the first value defaults to 0).

You can also refer to an enumeration value defined earlier in the same
enumeration:

<div class="example">

``` example
enum yet_more_fruit {kumquat, raspberry, peach,
                     plum = peach + 2};
```

</div>

In that example, `kumquat` is 0, `raspberry` is 1, `peach` is 2, and
`plum` is 4.

You can’t use the same name for an `enum` as a `struct` or `union` in
the same scope.

------------------------------------------------------------------------

<span id="Declaring-Enumerations"></span>

<div class="header">

Previous:
<a href="#Defining-Enumerations" accesskey="p" rel="prev">Defining
Enumerations</a>, Up:
<a href="#Enumerations" accesskey="u" rel="up">Enumerations</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Enumerations-1"></span>

#### 2.2.2 Declaring Enumerations

<span id="index-declaring-enumerations"></span>
<span id="index-enumerations_002c-declaring"></span>

You can declare variables of an enumeration type both when the
enumeration is defined and afterward. This example declares one
variable, named `my_fruit` of type `enum fruit`, all in a single
statement:

<div class="example">

``` example
enum fruit {banana, apple, blueberry, mango} my_fruit;
```

</div>

while this example declares the type and variable separately:

<div class="example">

``` example
enum fruit {banana, apple, blueberry, mango};
enum fruit my_fruit;
```

</div>

(Of course, you couldn’t declare it that way if you hadn’t named the
enumeration.)

Although such variables are considered to be of an enumeration type, you
can assign them any value that you could assign to an `int` variable,
including values from other enumerations. Furthermore, any variable that
can be assigned an `int` value can be assigned a value from an
enumeration.

However, you cannot change the values in an enumeration once it has been
defined; they are constant values. For example, this won’t work:

<div class="example">

``` example
enum fruit {banana, apple, blueberry, mango};
banana = 15;  /* You can’t do this! */
```

</div>

Enumerations are useful in conjunction with the `switch` statement,
because the compiler can warn you if you have failed to handle one of
the enumeration values. Using the example above, if your code handles
`banana`, `apple` and `mango` only but not `blueberry`, GCC can generate
a warning.

------------------------------------------------------------------------

<span id="Unions"></span>

<div class="header">

Next: <a href="#Structures" accesskey="n" rel="next">Structures</a>,
Previous:
<a href="#Enumerations" accesskey="p" rel="prev">Enumerations</a>, Up:
<a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Unions-1"></span>

### 2.3 Unions

<span id="index-unions"></span>
<span id="index-types_002c-union"></span>
<span id="index-data-types_002c-union"></span>

A union is a custom data type used for storing several variables in the
same memory space. Although you can access any of those variables at any
time, you should only read from one of them at a time—assigning a value
to one of them overwrites the values in the others.

|  |  |  |
|:---|----|:---|
| • <a href="#Defining-Unions" accesskey="1">Defining Unions</a>: |    |  |
| • <a href="#Declaring-Union-Variables" accesskey="2">Declaring Union
Variables</a>: |    |  |
| • <a href="#Accessing-Union-Members" accesskey="3">Accessing Union
Members</a>: |    |  |
| • <a href="#Size-of-Unions" accesskey="4">Size of Unions</a>: |    |  |

------------------------------------------------------------------------

<span id="Defining-Unions"></span>

<div class="header">

Next:
<a href="#Declaring-Union-Variables" accesskey="n" rel="next">Declaring
Union Variables</a>, Up:
<a href="#Unions" accesskey="u" rel="up">Unions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Defining-Unions-1"></span>

#### 2.3.1 Defining Unions

<span id="index-defining-unions"></span>
<span id="index-unions_002c-defining"></span>

You define a union using the `union` keyword followed by the
declarations of the union’s members, enclosed in braces. You declare
each member of a union just as you would normally declare a
variable—using the data type followed by one or more variable names
separated by commas, and ending with a semicolon. Then end the union
definition with a semicolon after the closing brace.

You should also include a name for the union between the `union` keyword
and the opening brace. This is syntactically optional, but if you leave
it out, you can’t refer to that union data type later on (without a
`typedef`, see [The typedef Statement](#The-typedef-Statement)).

Here is an example of defining a simple union for holding an integer
value and a floating point value:

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
```

</div>

That defines a union named `numbers`, which contains two members, `i`
and `f`, which are of type `int` and `float`, respectively.

------------------------------------------------------------------------

<span id="Declaring-Union-Variables"></span>

<div class="header">

Next:
<a href="#Accessing-Union-Members" accesskey="n" rel="next">Accessing
Union Members</a>, Previous:
<a href="#Defining-Unions" accesskey="p" rel="prev">Defining Unions</a>,
Up: <a href="#Unions" accesskey="u" rel="up">Unions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Union-Variables-1"></span>

#### 2.3.2 Declaring Union Variables

<span id="index-declaring-union-variables"></span>
<span id="index-union-variables_002c-declaring"></span>

You can declare variables of a union type when both you initially define
the union and after the definition, provided you gave the union type a
name.

|  |  |  |
|:---|----|:---|
| • <a href="#Declaring-Union-Variables-at-Definition"
accesskey="1">Declaring Union Variables at Definition</a>: |    |  |
| • <a href="#Declaring-Union-Variables-After-Definition"
accesskey="2">Declaring Union Variables After Definition</a>: |    |  |
| • <a href="#Initializing-Union-Members" accesskey="3">Initializing Union
Members</a>: |    |  |

------------------------------------------------------------------------

<span id="Declaring-Union-Variables-at-Definition"></span>

<div class="header">

Next:
<a href="#Declaring-Union-Variables-After-Definition" accesskey="n"
rel="next">Declaring Union Variables After Definition</a>, Up:
<a href="#Declaring-Union-Variables" accesskey="u" rel="up">Declaring
Union Variables</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Union-Variables-at-Definition-1"></span>

#### 2.3.2.1 Declaring Union Variables at Definition

<span id="index-declaring-union-variables-at-definition"></span>
<span id="index-union-variables_002c-declaring-at-definition"></span>

You can declare variables of a union type when you define the union type
by putting the variable names after the closing brace of the union
definition, but before the final semicolon. You can declare more than
one such variable by separating the names with commas.

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  } first_number, second_number;
```

</div>

That example declares two variables of type `union numbers`,
`first_number` and `second_number`.

------------------------------------------------------------------------

<span id="Declaring-Union-Variables-After-Definition"></span>

<div class="header">

Next: <a href="#Initializing-Union-Members" accesskey="n"
rel="next">Initializing Union Members</a>, Previous:
<a href="#Declaring-Union-Variables-at-Definition" accesskey="p"
rel="prev">Declaring Union Variables at Definition</a>, Up:
<a href="#Declaring-Union-Variables" accesskey="u" rel="up">Declaring
Union Variables</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Union-Variables-After-Definition-1"></span>

#### 2.3.2.2 Declaring Union Variables After Definition

<span id="index-declaring-union-variables-after-definition"></span>
<span id="index-union-variables_002c-declaring-after-definition"></span>

You can declare variables of a union type after you define the union by
using the `union` keyword and the name you gave the union type, followed
by one or more variable names separated by commas.

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
union numbers first_number, second_number;
```

</div>

That example declares two variables of type `union numbers`,
`first_number` and `second_number`.

------------------------------------------------------------------------

<span id="Initializing-Union-Members"></span>

<div class="header">

Previous:
<a href="#Declaring-Union-Variables-After-Definition" accesskey="p"
rel="prev">Declaring Union Variables After Definition</a>, Up:
<a href="#Declaring-Union-Variables" accesskey="u" rel="up">Declaring
Union Variables</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Initializing-Union-Members-1"></span>

#### 2.3.2.3 Initializing Union Members

<span id="index-initializing-union-members"></span>
<span id="index-union-members_002c-initializing"></span>

You can initialize the first member of a union variable when you declare
it:

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
union numbers first_number = { 5 };
```

</div>

In that example, the `i` member of `first_number` gets the value 5. The
`f` member is left alone.

Another way to initialize a union member is to specify the name of the
member to initialize. This way, you can initialize whichever member you
want to, not just the first one. There are two methods that you can
use—either follow the member name with a colon, and then its value, like
this:

<div class="example">

``` example
union numbers first_number = { f: 3.14159 };
```

</div>

or precede the member name with a period and assign a value with the
assignment operator, like this:

<div class="example">

``` example
union numbers first_number = { .f = 3.14159 };
```

</div>

You can also initialize a union member when you declare the union
variable during the definition:

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  } first_number = { 5 };
```

</div>

------------------------------------------------------------------------

<span id="Accessing-Union-Members"></span>

<div class="header">

Next:
<a href="#Size-of-Unions" accesskey="n" rel="next">Size of Unions</a>,
Previous:
<a href="#Declaring-Union-Variables" accesskey="p" rel="prev">Declaring
Union Variables</a>, Up:
<a href="#Unions" accesskey="u" rel="up">Unions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Accessing-Union-Members-1"></span>

#### 2.3.3 Accessing Union Members

<span id="index-accessing-union-members"></span>
<span id="index-union-members_002c-accessing"></span>

You can access the members of a union variable using the member access
operator. You put the name of the union variable on the left side of the
operator, and the name of the member on the right side.

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
union numbers first_number;
first_number.i = 5;
first_number.f = 3.9;
```

</div>

Notice in that example that giving a value to the `f` member overrides
the value stored in the `i` member.

------------------------------------------------------------------------

<span id="Size-of-Unions"></span>

<div class="header">

Previous:
<a href="#Accessing-Union-Members" accesskey="p" rel="prev">Accessing
Union Members</a>, Up:
<a href="#Unions" accesskey="u" rel="up">Unions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Size-of-Unions-1"></span>

#### 2.3.4 Size of Unions

<span id="index-size-of-unions"></span>
<span id="index-unions_002c-size-of"></span>

This size of a union is equal to the size of its largest member.
Consider the first union example from this section:

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
```

</div>

The size of the union data type is the same as `sizeof (float)`, because
the `float` type is larger than the `int` type. Since all of the members
of a union occupy the same memory space, the union data type size
doesn’t need to be large enough to hold the sum of all their sizes; it
just needs to be large enough to hold the largest member.

------------------------------------------------------------------------

<span id="Structures"></span>

<div class="header">

Next: <a href="#Arrays" accesskey="n" rel="next">Arrays</a>, Previous:
<a href="#Unions" accesskey="p" rel="prev">Unions</a>, Up:
<a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Structures-1"></span>

### 2.4 Structures

<span id="index-structures"></span>
<span id="index-types_002c-structure"></span>
<span id="index-data-types_002c-structure"></span>

A structure is a programmer-defined data type made up of variables of
other data types (possibly including other structure types).

|  |  |  |
|:---|----|:---|
| • <a href="#Defining-Structures" accesskey="1">Defining Structures</a>: |    |  |
| • <a href="#Declaring-Structure-Variables" accesskey="2">Declaring
Structure Variables</a>: |    |  |
| • <a href="#Accessing-Structure-Members" accesskey="3">Accessing Structure
Members</a>: |    |  |
| • <a href="#Bit-Fields" accesskey="4">Bit Fields</a>: |    |  |
| • <a href="#Size-of-Structures" accesskey="5">Size of Structures</a>: |    |  |

------------------------------------------------------------------------

<span id="Defining-Structures"></span>

<div class="header">

Next: <a href="#Declaring-Structure-Variables" accesskey="n"
rel="next">Declaring Structure Variables</a>, Up:
<a href="#Structures" accesskey="u" rel="up">Structures</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Defining-Structures-1"></span>

#### 2.4.1 Defining Structures

<span id="index-defining-structures"></span>
<span id="index-structures_002c-defining"></span>

You define a structure using the `struct` keyword followed by the
declarations of the structure’s members, enclosed in braces. You declare
each member of a structure just as you would normally declare a
variable—using the data type followed by one or more variable names
separated by commas, and ending with a semicolon. Then end the structure
definition with a semicolon after the closing brace.

You should also include a name for the structure in between the `struct`
keyword and the opening brace. This is optional, but if you leave it
out, you can’t refer to that structure data type later on (without a
`typedef`, see [The typedef Statement](#The-typedef-Statement)).

Here is an example of defining a simple structure for holding the X and
Y coordinates of a point:

<div class="example">

``` example
struct point
  {
    int x, y;
  };
```

</div>

That defines a structure type named `struct point`, which contains two
members, `x` and `y`, both of which are of type `int`.

Structures (and unions) may contain instances of other structures and
unions, but of course not themselves. It is possible for a structure or
union type to contain a field which is a pointer to the same type (see
[Incomplete Types](#Incomplete-Types)).

------------------------------------------------------------------------

<span id="Declaring-Structure-Variables"></span>

<div class="header">

Next: <a href="#Accessing-Structure-Members" accesskey="n"
rel="next">Accessing Structure Members</a>, Previous:
<a href="#Defining-Structures" accesskey="p" rel="prev">Defining
Structures</a>, Up:
<a href="#Structures" accesskey="u" rel="up">Structures</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Structure-Variables-1"></span>

#### 2.4.2 Declaring Structure Variables

<span id="index-declaring-structure-variables"></span>
<span id="index-structure-variables_002c-declaring"></span>

You can declare variables of a structure type when both you initially
define the structure and after the definition, provided you gave the
structure type a name.

|  |  |  |
|:---|----|:---|
| • <a href="#Declaring-Structure-Variables-at-Definition"
accesskey="1">Declaring Structure Variables at Definition</a>: |    |  |
| • <a href="#Declaring-Structure-Variables-After-Definition"
accesskey="2">Declaring Structure Variables After Definition</a>: |    |  |
| • <a href="#Initializing-Structure-Members" accesskey="3">Initializing
Structure Members</a>: |    |  |

------------------------------------------------------------------------

<span id="Declaring-Structure-Variables-at-Definition"></span>

<div class="header">

Next:
<a href="#Declaring-Structure-Variables-After-Definition" accesskey="n"
rel="next">Declaring Structure Variables After Definition</a>, Up:
<a href="#Declaring-Structure-Variables" accesskey="u"
rel="up">Declaring Structure Variables</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Structure-Variables-at-Definition-1"></span>

#### 2.4.2.1 Declaring Structure Variables at Definition

<span id="index-declaring-structure-variables-at-definition"></span>
<span id="index-structure-variables_002c-declaring-at-definition"></span>

You can declare variables of a structure type when you define the
structure type by putting the variable names after the closing brace of
the structure definition, but before the final semicolon. You can
declare more than one such variable by separating the names with commas.

<div class="example">

``` example
struct point
  {
    int x, y;
  } first_point, second_point;
```

</div>

That example declares two variables of type `struct point`,
`first_point` and `second_point`.

------------------------------------------------------------------------

<span id="Declaring-Structure-Variables-After-Definition"></span>

<div class="header">

Next: <a href="#Initializing-Structure-Members" accesskey="n"
rel="next">Initializing Structure Members</a>, Previous:
<a href="#Declaring-Structure-Variables-at-Definition" accesskey="p"
rel="prev">Declaring Structure Variables at Definition</a>, Up:
<a href="#Declaring-Structure-Variables" accesskey="u"
rel="up">Declaring Structure Variables</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Structure-Variables-After-Definition-1"></span>

#### 2.4.2.2 Declaring Structure Variables After Definition

<span id="index-declaring-structure-variables-after-definition"></span>
<span id="index-structure-variables_002c-declaring-after-definition"></span>

You can declare variables of a structure type after defining the
structure by using the `struct` keyword and the name you gave the
structure type, followed by one or more variable names separated by
commas.

<div class="example">

``` example
struct point
  {
    int x, y;
  };
struct point first_point, second_point;
```

</div>

That example declares two variables of type `struct point`,
`first_point` and `second_point`.

------------------------------------------------------------------------

<span id="Initializing-Structure-Members"></span>

<div class="header">

Previous:
<a href="#Declaring-Structure-Variables-After-Definition" accesskey="p"
rel="prev">Declaring Structure Variables After Definition</a>, Up:
<a href="#Declaring-Structure-Variables" accesskey="u"
rel="up">Declaring Structure Variables</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Initializing-Structure-Members-1"></span>

#### 2.4.2.3 Initializing Structure Members

<span id="index-initializing-structure-members"></span>
<span id="index-structure-members_002c-initializing"></span>

You can initialize the members of a structure type to have certain
values when you declare structure variables.

If you do not initialize a structure variable, the effect depends on
whether it has static storage (see [Storage Class
Specifiers](#Storage-Class-Specifiers)) or not. If it is, members with
integral types are initialized with 0 and pointer members are
initialized to NULL; otherwise, the value of the structure’s members is
indeterminate.

One way to initialize a structure is to specify the values in a set of
braces and separated by commas. Those values are assigned to the
structure members in the same order that the members are declared in the
structure in definition.

<div class="example">

``` example
struct point
  {
    int x, y;
  };
struct point first_point = { 5, 10 };
```

</div>

In that example, the `x` member of `first_point` gets the value 5, and
the `y` member gets the value 10.

Another way to initialize the members is to specify the name of the
member to initialize. This way, you can initialize the members in any
order you like, and even leave some of them uninitialized. There are two
methods that you can use. The first method is available in C99 and as a
C89 extension in GCC:

<div class="example">

``` example
struct point first_point = { .y = 10, .x = 5 };
```

</div>

You can also omit the period and use a colon instead of ‘`=`’, though
this is a GNU C extension:

<div class="example">

``` example
struct point first_point = { y: 10, x: 5 };
```

</div>

You can also initialize the structure variable’s members when you
declare the variable during the structure definition:

<div class="example">

``` example
struct point
  {
    int x, y;
  } first_point = { 5, 10 };
```

</div>

You can also initialize fewer than all of a structure variable’s
members:

<div class="example">

``` example
struct pointy
  {
    int x, y;
    char *p;
  };
struct pointy first_pointy = { 5 };
```

</div>

Here, `x` is initialized with 5, `y` is initialized with 0, and `p` is
initialized with NULL. The rule here is that `y` and `p` are initialized
just as they would be if they were static variables.

Here is another example that initializes a structure’s members which are
structure variables themselves:

<div class="example">

``` example
struct point
  {
    int x, y;
  };

struct rectangle
  {
    struct point top_left, bottom_right;
  };

struct rectangle my_rectangle = { {0, 5}, {10, 0} };
```

</div>

That example defines the `rectangle` structure to consist of two `point`
structure variables. Then it declares one variable of type
`struct rectangle` and initializes its members. Since its members are
structure variables, we used an extra set of braces surrounding the
members that belong to the `point` structure variables. However, those
extra braces are not necessary; they just make the code easier to read.

------------------------------------------------------------------------

<span id="Accessing-Structure-Members"></span>

<div class="header">

Next: <a href="#Bit-Fields" accesskey="n" rel="next">Bit Fields</a>,
Previous: <a href="#Declaring-Structure-Variables" accesskey="p"
rel="prev">Declaring Structure Variables</a>, Up:
<a href="#Structures" accesskey="u" rel="up">Structures</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Accessing-Structure-Members-1"></span>

#### 2.4.3 Accessing Structure Members

<span id="index-accessing-structure-members"></span>
<span id="index-structure-members_002c-accessing"></span>

You can access the members of a structure variable using the member
access operator. You put the name of the structure variable on the left
side of the operator, and the name of the member on the right side.

<div class="example">

``` example
struct point
  {
    int x, y;
  };

struct point first_point;

first_point.x = 0;
first_point.y = 5;
```

</div>

You can also access the members of a structure variable which is itself
a member of a structure variable.

<div class="example">

``` example
struct rectangle
  {
    struct point top_left, bottom_right;
  };

struct rectangle my_rectangle;

my_rectangle.top_left.x = 0;
my_rectangle.top_left.y = 5;

my_rectangle.bottom_right.x = 10;
my_rectangle.bottom_right.y = 0;
```

</div>

------------------------------------------------------------------------

<span id="Bit-Fields"></span>

<div class="header">

Next: <a href="#Size-of-Structures" accesskey="n" rel="next">Size of
Structures</a>, Previous:
<a href="#Accessing-Structure-Members" accesskey="p"
rel="prev">Accessing Structure Members</a>, Up:
<a href="#Structures" accesskey="u" rel="up">Structures</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Bit-Fields-1"></span>

#### 2.4.4 Bit Fields

<span id="index-bit-fields"></span>
<span id="index-fields_002c-bit"></span>

You can create structures with integer members of nonstandard sizes,
called *bit fields*. You do this by specifying an integer (`int`,
`char`, `long int`, etc.) member as usual, and inserting a colon and the
number of bits that the member should occupy in between the member’s
name and the semicolon.

<div class="example">

``` example
struct card
  {
    unsigned int suit : 2;
    unsigned int face_value : 4;
  };
```

</div>

That example defines a structure type with two bit fields, `suit` and
`face_value`, which take up 2 bits and 4 bits, respectively. `suit` can
hold values from 0 to 3, and `face_value` can hold values from 0 to 15.
Notice that these bit fields were declared as `unsigned int`; had they
been signed integers, then their ranges would have been from -2 to 1,
and from -8 to 7, respectively.

More generally, the range of an unsigned bit field of *N* bits is from 0
to *2^N - 1*, and the range of a signed bit field of *N* bits is from
*-(2^N) / 2* to *((2^N) / 2) - 1*.

Bit fields can be specified without a name in order to control which
actual bits within the containing unit are used. However, the effect of
this is not very portable and it is rarely useful. You can also specify
a bit field of size 0, which indicates that subsequent bit fields not
further bit fields should be packed into the unit containing the
previous bit field. This is likewise not generally useful.

You may not take the address of a bit field with the address operator
`&` (see [Pointer Operators](#Pointer-Operators)).

------------------------------------------------------------------------

<span id="Size-of-Structures"></span>

<div class="header">

Previous: <a href="#Bit-Fields" accesskey="p" rel="prev">Bit Fields</a>,
Up: <a href="#Structures" accesskey="u" rel="up">Structures</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Size-of-Structures-1"></span>

#### 2.4.5 Size of Structures

<span id="index-size-of-structures"></span>
<span id="index-structures_002c-size-of"></span>

The size of a structure type is equal to the sum of the size of all of
its members, possibly including padding to cause the structure type to
align to a particular byte boundary. The details vary depending on your
computer platform, but it would not be atypical to see structures padded
to align on four- or eight-byte boundaries. This is done in order to
speed up memory accesses of instances of the structure type.

As a GNU extension, GCC allows structures with no members. Such
structures have zero size.

If you wish to explicitly omit padding from your structure types (which
may, in turn, decrease the speed of structure memory accesses), then GCC
provides multiple methods of turning packing off. The quick and easy
method is to use the `-fpack-struct` compiler option. For more details
on omitting packing, please see the GCC manual which corresponds to your
version of the compiler.

------------------------------------------------------------------------

<span id="Arrays"></span>

<div class="header">

Next: <a href="#Pointers" accesskey="n" rel="next">Pointers</a>,
Previous: <a href="#Structures" accesskey="p" rel="prev">Structures</a>,
Up: <a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Arrays-1"></span>

### 2.5 Arrays

<span id="index-arrays"></span>
<span id="index-types_002c-array"></span>
<span id="index-data-types_002c-array"></span>

An array is a data structure that lets you store one or more elements
consecutively in memory. In C, array elements are indexed beginning at
position zero, not one.

|  |  |  |
|:---|----|:---|
| • <a href="#Declaring-Arrays" accesskey="1">Declaring Arrays</a>: |    |  |
| • <a href="#Initializing-Arrays" accesskey="2">Initializing Arrays</a>: |    |  |
| • <a href="#Accessing-Array-Elements" accesskey="3">Accessing Array
Elements</a>: |    |  |
| • <a href="#Multidimensional-Arrays" accesskey="4">Multidimensional
Arrays</a>: |    |  |
| • <a href="#Arrays-as-Strings" accesskey="5">Arrays as Strings</a>: |    |  |
| • <a href="#Arrays-of-Unions" accesskey="6">Arrays of Unions</a>: |    |  |
| • <a href="#Arrays-of-Structures" accesskey="7">Arrays of Structures</a>: |    |  |

------------------------------------------------------------------------

<span id="Declaring-Arrays"></span>

<div class="header">

Next:
<a href="#Initializing-Arrays" accesskey="n" rel="next">Initializing
Arrays</a>, Up: <a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Arrays-1"></span>

#### 2.5.1 Declaring Arrays

<span id="index-declaring-arrays"></span>
<span id="index-arrays_002c-declaring"></span>

You declare an array by specifying the data type for its elements, its
name, and the number of elements it can store. Here is an example that
declares an array that can store ten integers:

<div class="example">

``` example
int my_array[10];
```

</div>

For standard C code, the number of elements in an array must be
positive.

As a GNU extension, the number of elements can be as small as zero.
Zero-length arrays are useful as the last element of a structure which
is really a header for a variable-length object:

<div class="example">

``` example
struct line
{
  int length;
  char contents[0];
};

{
  struct line *this_line = (struct line *)
    malloc (sizeof (struct line) + this_length);
  this_line -> length = this_length;
}
```

</div>

Another GNU extension allows you to declare an array size using
variables, rather than only constants. For example, here is a function
definition that declares an array using its parameter as the number of
elements:

<div class="example">

``` example
int
my_function (int number)
{
  int my_array[number];
  …;
}
```

</div>

------------------------------------------------------------------------

<span id="Initializing-Arrays"></span>

<div class="header">

Next:
<a href="#Accessing-Array-Elements" accesskey="n" rel="next">Accessing
Array Elements</a>, Previous:
<a href="#Declaring-Arrays" accesskey="p" rel="prev">Declaring
Arrays</a>, Up: <a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Initializing-Arrays-1"></span>

#### 2.5.2 Initializing Arrays

<span id="index-initializing-arrays"></span>
<span id="index-arrays_002c-initializing"></span>

You can initialize the elements in an array when you declare it by
listing the initializing values, separated by commas, in a set of
braces. Here is an example:

<div class="example">

``` example
int my_array[5] = { 0, 1, 2, 3, 4 };
```

</div>

You don’t have to explicitly initialize all of the array elements. For
example, this code initializes the first three elements as specified,
and then initializes the last two elements to a default value of zero:

<div class="example">

``` example
int my_array[5] = { 0, 1, 2 };
```

</div>

When using either ISO C99, or C89 with GNU extensions, you can
initialize array elements out of order, by specifying which array
indices to initialize. To do this, include the array index in brackets,
and optionally the assignment operator, before the value. Here is an
example:

<div class="example">

``` example
int my_array[5] = { [2] 5, [4] 9 };
```

</div>

Or, using the assignment operator:

<div class="example">

``` example
int my_array[5] = { [2] = 5, [4] = 9 };
```

</div>

Both of those examples are equivalent to:

<div class="example">

``` example
int my_array[5] = { 0, 0, 5, 0, 9 };
```

</div>

When using GNU extensions, you can initialize a range of elements to the
same value, by specifying the first and last indices, in the form
` [``first``] ... [``last``] `. Here is an example:

<div class="example">

``` example
int new_array[100] = { [0 ... 9] = 1, [10 ... 98] = 2, 3 };
```

</div>

That initializes elements 0 through 9 to 1, elements 10 through 98 to 2,
and element 99 to 3. (You also could explicitly write `[99] = 3`.) Also,
notice that you *must* have spaces on both sides of the ‘`...`’.

If you initialize every element of an array, then you do not have to
specify its size; its size is determined by the number of elements you
initialize. Here is an example:

<div class="example">

``` example
int my_array[] = { 0, 1, 2, 3, 4 };
```

</div>

Although this does not explicitly state that the array has five elements
using `my_array[5]`, it initializes five elements, so that is how many
it has.

Alternately, if you specify which elements to initialize, then the size
of the array is equal to the highest element number initialized, plus
one. For example:

<div class="example">

``` example
int my_array[] = { 0, 1, 2, [99] = 99 };
```

</div>

In that example, only four elements are initialized, but the last one
initialized is element number 99, so there are 100 elements.

------------------------------------------------------------------------

<span id="Accessing-Array-Elements"></span>

<div class="header">

Next: <a href="#Multidimensional-Arrays" accesskey="n"
rel="next">Multidimensional Arrays</a>, Previous:
<a href="#Initializing-Arrays" accesskey="p" rel="prev">Initializing
Arrays</a>, Up: <a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Accessing-Array-Elements-1"></span>

#### 2.5.3 Accessing Array Elements

<span id="index-accessing-array-elements"></span>
<span id="index-array-elements_002c-accessing"></span>

You can access the elements of an array by specifying the array name,
followed by the element index, enclosed in brackets. Remember that the
array elements are numbered starting with zero. Here is an example:

<div class="example">

``` example
my_array[0] = 5;
```

</div>

That assigns the value 5 to the first element in the array, at position
zero. You can treat individual array elements like variables of whatever
data type the array is made up of. For example, if you have an array
made of a structure data type, you can access the structure elements
like this:

<div class="example">

``` example
struct point
{
  int x, y;
};
struct point point_array[2] = { {4, 5}, {8, 9} };
point_array[0].x = 3;
```

</div>

------------------------------------------------------------------------

<span id="Multidimensional-Arrays"></span>

<div class="header">

Next: <a href="#Arrays-as-Strings" accesskey="n" rel="next">Arrays as
Strings</a>, Previous:
<a href="#Accessing-Array-Elements" accesskey="p" rel="prev">Accessing
Array Elements</a>, Up:
<a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Multidimensional-Arrays-1"></span>

#### 2.5.4 Multidimensional Arrays

<span id="index-multidimensional-arrays"></span>
<span id="index-arrays_002c-multidimensional"></span>

You can make multidimensional arrays, or “arrays of arrays”. You do this
by adding an extra set of brackets and array lengths for every
additional dimension you want your array to have. For example, here is a
declaration for a two-dimensional array that holds five elements in each
dimension (a two-element array consisting of five-element arrays):

<div class="example">

``` example
int two_dimensions[2][5] { {1, 2, 3, 4, 5}, {6, 7, 8, 9, 10} };
```

</div>

Multidimensional array elements are accessed by specifying the desired
index of both dimensions:

<div class="example">

``` example
two_dimensions[1][3] = 12;
```

</div>

In our example, `two_dimensions[0]` is itself an array. The element
`two_dimensions[0][2]` is followed by `two_dimensions[0][3]`, not by
`two_dimensions[1][2]`.

------------------------------------------------------------------------

<span id="Arrays-as-Strings"></span>

<div class="header">

Next: <a href="#Arrays-of-Unions" accesskey="n" rel="next">Arrays of
Unions</a>, Previous: <a href="#Multidimensional-Arrays" accesskey="p"
rel="prev">Multidimensional Arrays</a>, Up:
<a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Arrays-as-Strings-1"></span>

#### 2.5.5 Arrays as Strings

<span id="index-arrays-as-strings"></span>
<span id="index-strings_002c-arrays-as"></span>

You can use an array of characters to hold a string (see [String
Constants](#String-Constants)). The array may be built of either signed
or unsigned characters.

<span id="index-string-arrays_002c-declaring"></span>
<span id="index-declaring-string-arrays"></span>

When you declare the array, you can specify the number of elements it
will have. That number will be the maximum number of characters that
should be in the string, including the null character used to end the
string. If you choose this option, then you do not have to initialize
the array when you declare it. Alternately, you can simply initialize
the array to a value, and its size will then be exactly large enough to
hold whatever string you used to initialize it.

<span id="index-string-arrays_002c-initializing"></span>
<span id="index-initializing-string-arrays"></span>

There are two different ways to initialize the array. You can specify of
comma-delimited list of characters enclosed in braces, or you can
specify a string literal enclosed in double quotation marks.

Here are some examples:

<div class="example">

``` example
char blue[26];
char yellow[26] = {'y', 'e', 'l', 'l', 'o', 'w', '\0'};
char orange[26] = "orange";
char gray[] = {'g', 'r', 'a', 'y', '\0'};
char salmon[] = "salmon";
```

</div>

In each of these cases, the null character `\0` is included at the end
of the string, even when not explicitly stated. (Note that if you
initialize a string using an array of individual characters, then the
null character is *not* guaranteed to be present. It might be, but such
an occurrence would be one of chance, and should not be relied upon.)

After initialization, you cannot assign a new string literal to an array
using the assignment operator. For example, this *will not work*:

<div class="example">

``` example
char lemon[26] = "custard";
lemon = "steak sauce";      /* Fails! */
```

</div>

However, there are functions in the GNU C library that perform
operations (including copy) on string arrays. You can also change one
character at a time, by accessing individual string elements as you
would any other array:

<div class="example">

``` example
char name[] = "bob";
name[0] = 'r';
```

</div>

It is possible for you to explicitly state the number of elements in the
array, and then initialize it using a string that has more characters
than there are elements in the array. This is not a good thing. The
larger string will *not* override the previously specified size of the
array, and you will get a compile-time warning. Since the original array
size remains, any part of the string that exceeds that original size is
being written to a memory location that was not allocated for it.

------------------------------------------------------------------------

<span id="Arrays-of-Unions"></span>

<div class="header">

Next: <a href="#Arrays-of-Structures" accesskey="n" rel="next">Arrays of
Structures</a>, Previous:
<a href="#Arrays-as-Strings" accesskey="p" rel="prev">Arrays as
Strings</a>, Up: <a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Arrays-of-Unions-1"></span>

#### 2.5.6 Arrays of Unions

<span id="index-arrays-of-unions"></span>
<span id="index-unions_002c-arrays-of"></span>

You can create an array of a union type just as you can an array of a
primitive data type.

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
union numbers number_array [3];
```

</div>

That example creates a 3-element array of `union numbers` variables
called `number_array`. You can also initialize the first members of the
elements of a number array:

<div class="example">

``` example
union numbers number_array [3] = { {3}, {4}, {5} };
```

</div>

The additional inner grouping braces are optional.

After initialization, you can still access the union members in the
array using the member access operator. You put the array name and
element number (enclosed in brackets) to the left of the operator, and
the member name to the right.

<div class="example">

``` example
union numbers number_array [3];
number_array[0].i = 2;
```

</div>

------------------------------------------------------------------------

<span id="Arrays-of-Structures"></span>

<div class="header">

Previous: <a href="#Arrays-of-Unions" accesskey="p" rel="prev">Arrays of
Unions</a>, Up: <a href="#Arrays" accesskey="u" rel="up">Arrays</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Arrays-of-Structures-1"></span>

#### 2.5.7 Arrays of Structures

<span id="index-arrays-of-structures"></span>
<span id="index-structures_002c-arrays-of"></span>

You can create an array of a structure type just as you can an array of
a primitive data type.

<div class="example">

``` example
struct point
  {
    int x, y;
  };
struct point point_array [3];
```

</div>

That example creates a 3-element array of `struct point` variables
called `point_array`. You can also initialize the elements of a
structure array:

<div class="example">

``` example
struct point point_array [3] = { {2, 3}, {4, 5}, {6, 7} };
```

</div>

As with initializing structures which contain structure members, the
additional inner grouping braces are optional. But, if you use the
additional braces, then you can partially initialize some of the
structures in the array, and fully initialize others:

<div class="example">

``` example
struct point point_array [3] = { {2}, {4, 5}, {6, 7} };
```

</div>

In that example, the first element of the array has only its `x` member
initialized. Because of the grouping braces, the value 4 is assigned to
the `x` member of the second array element, *not* to the `y` member of
the first element, as would be the case without the grouping braces.

After initialization, you can still access the structure members in the
array using the member access operator. You put the array name and
element number (enclosed in brackets) to the left of the operator, and
the member name to the right.

<div class="example">

``` example
struct point point_array [3];
point_array[0].x = 2;
point_array[0].y = 3;
```

</div>

------------------------------------------------------------------------

<span id="Pointers"></span>

<div class="header">

Next: <a href="#Incomplete-Types" accesskey="n" rel="next">Incomplete
Types</a>, Previous:
<a href="#Arrays" accesskey="p" rel="prev">Arrays</a>, Up:
<a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Pointers-1"></span>

### 2.6 Pointers

<span id="index-pointers"></span>
<span id="index-types_002c-pointer"></span>
<span id="index-data-types_002c-pointer"></span>

Pointers hold memory addresses of stored constants or variables. For any
data type, including both primitive types and custom types, you can
create a pointer that holds the memory address of an instance of that
type.

|  |  |  |
|:---|----|:---|
| • <a href="#Declaring-Pointers" accesskey="1">Declaring Pointers</a>: |    |  |
| • <a href="#Initializing-Pointers" accesskey="2">Initializing Pointers</a>: |    |  |
| • <a href="#Pointers-to-Unions" accesskey="3">Pointers to Unions</a>: |    |  |
| • <a href="#Pointers-to-Structures" accesskey="4">Pointers to
Structures</a>: |    |  |

------------------------------------------------------------------------

<span id="Declaring-Pointers"></span>

<div class="header">

Next:
<a href="#Initializing-Pointers" accesskey="n" rel="next">Initializing
Pointers</a>, Up:
<a href="#Pointers" accesskey="u" rel="up">Pointers</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Declaring-Pointers-1"></span>

#### 2.6.1 Declaring Pointers

<span id="index-declaring-pointers"></span>
<span id="index-pointers_002c-declaring"></span>

You declare a pointer by specifying a name for it and a data type. The
data type indicates of what type of variable the pointer will hold
memory addresses.

To declare a pointer, include the indirection operator (see [Pointer
Operators](#Pointer-Operators)) before the identifier. Here is the
general form of a pointer declaration:

<div class="example">

``` example
data-type * name;
```

</div>

White space is not significant around the indirection operator:

<div class="example">

``` example
data-type *name;
data-type* name;
```

</div>

Here is an example of declaring a pointer to hold the address of an
`int` variable:

<div class="example">

``` example
int *ip;
```

</div>

Be careful, though: when declaring multiple pointers in the same
statement, you must explicitly declare each as a pointer, using the
indirection operator:

<div class="example">

``` example
int *foo, *bar;  /* Two pointers. */
int *baz, quux;   /* A pointer and an integer variable. */
```

</div>

------------------------------------------------------------------------

<span id="Initializing-Pointers"></span>

<div class="header">

Next: <a href="#Pointers-to-Unions" accesskey="n" rel="next">Pointers to
Unions</a>, Previous:
<a href="#Declaring-Pointers" accesskey="p" rel="prev">Declaring
Pointers</a>, Up:
<a href="#Pointers" accesskey="u" rel="up">Pointers</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Initializing-Pointers-1"></span>

#### 2.6.2 Initializing Pointers

<span id="index-initializing-pointers"></span>
<span id="index-pointers_002c-initializing"></span>

You can initialize a pointer when you first declare it by specifying a
variable address to store in it. For example, the following code
declares an `int` variable ‘`i`’, and a pointer which is initialized
with the address of ‘`i`’:

<div class="example">

``` example
int i;
int *ip = &i;
```

</div>

Note the use of the address operator (see [Pointer
Operators](#Pointer-Operators)), used to get the memory address of a
variable. After you declare a pointer, you do *not* use the indirection
operator with the pointer’s name when assigning it a new address to
point to. On the contrary, that would change the value of the variable
that the points to, not the value of the pointer itself. For example:

<div class="example">

``` example
int i, j;
int *ip = &i;  /* ‘ip’ now holds the address of ‘i’. */
ip = &j;       /* ‘ip’ now holds the address of ‘j’. */
*ip = &i;      /* ‘j’ now holds the address of ‘i’. */
```

</div>

The value stored in a pointer is an integral number: a location within
the computer’s memory space. If you are so inclined, you can assign
pointer values explicitly using literal integers, casting them to the
appropriate pointer type. However, we do not recommend this practice
unless you need to have extremely fine-tuned control over what is stored
in memory, and you know exactly what you are doing. It would be all too
easy to accidentally overwrite something that you did not intend to.
Most uses of this technique are also non-portable.

It is important to note that if you do not initialize a pointer with the
address of some other existing object, it points nowhere in particular
and will likely make your program crash if you use it (formally, this
kind of thing is called *undefined behavior*).

------------------------------------------------------------------------

<span id="Pointers-to-Unions"></span>

<div class="header">

Next:
<a href="#Pointers-to-Structures" accesskey="n" rel="next">Pointers to
Structures</a>, Previous:
<a href="#Initializing-Pointers" accesskey="p" rel="prev">Initializing
Pointers</a>, Up:
<a href="#Pointers" accesskey="u" rel="up">Pointers</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Pointers-to-Unions-1"></span>

#### 2.6.3 Pointers to Unions

<span id="index-pointers-to-unions"></span>
<span id="index-unions_002c-pointers-to"></span>

You can create a pointer to a union type just as you can a pointer to a
primitive data type.

<div class="example">

``` example
union numbers
  {
    int i;
    float f;
  };
union numbers foo = {4};
union numbers *number_ptr = &foo;
```

</div>

That example creates a new union type, `union numbers`, and declares
(and initializes the first member of) a variable of that type named
`foo`. Finally, it declares a pointer to the type `union numbers`, and
gives it the address of `foo`.

You can access the members of a union variable through a pointer, but
you can’t use the regular member access operator anymore. Instead, you
have to use the indirect member access operator (see [Member Access
Expressions](#Member-Access-Expressions)). Continuing with the previous
example, the following example will change the value of the first member
of `foo`:

<div class="example">

``` example
number_ptr -> i = 450;
```

</div>

Now the `i` member in `foo` is 450.

------------------------------------------------------------------------

<span id="Pointers-to-Structures"></span>

<div class="header">

Previous:
<a href="#Pointers-to-Unions" accesskey="p" rel="prev">Pointers to
Unions</a>, Up: <a href="#Pointers" accesskey="u" rel="up">Pointers</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Pointers-to-Structures-1"></span>

#### 2.6.4 Pointers to Structures

<span id="index-pointers-to-structures"></span>
<span id="index-structures_002c-pointers-to"></span>

You can create a pointer to a structure type just as you can a pointer
to a primitive data type.

<div class="example">

``` example
struct fish
  {
    float length, weight;
  };
struct fish salmon = {4.3, 5.8};
struct fish *fish_ptr = &salmon;
```

</div>

That example creates a new structure type, `struct fish`, and declares
(and initializes) a variable of that type named `salmon`. Finally, it
declares a pointer to the type `struct fish`, and gives it the address
of `salmon`.

You can access the members of a structure variable through a pointer,
but you can’t use the regular member access operator anymore. Instead,
you have to use the indirect member access operator (see [Member Access
Expressions](#Member-Access-Expressions)). Continuing with the previous
example, the following example will change the values of the members of
`salmon`:

<div class="example">

``` example
fish_ptr -> length = 5.1;
fish_ptr -> weight = 6.2;
```

</div>

Now the `length` and `width` members in `salmon` are 5.1 and 6.2,
respectively.

------------------------------------------------------------------------

<span id="Incomplete-Types"></span>

<div class="header">

Next:
<a href="#Type-Qualifiers" accesskey="n" rel="next">Type Qualifiers</a>,
Previous: <a href="#Pointers" accesskey="p" rel="prev">Pointers</a>, Up:
<a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Incomplete-Types-1"></span>

### 2.7 Incomplete Types

<span id="index-incomplete-types"></span>
<span id="index-types_002c-incomplete"></span>
<span id="index-structures_002c-incomplete"></span>
<span id="index-enumerations_002c-incomplete"></span>
<span id="index-unions_002c-incomplete"></span>

You can define structures, unions, and enumerations without listing
their members (or values, in the case of enumerations). Doing so results
in an incomplete type. You can’t declare variables of incomplete types,
but you can work with pointers to those types.

<div class="example">

``` example
struct point;
```

</div>

At some time later in your program you will want to complete the type.
You do this by defining it as you usually would:

<div class="example">

``` example
struct point
  {
    int x, y;
  };
```

</div>

This technique is commonly used to for linked lists:

<div class="example">

``` example
struct singly_linked_list
  {
    struct singly_linked_list *next;
    int x;
    /* other members here perhaps */
  };
struct singly_linked_list *list_head;
```

</div>

------------------------------------------------------------------------

<span id="Type-Qualifiers"></span>

<div class="header">

Next:
<a href="#Storage-Class-Specifiers" accesskey="n" rel="next">Storage
Class Specifiers</a>, Previous:
<a href="#Incomplete-Types" accesskey="p" rel="prev">Incomplete
Types</a>, Up:
<a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Type-Qualifiers-1"></span>

### 2.8 Type Qualifiers

<span id="index-type-qualifiers"></span>
<span id="index-qualifiers_002c-type"></span>
<span id="index-const-type-qualifier"></span>
<span id="index-volatile-type-qualifier"></span>

There are two type qualifiers that you can prepend to your variable
declarations which change how the variables may be accessed: `const` and
`volatile`.

`const` causes the variable to be read-only; after initialization, its
value may not be changed.

<div class="example">

``` example
const float pi = 3.14159f;
```

</div>

In addition to helping to prevent accidental value changes, declaring
variables with `const` can aid the compiler in code optimization.

`volatile` tells the compiler that the variable is explicitly
changeable, and seemingly useless accesses of the variable (for
instance, via pointers) should not be optimized away. You might use
`volatile` variables to store data that is updated via callback
functions or signal handlers. [Sequence Points and Signal
Delivery](#Sequence-Points-and-Signal-Delivery).

<div class="example">

``` example
volatile float currentTemperature = 40.0;
```

</div>

------------------------------------------------------------------------

<span id="Storage-Class-Specifiers"></span>

<div class="header">

Next:
<a href="#Renaming-Types" accesskey="n" rel="next">Renaming Types</a>,
Previous:
<a href="#Type-Qualifiers" accesskey="p" rel="prev">Type Qualifiers</a>,
Up: <a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Storage-Class-Specifiers-1"></span>

### 2.9 Storage Class Specifiers

<span id="index-storage-class-specifiers"></span>
<span id="index-specifiers_002c-storage-class"></span>
<span id="index-auto-storage-class-specifier"></span>
<span id="index-extern-storage-class-specifier"></span>
<span id="index-register-storage-class-specifier"></span>
<span id="index-static-storage-class-specifier"></span>

There are four storage class specifiers that you can prepend to your
variable declarations which change how the variables are stored in
memory: `auto`, `extern`, `register`, and `static`.

You use `auto` for variables which are local to a function, and whose
values should be discarded upon return from the function in which they
are declared. This is the default behavior for variables declared within
functions.

<div class="example">

``` example
void
foo (int value)
{
  auto int x = value;
  …
  return;
}
```

</div>

`register` is nearly identical in purpose to `auto`, except that it also
suggests to the compiler that the variable will be heavily used, and, if
possible, should be stored in a register. You cannot use the address-of
operator to obtain the address of a variable declared with `register`.
This means that you cannot refer to the elements of an array declared
with storage class `register`. In fact the only thing you can do with
such an array is measure its size with `sizeof`. GCC normally makes good
choices about which values to hold in registers, and so `register` is
not often used.

`static` is essentially the opposite of `auto`: when applied to
variables within a function or block, these variables will retain their
value even when the function or block is finished. This is known as
*static storage duration*.

<div class="example">

``` example
int
sum (int x)
{
  static int sumSoFar = 0;
  sumSoFar = sumSoFar + x;
  return sumSoFar;
}
```

</div>

You can also declare variables (or functions) at the top level (that is,
not inside a function) to be `static`; such variables are visible
(global) to the current source file (but not other source files). This
gives an unfortunate double meaning to `static`; this second meaning is
known as *static linkage*. Two functions or variables having static
linkage in separate files are entirely separate; neither is visible
outside the file in which it is declared.

Uninitialized variables that are declared as `extern` are given default
values of `0`, `0.0`, or `NULL`, depending on the type. Uninitialized
variables that are declared as `auto` or `register` (including the
default usage of `auto`) are left uninitialized, and hence should not be
assumed to hold any particular value.

`extern` is useful for declaring variables that you want to be visible
to all source files that are linked into your project. You cannot
initialize a variable in an `extern` declaration, as no space is
actually allocated during the declaration. You must make both an
`extern` declaration (typically in a header file that is included by the
other source files which need to access the variable) and a non-`extern`
declaration which is where space is actually allocated to store the
variable. The `extern` declaration may be repeated multiple times.

<div class="example">

``` example
extern int numberOfClients;

…

int numberOfClients = 0;
```

</div>

See [Program Structure and Scope](#Program-Structure-and-Scope), for
related information.

------------------------------------------------------------------------

<span id="Renaming-Types"></span>

<div class="header">

Previous:
<a href="#Storage-Class-Specifiers" accesskey="p" rel="prev">Storage
Class Specifiers</a>, Up:
<a href="#Data-Types" accesskey="u" rel="up">Data Types</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Renaming-Types-1"></span>

### 2.10 Renaming Types

<span id="index-renaming-types"></span>
<span id="index-types_002c-renaming"></span>

Sometimes it is convenient to give a new name to a type. You can do this
using the `typedef` statement. See [The typedef
Statement](#The-typedef-Statement), for more information.

------------------------------------------------------------------------

<span id="Expressions-and-Operators"></span>

<div class="header">

Next: <a href="#Statements" accesskey="n" rel="next">Statements</a>,
Previous: <a href="#Data-Types" accesskey="p" rel="prev">Data Types</a>,
Up: <a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Expressions-and-Operators-1"></span>

## 3 Expressions and Operators

|  |  |  |
|:---|----|:---|
| • <a href="#Expressions" accesskey="1">Expressions</a>: |    |  |
| • <a href="#Assignment-Operators" accesskey="2">Assignment Operators</a>: |    |  |
| • <a href="#Incrementing-and-Decrementing" accesskey="3">Incrementing and
Decrementing</a>: |    |  |
| • <a href="#Arithmetic-Operators" accesskey="4">Arithmetic Operators</a>: |    |  |
| • <a href="#Complex-Conjugation" accesskey="5">Complex Conjugation</a>: |    |  |
| • <a href="#Comparison-Operators" accesskey="6">Comparison Operators</a>: |    |  |
| • <a href="#Logical-Operators" accesskey="7">Logical Operators</a>: |    |  |
| • <a href="#Bit-Shifting" accesskey="8">Bit Shifting</a>: |    |  |
| • <a href="#Bitwise-Logical-Operators" accesskey="9">Bitwise Logical
Operators</a>: |    |  |
| • [Pointer Operators](#Pointer-Operators): |    |  |
| • [The sizeof Operator](#The-sizeof-Operator): |    |  |
| • [Type Casts](#Type-Casts): |    |  |
| • [Array Subscripts](#Array-Subscripts): |    |  |
| • [Function Calls as Expressions](#Function-Calls-as-Expressions): |    |  |
| • [The Comma Operator](#The-Comma-Operator): |    |  |
| • [Member Access Expressions](#Member-Access-Expressions): |    |  |
| • [Conditional Expressions](#Conditional-Expressions): |    |  |
| • [Statements and Declarations in Expressions](#Statements-and-Declarations-in-Expressions): |    |  |
| • [Operator Precedence](#Operator-Precedence): |    |  |
| • [Order of Evaluation](#Order-of-Evaluation): |    |  |

------------------------------------------------------------------------

<span id="Expressions"></span>

<div class="header">

Next:
<a href="#Assignment-Operators" accesskey="n" rel="next">Assignment
Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Expressions-1"></span>

### 3.1 Expressions

<span id="index-expressions"></span>

An *expression* consists of at least one operand and zero or more
operators. Operands are typed objects such as constants, variables, and
function calls that return values. Here are some examples:

<div class="example">

``` example
47
2 + 2
cosine(3.14159) /* We presume this returns a floating point value. */
```

</div>

Parentheses group subexpressions:

<div class="example">

``` example
( 2 * ( ( 3 + 10 ) - ( 2 * 6 ) ) )
```

</div>

Innermost expressions are evaluated first. In the above example,
`3 + 10` and `2 * 6` evaluate to `13` and `12`, respectively. Then `12`
is subtracted from `13`, resulting in `1`. Finally, `1` is multiplied by
`2`, resulting in `2`. The outermost parentheses are completely
optional.

<span id="index-operators"></span>

An *operator* specifies an operation to be performed on its operand(s).
Operators may have one, two, or three operands, depending on the
operator.

------------------------------------------------------------------------

<span id="Assignment-Operators"></span>

<div class="header">

Next: <a href="#Incrementing-and-Decrementing" accesskey="n"
rel="next">Incrementing and Decrementing</a>, Previous:
<a href="#Expressions" accesskey="p" rel="prev">Expressions</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Assignment-Operators-1"></span>

### 3.2 Assignment Operators

<span id="index-assignment-operators"></span>
<span id="index-operators_002c-assignment"></span>

Assignment operators store values in variables. C provides several
variations of assignment operators.

The standard assignment operator `=` simply stores the value of its
right operand in the variable specified by its left operand. As with all
assignment operators, the left operand (commonly referred to as the
“lvalue”) cannot be a literal or constant value.

<div class="example">

``` example
int x = 10;
float y = 45.12 + 2.0;
int z = (2 * (3 + function () ));

struct foo {
  int bar;
  int baz;
} quux = {3, 4};
```

</div>

Note that, unlike the other assignment operators described below, you
can use the plain assignment operator to store values of a structure
type.

Compound assignment operators perform an operation involving both the
left and right operands, and then assign the resulting expression to the
left operand. Here is a list of the compound assignment operators, and a
brief description of what they do:

- `+=`

  Adds the two operands together, and then assign the result of the
  addition to the left operand.

- `-=`

  Subtract the right operand from the left operand, and then assign the
  result of the subtraction to the left operand.

- `*=`

  Multiply the two operands together, and then assign the result of the
  multiplication to the left operand.

- `/=`

  Divide the left operand by the right operand, and assign the result of
  the division to the left operand.

- `%=`

  Perform modular division on the two operands, and assign the result of
  the division to the left operand.

- `<<=`

  Perform a left shift operation on the left operand, shifting by the
  number of bits specified by the right operand, and assign the result
  of the shift to the left operand.

- `>>=`

  Perform a right shift operation on the left operand, shifting by the
  number of bits specified by the right operand, and assign the result
  of the shift to the left operand.

- `&=`

  Perform a bitwise conjunction operation on the two operands, and
  assign the result of the operation to the left operand.

- `^=`

  Performs a bitwise exclusive disjunction operation on the two
  operands, and assign the result of the operation to the left operand.

- `|=`

  Performs a bitwise inclusive disjunction operation on the two
  operands, and assign the result of the operation to the left operand.

Here is an example of using one of the compound assignment operators:

<div class="example">

``` example
x += y;
```

</div>

Since there are no side effects wrought by evaluating the variable `x`
as an lvalue, the above code produces the same result as:

<div class="example">

``` example
x = x + y;
```

</div>

------------------------------------------------------------------------

<span id="Incrementing-and-Decrementing"></span>

<div class="header">

Next:
<a href="#Arithmetic-Operators" accesskey="n" rel="next">Arithmetic
Operators</a>, Previous:
<a href="#Assignment-Operators" accesskey="p" rel="prev">Assignment
Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Incrementing-and-Decrementing-1"></span>

### 3.3 Incrementing and Decrementing

<span id="index-increment-operator"></span>
<span id="index-decrement-operator"></span>
<span id="index-operator_002c-increment"></span>
<span id="index-operator_002c-decrement"></span>

The increment operator `++` adds 1 to its operand. The operand must be a
either a variable of one of the primitive data types, a pointer, or an
enumeration variable. You can apply the increment operator either before
or after the operand. Here are some examples:

<div class="example">

``` example
char w = '1';
int x = 5;
char y = 'B';
float z = 5.2;
int *p = &x;

++w;   /* w is now the character ‘2’ (not the value 2). */
x++;   /* x is now 6. */
++y;   /* y is now ‘C’ (on ASCII systems). */
z++;   /* z is now 6.2. */
++p;   /* p is now &x + sizeof(int). */
```

</div>

(Note that incrementing a pointer only makes sense if you have reason to
believe that the new pointer value will be a valid memory address.)

A prefix increment adds 1 before the operand is evaluated. A postfix
increment adds 1 after the operand is evaluated. In the previous
examples, changing the position of the operator would make no
difference. However, there are cases where it does make a difference:

<div class="example">

``` example
int x = 5;
printf ("%d \n", x++);    /* Print x and then increment it. */
/* x is now equal to 6. */
printf ("%d \n", ++x);    /* Increment x and then print it. */
```

</div>

The output of the above example is:

<div class="example">

``` example
5
7
```

</div>

Likewise, you can subtract 1 from an operand using the decrement
operator:

<div class="example">

``` example
int x = 5;

x--; /* x is now 4. */
```

</div>

The concepts of prefix and postfix application apply here as with the
increment operator.

------------------------------------------------------------------------

<span id="Arithmetic-Operators"></span>

<div class="header">

Next: <a href="#Complex-Conjugation" accesskey="n" rel="next">Complex
Conjugation</a>, Previous:
<a href="#Incrementing-and-Decrementing" accesskey="p"
rel="prev">Incrementing and Decrementing</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Arithmetic-Operators-1"></span>

### 3.4 Arithmetic Operators

<span id="index-arithmetic-operators"></span>
<span id="index-operators_002c-arithmetic"></span>

C provides operators for standard arithmetic operations: addition,
subtraction, multiplication, and division, along with modular division
and negation. Usage of these operators is straightforward; here are some
examples:

<div class="example">

``` example
/* Addition. */
x = 5 + 3;
y = 10.23 + 37.332;
quux_pointer = foo_pointer + bar_pointer;
```

</div>

<div class="example">

``` example
/* Subtraction. */
x = 5 - 3;
y = 57.223 - 10.903;
quux_pointer = foo_pointer - bar_pointer;
```

</div>

You can add and subtract memory pointers, but you cannot multiply or
divide them.

<div class="example">

``` example
/* Multiplication. */
x = 5 * 3;
y = 47.4 * 1.001;
```

</div>

<div class="example">

``` example
/* Division. */
x = 5 / 3;
y = 940.0 / 20.2;
```

</div>

Integer division of positive values truncates towards zero, so 5/3 is 1.
However, if either operand is negative, the direction of rounding is
implementation-defined. [Signed Integer
Division](#Signed-Integer-Division) for information about overflow in
signed integer division.

You use the modulus operator `%` to obtain the remainder produced by
dividing its two operands. You put the operands on either side of the
operator, and it does matter which operand goes on which side: `3 % 5`
and `5 % 3` do not have the same result. The operands must be
expressions of a primitive data type.

<div class="example">

``` example
/* Modular division. */
x = 5 % 3;
y = 74 % 47;
```

</div>

Modular division returns the remainder produced after performing integer
division on the two operands. The operands must be of a primitive
integer type.

<div class="example">

``` example
/* Negation. */
int x = -5;
float y = -3.14159;
```

</div>

If the operand you use with the negative operator is of an unsigned data
type, then the result cannot negative, but rather is the maximum value
of the unsigned data type, minus the value of the operand.

Many systems use twos-complement arithmetic, and on such systems the
most negative value a signed type can hold is further away from zero
than the most positive value. For example, on one platform, this
program:

<div class="example">

``` example
#include <limits.h>
#include <stdio.h>

int main (int argc, char *argv[]) 
{
  int x;
  x = INT_MAX;
  printf("INT_MAX  = %d\n", x);
  x = INT_MIN;
  printf("INT_MIN  = %d\n", x);
  x = -x;
  printf("-INT_MIN = %d\n", x);
  return 0;
}
```

</div>

Produces this output:

<div class="example">

``` example
INT_MAX  = 2147483647
INT_MIN  = -2147483648
-INT_MIN = -2147483648
```

</div>

Trivially, you can also apply a positive operator to a numeric
expression:

<div class="example">

``` example
int x = +42;
```

</div>

Numeric values are assumed to be positive unless explicitly made
negative, so this operator has no effect on program operation.

------------------------------------------------------------------------

<span id="Complex-Conjugation"></span>

<div class="header">

Next:
<a href="#Comparison-Operators" accesskey="n" rel="next">Comparison
Operators</a>, Previous:
<a href="#Arithmetic-Operators" accesskey="p" rel="prev">Arithmetic
Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Complex-Conjugation-1"></span>

### 3.5 Complex Conjugation

<span id="index-complex-conjugation"></span>
<span id="index-conjugation"></span>

As a GNU extension, you can use the complex conjugation operator `~` to
perform complex conjugation on its operand — that is, it reverses the
sign of its imaginary component. The operand must be an expression of a
complex number type. Here is an example:

<div class="example">

``` example
__complex__ int x = 5 + 17i;
 
printf ("%d  \n", (x * ~x));
```

</div>

Since an imaginary number *(a + bi)* multiplied by its conjugate is
equal to *a^2 + b^2*, the above `printf` statement will print 314, which
is equal to *25 + 289*.

------------------------------------------------------------------------

<span id="Comparison-Operators"></span>

<div class="header">

Next: <a href="#Logical-Operators" accesskey="n" rel="next">Logical
Operators</a>, Previous:
<a href="#Complex-Conjugation" accesskey="p" rel="prev">Complex
Conjugation</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Comparison-Operators-1"></span>

### 3.6 Comparison Operators

<span id="index-comparison-operators"></span>
<span id="index-operators_002c-comparison"></span>

You use the comparison operators to determine how two operands relate to
each other: are they equal to each other, is one larger than the other,
is one smaller than the other, and so on. When you use any of the
comparison operators, the result is either 1 or 0, meaning true or
false, respectively.

(In the following code examples, the variables `x` and `y` stand for any
two expressions of arithmetic types, or pointers.)

The equal-to operator `==` tests its two operands for equality. The
result is 1 if the operands are equal, and 0 if the operands are not
equal.

<div class="example">

``` example
if (x == y)
  puts ("x is equal to y");
else
  puts ("x is not equal to y");
```

</div>

The not-equal-to operator `!=` tests its two operands for inequality.
The result is 1 if the operands are not equal, and 0 if the operands
*are* equal.

<div class="example">

``` example
if (x != y)
  puts ("x is not equal to y");
else
  puts ("x is equal to y");
```

</div>

Comparing floating-point values for exact equality or inequality can
produce unexpected results. [Real Number Types](#Real-Number-Types) for
more information.

You can compare function pointers for equality or inequality; the
comparison tests if two function pointers point to the same function or
not.

Beyond equality and inequality, there are operators you can use to test
if one value is less than, greater than, less-than-or-equal-to, or
greater-than-or-equal-to another value. Here are some code samples that
exemplify usage of these operators:

<div class="example">

``` example
if (x < y)
  puts ("x is less than y");
```

</div>

<div class="example">

``` example
if (x <= y)
  puts ("x is less than or equal to y");
```

</div>

<div class="example">

``` example
if (x > y)
  puts ("x is greater than y");
```

</div>

<div class="example">

``` example
if (x >= y)
  puts ("x is greater than or equal to y");
```

</div>

------------------------------------------------------------------------

<span id="Logical-Operators"></span>

<div class="header">

Next: <a href="#Bit-Shifting" accesskey="n" rel="next">Bit Shifting</a>,
Previous:
<a href="#Comparison-Operators" accesskey="p" rel="prev">Comparison
Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Logical-Operators-1"></span>

### 3.7 Logical Operators

<span id="index-logical-operators"></span>

Logical operators test the truth value of a pair of operands. Any
nonzero expression is considered true in C, while an expression that
evaluates to zero is considered false.

The logical conjunction operator `&&` tests if two expressions are both
true. If the first expression is false, then the second expression is
not evaluated.

<div class="example">

``` example
if ((x == 5) && (y == 10))
  printf ("x is 5 and y is 10");
```

</div>

The logical disjunction operator `||` tests if at least one of two
expressions it true. If the first expression is true, then the second
expression is not evaluated.

<div class="example">

``` example
if ((x == 5) || (y == 10))
   printf ("x is 5 or y is 10");
```

</div>

You can prepend a logical expression with a negation operator `!` to
flip the truth value:

<div class="example">

``` example
if (!(x == 5))
  printf ("x is not 5");
```

</div>

Since the second operand in a logical expression pair is not necessarily
evaluated, you can write code with perhaps unintuitive results:

<div class="example">

``` example
if (foo && x++)
  bar();
```

</div>

If `foo` is ever zero, then not only would `bar` not be called, but `x`
would not be incremented. If you intend to increment `x` regardless of
the value of `foo`, you should do so outside of the conjunction
expression.

------------------------------------------------------------------------

<span id="Bit-Shifting"></span>

<div class="header">

Next:
<a href="#Bitwise-Logical-Operators" accesskey="n" rel="next">Bitwise
Logical Operators</a>, Previous:
<a href="#Logical-Operators" accesskey="p" rel="prev">Logical
Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Bit-Shifting-1"></span>

### 3.8 Bit Shifting

<span id="index-bit-shifting"></span> <span id="index-shifting"></span>

You use the left-shift operator `<<` to shift its first operand’s bits
to the left. The second operand denotes the number of bit places to
shift. Bits shifted off the left side of the value are discarded; new
bits added on the right side will all be 0.

<div class="example">

``` example
x = 47;    /* 47 is 00101111 in binary. */
x << 1;    /* 00101111 << 1 is 01011110. */
```

</div>

Similarly, you use the right-shift operator `>>` to shift its first
operand’s bits to the right. Bits shifted off the right side are
discarded; new bits added on the left side are *usually* 0, but if the
first operand is a signed negative value, then the added bits will be
either 0 *or* whatever value was previously in the leftmost bit
position.

<div class="example">

``` example
x = 47;   /* 47 is 00101111 in binary. */
x >> 1;   /* 00101111 >> 1 is 00010111. */
```

</div>

For both `<<` and `>>`, if the second operand is greater than the
bit-width of the first operand, or the second operand is negative, the
behavior is undefined.

You can use the shift operators to perform a variety of interesting
hacks. For example, given a date with the day of the month numbered as
`d`, the month numbered as `m`, and the year `y`, you can store the
entire date in a single number `x`:

<div class="example">

``` example
int d = 12;
int m = 6;
int y = 1983;
int x = (((y << 4) + m) << 5) + d;
```

</div>

You can then extract the original day, month, and year out of `x` using
a combination of shift operators and modular division:

<div class="example">

``` example
d = x % 32;
m = (x >> 5) % 16;
y = x >> 9;
```

</div>

------------------------------------------------------------------------

<span id="Bitwise-Logical-Operators"></span>

<div class="header">

Next: <a href="#Pointer-Operators" accesskey="n" rel="next">Pointer
Operators</a>, Previous:
<a href="#Bit-Shifting" accesskey="p" rel="prev">Bit Shifting</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Bitwise-Logical-Operators-1"></span>

### 3.9 Bitwise Logical Operators

<span id="index-bitwise-logical-operators"></span>
<span id="index-logical-operators_002c-bitwise"></span>

C provides operators for performing bitwise conjunction, inclusive
disjunction, exclusive disjunction, and negation (complement).

Biwise conjunction examines each bit in its two operands, and when two
corresponding bits are both 1, the resulting bit is 1. All other
resulting bits are 0. Here is an example of how this works, using binary
numbers:

<div class="example">

``` example
11001001 & 10011011 = 10001001
```

</div>

Bitwise inclusive disjunction examines each bit in its two operands, and
when two corresponding bits are both 0, the resulting bit is 0. All
other resulting bits are 1.

<div class="example">

``` example
11001001 | 10011011 = 11011011
```

</div>

Bitwise exclusive disjunction examines each bit in its two operands, and
when two corresponding bits are different, the resulting bit is 1. All
other resulting bits are 0.

<div class="example">

``` example
11001001 ^ 10011011 = 01010010
```

</div>

Bitwise negation reverses each bit in its operand:

<div class="example">

``` example
~11001001 = 00110110
```

</div>

In C, you can only use these operators with operands of an integer (or
character) type, and for maximum portability, you should only use the
bitwise negation operator with unsigned integer types. Here are some
examples of using these operators in C code:

<div class="example">

``` example
unsigned int foo = 42;
unsigned int bar = 57;
unsigned int quux;

quux = foo & bar;
quux = foo | bar;
quux = foo ^ bar;
quux = ~foo;
```

</div>

------------------------------------------------------------------------

<span id="Pointer-Operators"></span>

<div class="header">

Next: <a href="#The-sizeof-Operator" accesskey="n" rel="next">The sizeof
Operator</a>, Previous:
<a href="#Bitwise-Logical-Operators" accesskey="p" rel="prev">Bitwise
Logical Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Pointer-Operators-1"></span>

### 3.10 Pointer Operators

<span id="index-pointer-operators"></span>

You can use the address operator `&` to obtain the memory address of an
object.

<div class="example">

``` example
int x = 5;
int *pointer_to_x = &x;
```

</div>

It is not necessary to use this operator to obtain the address of a
function, although you can:

<div class="example">

``` example
extern int foo (void);
int (*fp1) (void) = foo; /* fp1 points to foo */
int (*fp2) (void) = &foo; /* fp2 also points to foo */
```

</div>

Function pointers and data pointers are not compatible, in the sense
that you cannot expect to store the address of a function into a data
pointer, and then copy that into a function pointer and call it
successfully. It might work on some systems, but it’s not a portable
technique.

As a GNU extension to C89, you can also obtain the address of a label
with the label address operator `&&`. The result is a `void*` pointer
which can be used with `goto`. See [The goto
Statement](#The-goto-Statement).

Given a memory address stored in a pointer, you can use the indirection
operator `*` to obtain the value stored at the address. (This is called
*dereferencing* the pointer.)

<div class="example">

``` example
int x = 5;
int y;
int *ptr;

ptr = &x;    /* ptr now holds the address of x. */

y = *ptr;    /* y gets the value stored at the address
                stored in ptr. */
```

</div>

Avoid using dereferencing pointers that have not been initialized to a
known memory location.

------------------------------------------------------------------------

<span id="The-sizeof-Operator"></span>

<div class="header">

Next: <a href="#Type-Casts" accesskey="n" rel="next">Type Casts</a>,
Previous: <a href="#Pointer-Operators" accesskey="p" rel="prev">Pointer
Operators</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-sizeof-Operator-1"></span>

### 3.11 The sizeof Operator

<span id="index-sizeof-operator"></span>

You can use the `sizeof` operator to obtain the size (in bytes) of the
data type of its operand. The operand may be an actual type specifier
(such as `int` or `float`), as well as any valid expression. When the
operand is a type name, it must be enclosed in parentheses. Here are
some examples:

<div class="example">

``` example
size_t a = sizeof(int);
size_t b = sizeof(float);
size_t c = sizeof(5);
size_t d = sizeof(5.143);
size_t e = sizeof a;
```

</div>

The result of the `sizeof` operator is of a type called `size_t`, which
is defined in the header file `<stddef.h>`. `size_t` is an unsigned
integer type, perhaps identical to `unsigned int` or
`unsigned long int`; it varies from system to system.

The `size_t` type is often a convenient type for a loop index, since it
is guaranteed to be able to hold the number of elements in any array;
this is not the case with `int`, for example.

The `sizeof` operator can be used to automatically compute the number of
elements in an array:

<div class="example">

``` example
#include <stddef.h>
#include <stdio.h>

static const int values[] = { 1, 2, 48, 681 };
#define ARRAYSIZE(x) (sizeof x/sizeof x[0])

int main (int argc, char *argv[]) 
{
    size_t i;
    for (i = 0; i < ARRAYSIZE(values); i++) 
    {
        printf("%d\n", values[i]);
    }
    return 0;
}
```

</div>

There are two cases where this technique does not work. The first is
where the array element has zero size (GCC supports zero-sized
structures as a GNU extension). The second is where the array is in fact
a function parameter (see [Function Parameters](#Function-Parameters)).

------------------------------------------------------------------------

<span id="Type-Casts"></span>

<div class="header">

Next: <a href="#Array-Subscripts" accesskey="n" rel="next">Array
Subscripts</a>, Previous:
<a href="#The-sizeof-Operator" accesskey="p" rel="prev">The sizeof
Operator</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Type-Casts-1"></span>

### 3.12 Type Casts

<span id="index-type-casts"></span> <span id="index-casts"></span>

You can use a type cast to explicitly cause an expression to be of a
specified data type. A type cast consists of a type specifier enclosed
in parentheses, followed by an expression. To ensure proper casting, you
should also enclose the expression that follows the type specifier in
parentheses. Here is an example:

<div class="example">

``` example
float x;
int y = 7;
int z = 3;
x = (float) (y / z);
```

</div>

In that example, since `y` and `z` are both integers, integer division
is performed, and even though `x` is a floating-point variable, it
receives the value 2. Explicitly casting the result of the division to
`float` does no good, because the computed value of `y/z` is already 2.

To fix this problem, you need to convert one of the operands to a
floating-point type before the division takes place:

<div class="example">

``` example
float x;
int y = 7;
int z = 3;
x = (y / (float)z);
```

</div>

Here, a floating-point value close to 2.333… is assigned to `x`.

Type casting only works with scalar types (that is, integer,
floating-point or pointer types). Therefore, this is not allowed:

<div class="example">

``` example
struct fooTag { /* members ... */ };
struct fooTag foo;
unsigned char byteArray[8];

foo = (struct fooType) byteArray; /* Fail! */
```

</div>

------------------------------------------------------------------------

<span id="Array-Subscripts"></span>

<div class="header">

Next: <a href="#Function-Calls-as-Expressions" accesskey="n"
rel="next">Function Calls as Expressions</a>, Previous:
<a href="#Type-Casts" accesskey="p" rel="prev">Type Casts</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Array-Subscripts-1"></span>

### 3.13 Array Subscripts

<span id="index-array-subscripts"></span>

You can access array elements by specifying the name of the array, and
the array subscript (or index, or element number) enclosed in brackets.
Here is an example, supposing an integer array called `my_array`:

<div class="example">

``` example
my_array[0] = 5;
```

</div>

The array subscript expression `A[i]` is defined as being identical to
the expression `(*((A)+(i)))`. This means that many uses of an array
name are equivalent to a pointer expression. It also means that you
cannot subscript an array having the `register` storage class.

------------------------------------------------------------------------

<span id="Function-Calls-as-Expressions"></span>

<div class="header">

Next: <a href="#The-Comma-Operator" accesskey="n" rel="next">The Comma
Operator</a>, Previous:
<a href="#Array-Subscripts" accesskey="p" rel="prev">Array
Subscripts</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Function-Calls-as-Expressions-1"></span>

### 3.14 Function Calls as Expressions

<span id="index-function-calls_002c-as-expressions"></span>

A call to any function which returns a value is an expression.

<div class="example">

``` example
int function(void);
…
a = 10 + function();
```

</div>

------------------------------------------------------------------------

<span id="The-Comma-Operator"></span>

<div class="header">

Next:
<a href="#Member-Access-Expressions" accesskey="n" rel="next">Member
Access Expressions</a>, Previous:
<a href="#Function-Calls-as-Expressions" accesskey="p"
rel="prev">Function Calls as Expressions</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-Comma-Operator-1"></span>

### 3.15 The Comma Operator

<span id="index-comma-operator"></span>

You use the comma operator `,` to separate two (ostensibly related)
expressions. For instance, the first expression might produce a value
that is used by the second expression:

<div class="example">

``` example
x++, y = x * x;
```

</div>

More commonly, the comma operator is used in `for` statements, like
this:

<div class="example">

``` example
/* Using the comma operator in a for statement. */

for (x = 1, y = 10;  x <=10 && y >=1;  x++, y--)
  {
    …
  }
```

</div>

This lets you conveniently set, monitor, and modify multiple control
expressions for the `for` statement.

A comma is also used to separate function parameters; however, this is
*not* the comma operator in action. In fact, if the comma operator is
used as we have discussed here in a function call, then the compiler
will interpret that as calling the function with an extra parameter.

If you want to use the comma operator in a function argument, you need
to put parentheses around it. That’s because commas in a function
argument list have a different meaning: they separate arguments. Thus,

<div class="example">

``` example
foo (x,  y=47,  x,  z);
```

</div>

is interpreted as a function call with four arguments, but

<div class="example">

``` example
foo (x,  (y=47,  x),  z);
```

</div>

is a function call with just three arguments. (The second argument is
`(y=47, x)`.)

------------------------------------------------------------------------

<span id="Member-Access-Expressions"></span>

<div class="header">

Next:
<a href="#Conditional-Expressions" accesskey="n" rel="next">Conditional
Expressions</a>, Previous:
<a href="#The-Comma-Operator" accesskey="p" rel="prev">The Comma
Operator</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Member-Access-Expressions-1"></span>

### 3.16 Member Access Expressions

<span id="index-member-access-expressions"></span>

You can use the member access operator `.` to access the members of a
structure or union variable. You put the name of the structure variable
on the left side of the operator, and the name of the member on the
right side.

<div class="example">

``` example
struct point
{
  int x, y;
};

struct point first_point;

first_point.x = 0;
first_point.y = 5;
```

</div>

<span id="index-indirect-member-access-operator"></span>

You can also access the members of a structure or union variable via a
pointer by using the indirect member access operator `->`. `x->y` is
equivalent to `(*x).y`.

<div class="example">

``` example
struct fish
  {
    int length, weight;
  };

struct fish salmon;

struct fish *fish_pointer = &salmon;

fish_pointer->length = 3;
fish_pointer->weight = 9;
```

</div>

See [Pointers](#Pointers).

------------------------------------------------------------------------

<span id="Conditional-Expressions"></span>

<div class="header">

Next:
<a href="#Statements-and-Declarations-in-Expressions" accesskey="n"
rel="next">Statements and Declarations in Expressions</a>, Previous:
<a href="#Member-Access-Expressions" accesskey="p" rel="prev">Member
Access Expressions</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Conditional-Expressions-1"></span>

### 3.17 Conditional Expressions

<span id="index-conditional-expressions"></span>
<span id="index-expressions_002c-conditional"></span>
<span id="index-ternary-operator"></span>

You use the conditional operator to cause the entire conditional
expression to evaluate to either its second or its third operand, based
on the truth value of its first operand. Here’s an example:

<div class="example">

``` example
a ? b : c
```

</div>

If expression `a` is true, then expression `b` is evaluated and the
result is the value of `b`. Otherwise, expression `c` is evaluated and
the result is `c`.

Expressions `b` and `c` must be compatible. That is, they must both be

1.  arithmetic types
2.  compatible `struct` or `union` types
3.  pointers to compatible types (one of which might be the NULL
    pointer)

Alternatively, one operand is a pointer and the other is a `void*`
pointer.

Here is an example

<div class="example">

``` example
a = (x == 5) ? y : z;
```

</div>

Here, if `x` equals 5, then `a` will receive the value of `y`.
Otherwise, `a` will receive the value of `z`. This can be considered a
shorthand method for writing a simple `if`…`else` statement. The
following example will accomplish the same task as the previous one:

<div class="example">

``` example
if (x == 5)
    a = y;
else
    a = z;
```

</div>

If the first operand of the conditional operator is true, then the third
operand is never evaluated. Similarly, if the first operand is false,
then the second operand is never evaluated. The first operand is always
evaluated.

------------------------------------------------------------------------

<span id="Statements-and-Declarations-in-Expressions"></span>

<div class="header">

Next: <a href="#Operator-Precedence" accesskey="n" rel="next">Operator
Precedence</a>, Previous:
<a href="#Conditional-Expressions" accesskey="p" rel="prev">Conditional
Expressions</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Statements-and-Declarations-in-Expressions-1"></span>

### 3.18 Statements and Declarations in Expressions

<span id="index-statements-inside-expressions"></span>
<span id="index-declarations-inside-expressions"></span>
<span id="index-expressions-containing-statements"></span>
<span id="index-macros_002c-statements-in-expressions"></span>

As a GNU C extension, you can build an expression using compound
statement enclosed in parentheses. This allows you to included loops,
switches, and local variables within an expression.

Recall that a compound statement (also known as a block) is a sequence
of statements surrounded by braces. In this construct, parentheses go
around the braces. Here is an example:

<div class="example">

``` example
({ int y = function (); int z;
    if (y > 0) z = y;
   else z = - y;
   z; })
```

</div>

That is a valid (though slightly more complex than necessary) expression
for the absolute value of `function ()`.

The last thing in the compound statement should be an expression
followed by a semicolon; the value of this subexpression serves as the
value of the entire construct. (If you use some other kind of statement
last within the braces, the construct has type `void`, and thus
effectively no value.)

This feature is especially useful in making macro definitions “safe” (so
that they evaluate each operand exactly once). For example, the
“maximum” function is commonly defined as a macro in standard C as
follows:

<div class="example">

``` example
#define max(a,b) ((a) > (b) ? (a) : (b))
```

</div>

<span id="index-side-effects_002c-macro-argument"></span>

But this definition computes either `a` or `b` twice, with bad results
if the operand has side effects. In GNU C, if you know the type of the
operands (here let’s assume `int`), you can define the macro safely as
follows:

<div class="example">

``` example
#define maxint(a,b) \
  ({int _a = (a), _b = (b); _a > _b ? _a : _b; })
```

</div>

If you don’t know the type of the operand, you can still do this, but
you must use `typeof` expressions or type naming.

Embedded statements are not allowed in constant expressions, such as the
value of an enumeration constant, the width of a bit field, or the
initial value of a static variable.

------------------------------------------------------------------------

<span id="Operator-Precedence"></span>

<div class="header">

Next: <a href="#Order-of-Evaluation" accesskey="n" rel="next">Order of
Evaluation</a>, Previous:
<a href="#Statements-and-Declarations-in-Expressions" accesskey="p"
rel="prev">Statements and Declarations in Expressions</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Operator-Precedence-1"></span>

### 3.19 Operator Precedence

<span id="index-operator-precedence"></span>
<span id="index-precedence_002c-operator"></span>

When an expression contains multiple operators, such as `a + b * f()`,
the operators are grouped based on rules of *precedence*. For instance,
the meaning of that expression is to call the function `f` with no
arguments, multiply the result by `b`, then add that result to `a`.
That’s what the C rules of operator precedence determine for this
expression.

The following is a list of types of expressions, presented in order of
highest precedence first. Sometimes two or more operators have equal
precedence; all those operators are applied from left to right unless
stated otherwise.

1.  Function calls, array subscripting, and membership access operator
    expressions.
2.  Unary operators, including logical negation, bitwise complement,
    increment, decrement, unary positive, unary negative, indirection
    operator, address operator, type casting, and `sizeof` expressions.
    When several unary operators are consecutive, the later ones are
    nested within the earlier ones: `!-x` means `!(-x)`.
3.  Multiplication, division, and modular division expressions.
4.  Addition and subtraction expressions.
5.  Bitwise shifting expressions.
6.  Greater-than, less-than, greater-than-or-equal-to, and
    less-than-or-equal-to  
    expressions.
7.  Equal-to and not-equal-to expressions.
8.  Bitwise AND expressions.
9.  Bitwise exclusive OR expressions.
10. Bitwise inclusive OR expressions.
11. Logical AND expressions.
12. Logical OR expressions.
13. Conditional expressions (using `?:`). When used as subexpressions,
    these are evaluated right to left.
14. All assignment expressions, including compound assignment. When
    multiple assignment statements appear as subexpressions in a single
    larger expression, they are evaluated right to left.
15. Comma operator expressions.

The above list is somewhat dry and is apparently straightforward, but it
does hide some pitfalls. Take this example:

<div class="example">

``` example
foo = *p++;
```

</div>

Here `p` is incremented as a side effect of the expression, but `foo`
takes the value of `*(p++)` rather than `(*p)++`, since the unary
operators bind right to left. There are other examples of potential
surprises lurking behind the C precedence table. For this reason if
there is the slightest risk of the reader misunderstanding the meaning
of the program, you should use parentheses to make your meaning clear.

------------------------------------------------------------------------

<span id="Order-of-Evaluation"></span>

<div class="header">

Previous:
<a href="#Operator-Precedence" accesskey="p" rel="prev">Operator
Precedence</a>, Up:
<a href="#Expressions-and-Operators" accesskey="u" rel="up">Expressions
and Operators</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Order-of-Evaluation-1"></span>

### 3.20 Order of Evaluation

In C you cannot assume that multiple subexpressions are evaluated in the
order that seems natural. For instance, consider the expression
`++a * f()`. Does this increment `a` before or after calling the
function `f`? The compiler could do it in either order, so you cannot
make assumptions.

This manual explains the semantics of the C language in the abstract.
However, an actual compiler translates source code into specific actions
in an actual computer, and may re-order operations for the sake of
efficiency. The correspondence between the program you write and the
things the computer actually does are specified in terms of *side
effects* and *sequence points*.

|  |  |  |
|:---|----|:---|
| • <a href="#Side-Effects" accesskey="1">Side Effects</a>: |    |  |
| • <a href="#Sequence-Points" accesskey="2">Sequence Points</a>: |    |  |
| • <a href="#Sequence-Points-Constrain-Expressions" accesskey="3">Sequence
Points Constrain Expressions</a>: |    |  |
| • <a href="#Sequence-Points-and-Signal-Delivery" accesskey="4">Sequence
Points and Signal Delivery</a>: |    |  |

------------------------------------------------------------------------

<span id="Side-Effects"></span>

<div class="header">

Next:
<a href="#Sequence-Points" accesskey="n" rel="next">Sequence Points</a>,
Up: <a href="#Order-of-Evaluation" accesskey="u" rel="up">Order of
Evaluation</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Side-Effects-1"></span>

#### 3.20.1 Side Effects

<span id="index-side-effect"></span>

A *side effect* is one of the following:

1.  accessing a `volatile` object
2.  modifying an object
3.  modifying a file
4.  a call to a function which performs any of the above side effects

These are essentially the externally-visible effects of running a
program. They are called side effects because they are effects of
expression evalation beyond the expression’s actual resulting value.

The compiler is allowed to perform the operations of your program in an
order different to the order implied by the source of your program,
provided that in the end all the necessary side effects actually take
place. The compiler is also allowed to entirely omit some operations;
for example it’s allowed to skip evaluating part of an expression if it
can be certain that the value is not used and evaluating that part of
the expression won’t produce any needed side effects.

------------------------------------------------------------------------

<span id="Sequence-Points"></span>

<div class="header">

Next: <a href="#Sequence-Points-Constrain-Expressions" accesskey="n"
rel="next">Sequence Points Constrain Expressions</a>, Previous:
<a href="#Side-Effects" accesskey="p" rel="prev">Side Effects</a>, Up:
<a href="#Order-of-Evaluation" accesskey="u" rel="up">Order of
Evaluation</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Sequence-Points-1"></span>

#### 3.20.2 Sequence Points

Another requirement on the compiler is that side effects should take
place in the correct order. In order to provide this without
over-constraining the compiler, the C89 and C90 standards specify a list
of sequence points. A *sequence point* is one of the following:

<span id="index-sequence-point"></span>

1.  a call to a function (after argument evaluation is complete)
2.  the end of the left-hand operand of the and operator `&&`
3.  the end of the left-hand operand of the or operator `||`
4.  the end of the left-hand operand of the comma operator `,`
5.  the end of the first operand of the ternary operator `a ? b : c`
6.  the end of a full declarator
    <a href="#FOOT2" id="DOCF2"><sup>2</sup></a>
7.  the end of an initialisation expression
8.  the end of an expression statement (i.e. an expression followed by
    `;`)
9.  the end of the controlling expression of an `if` or `switch`
    statement
10. the end of the controlling expression of a `while` or `do` statement
11. the end of any of the three controlling expressions of a `for`
    statement
12. the end of the expression in a return statement
13. immediately before the return of a library function
14. after the actions associated with an item of formatted I/O (as used
    for example with the `strftime` or the `printf` and `scanf` famlies
    of functions).
15. immediately before and after a call to a comparison function (as
    called for example by `qsort`)

At a sequence point, all the side effects of previous expression
evaluations must be complete, and no side effects of later evaluations
may have taken place.

This may seem a little hard to grasp, but there is another way to
consider this. Imagine you wrote a library (some of whose functions are
external and perhaps others not) and compiled it, allowing someone else
to call one of your functions from their code. The definitions above
ensure that, at the time they call your function, the data they pass in
has values which are consistent with the behaviour specified by the
abstract machine, and any data returned by your function has a state
which is also consistent with the abstract machine. This includes data
accessible via pointers (i.e. not just function parameters and
identifiers with external linkage).

The above is a slight simplification, since compilers exist that perform
whole-program optimisation at link time. Importantly however, although
they might perform optimisations, the visible side effects of the
program must be the same as if they were produced by the abstract
machine.

------------------------------------------------------------------------

<span id="Sequence-Points-Constrain-Expressions"></span>

<div class="header">

Next: <a href="#Sequence-Points-and-Signal-Delivery" accesskey="n"
rel="next">Sequence Points and Signal Delivery</a>, Previous:
<a href="#Sequence-Points" accesskey="p" rel="prev">Sequence Points</a>,
Up: <a href="#Order-of-Evaluation" accesskey="u" rel="up">Order of
Evaluation</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Sequence-Points-Constrain-Expressions-1"></span>

#### 3.20.3 Sequence Points Constrain Expressions

The code fragment

<div class="example">

``` example
i = i + 1;
```

</div>

is quite normal and no doubt occurs in many programs. However, the quite
similar code fragment

<div class="example">

``` example
i = ++i + 1;
```

</div>

is a little harder to understand; what is the final value of `i`? The C
standards (both C89 and C99) both forbid this construct in conforming
programs.

Between two sequence points,

1.  an object may have its stored value modified at most once by the
    evaluation of an expression
2.  the prior value of the object shall be read only to determine the
    value to be stored.

The first of these two conditions forbids expressions like
`foo(x=2, ++x)`. The second condition forbids expressions like
`a[i++] = i`.

`int x=0; foo(++x, ++x)`  
Not allowed in a conforming program; modifies `x` twice before argument
evaluation is complete.

`int x=0; bar((++x,++x))`  
Allowed; the function `bar` takes one argument (the value 2 is passed
here), and there is a sequence point at the comma operator.

`*p++ || *p++`  
Allowed; there is a sequence point at `||`.

`int x = 1, y = x++;`  
Allowed; there is a sequence point after the full declarator of `x`.

`x=2; x++;`  
Allowed; there is a sequence point at the end of the first expression
statement.

`if (x++ > MAX) x = 0;`  
Allowed; there is a sequence point at the end of the controlling
expression of the `if`<a href="#FOOT3" id="DOCF3"><sup>3</sup></a>.

`(x=y) ? ++x : x--;`  
Allowed; there is a sequence point before the `?`, and only one of the
two following expressions is evaluated.

`int *p=malloc(sizeof(*p)), *q=p; *p=foo(); bar((*p)++,(*q)++);`  
Not allowed; the object at `p` is being modified twice before the
evaluation of the arguments to `bar` is complete. The fact that this is
done once via `p` and once via `q` is irrelevant, since they both point
to the same object.

Let’s go back to the example we used to introduce the problem of the
order of evaluation, `++a * f()`. Suppose the code actually looks like
this:

<div class="example">

``` example
static int a = 1;

static int f (void)
{
  a = 100;
  return 3;
}

int foo (void)
{
   return ++a * f();
}
```

</div>

Is this code allowed in a standard-conforming program? Although the
expression in `foo` modifies `a` twice, this is not a problem. Let’s
look at the two possible cases.

The right operand `f()` is evaluated first  
Since `f` returns a value other than void, it must contain a `return`
statement. Therefore, there is a sequence point at the end of the return
expression. That comes between the modification to `a` that `f` makes
and the evaluation of the left operand.

The left operand `++a` is evaluated first  
First, `a` is incremented. Then the arguments to `f` are evaluated
(there are zero of them). Then there is a sequence point before `f` is
actually called.

So, we see that our program is standard-conforming. Notice that the
above argument does not actually depend on the details of the body of
the function `f`. It only depends on the function containing something
ending in a sequence point – in our example this is a return statement,
but an expression statement or a full declarator would do just as well.

<span id="index-unspecified-behaviour"></span>

However, the result of executing this code depends on the order of
evaluation of the operands of `*`. If the left-hand operand is evaluated
first, `foo` returns 6. Otherwise, it returns 303. The C standard does
not specify in which order the operands should be evaluated, and also
does not require an implementation either to document the order or even
to stick to one order. The effect of this code is *unspecified*, meaning
that one of several specific things will happen, but the C standards do
not say which.

------------------------------------------------------------------------

<span id="Sequence-Points-and-Signal-Delivery"></span>

<div class="header">

Previous: <a href="#Sequence-Points-Constrain-Expressions" accesskey="p"
rel="prev">Sequence Points Constrain Expressions</a>, Up:
<a href="#Order-of-Evaluation" accesskey="u" rel="up">Order of
Evaluation</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Sequence-Points-and-Signal-Delivery-1"></span>

#### 3.20.4 Sequence Points and Signal Delivery

Signals are mainly documented in the GNU C Library manual rather than
this document, even though the C standards consider the compiler and the
C library together to be “the implementation”.

When a signal is received, this will happen between sequence points.
Side effects on `volatile` objects prior to the previous sequence point
will have occurred, but other updates may not have occurred yet. This
even applies to straight assignments, such as `x=0;`, because the code
generated for that statement may require more than one instruction,
meaning that it can be interrupted part-way through by the delivery of a
signal.

The C standard is quite restrictive about what data access can occur
within a signal handler. They can of course use `auto` variables, but in
terms of reading or writing other objects, they must be
`volatile sig_atomic_t`. The `volatile` type qualifier ensures that
access to the variable in the other parts of the program doesn’t span
sequence points and the use of the `sig_atomic_t` type ensures that
changes to the variable are atomic with respect to signal delivery.

The POSIX standard also allows a small number of library functions to be
called from a signal handler. These functions are referred to as the set
of *async-signal-safe* functions. If your program is intended to run on
a POSIX system but not on other systems, you can safely call these from
your signal handler too.

------------------------------------------------------------------------

<span id="Statements"></span>

<div class="header">

Next: <a href="#Functions" accesskey="n" rel="next">Functions</a>,
Previous: <a href="#Expressions-and-Operators" accesskey="p"
rel="prev">Expressions and Operators</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Statements-1"></span>

## 4 Statements

<span id="index-statements"></span>

You write statements to cause actions and to control flow within your
programs. You can also write statements that do not do anything at all,
or do things that are uselessly trivial.

|  |  |  |
|:---|----|:---|
| • <a href="#Labels" accesskey="1">Labels</a>: |    |  |
| • <a href="#Expression-Statements" accesskey="2">Expression Statements</a>: |    |  |
| • <a href="#The-if-Statement" accesskey="3">The if Statement</a>: |    |  |
| • <a href="#The-switch-Statement" accesskey="4">The switch Statement</a>: |    |  |
| • <a href="#The-while-Statement" accesskey="5">The while Statement</a>: |    |  |
| • <a href="#The-do-Statement" accesskey="6">The do Statement</a>: |    |  |
| • <a href="#The-for-Statement" accesskey="7">The for Statement</a>: |    |  |
| • <a href="#Blocks" accesskey="8">Blocks</a>: |    |  |
| • <a href="#The-Null-Statement" accesskey="9">The Null Statement</a>: |    |  |
| • [The goto Statement](#The-goto-Statement): |    |  |
| • [The break Statement](#The-break-Statement): |    |  |
| • [The continue Statement](#The-continue-Statement): |    |  |
| • [The return Statement](#The-return-Statement): |    |  |
| • [The typedef Statement](#The-typedef-Statement): |    |  |

------------------------------------------------------------------------

<span id="Labels"></span>

<div class="header">

Next:
<a href="#Expression-Statements" accesskey="n" rel="next">Expression
Statements</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Labels-1"></span>

### 4.1 Labels

<span id="index-labels"></span>
<span id="index-labeled-statements"></span>
<span id="index-statements_002c-labeled"></span>

You can use labels to identify a section of source code for use with a
later `goto` (see [The goto Statement](#The-goto-Statement)). A label
consists of an identifier (such as those used for variable names)
followed by a colon. Here is an example:

<div class="example">

``` example
treet:
```

</div>

You should be aware that label names do not interfere with other
identifier names:

<div class="example">

``` example
int treet = 5;    /* treet the variable. */
treet:            /* treet the label. */
```

</div>

The ISO C standard mandates that a label must be followed by at least
one statement, possibly a null statement (see [The Null
Statement](#The-Null-Statement)). GCC will compile code that does not
meet this requirement, but be aware that if you violate it, your code
may have portability issues.

------------------------------------------------------------------------

<span id="Expression-Statements"></span>

<div class="header">

Next: <a href="#The-if-Statement" accesskey="n" rel="next">The if
Statement</a>, Previous:
<a href="#Labels" accesskey="p" rel="prev">Labels</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Expression-Statements-1"></span>

### 4.2 Expression Statements

<span id="index-expression-statements"></span>
<span id="index-statements_002c-expression"></span>

You can turn any expression into a statement by adding a semicolon to
the end of the expression. Here are some examples:

<div class="example">

``` example
5;
2 + 2;
10 >= 9;
```

</div>

In each of those, all that happens is that each expression is evaluated.
However, they are useless because they do not store a value anywhere,
nor do they actually do anything, other than the evaluation itself. The
compiler is free to ignore such statements.

Expression statements are only useful when they have some kind of side
effect, such as storing a value, calling a function, or (this is
esoteric) causing a fault in the program. Here are some more useful
examples:

<div class="example">

``` example
x++;
y = x + 25;
puts ("Hello, user!");
*cucumber;
```

</div>

The last of those statements, `*cucumber;`, could potentially cause a
fault in the program if the value of `cucumber` is both not a valid
pointer and has been declared as `volatile`.

------------------------------------------------------------------------

<span id="The-if-Statement"></span>

<div class="header">

Next:
<a href="#The-switch-Statement" accesskey="n" rel="next">The switch
Statement</a>, Previous:
<a href="#Expression-Statements" accesskey="p" rel="prev">Expression
Statements</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-if-Statement-1"></span>

### 4.3 The `if` Statement

<span id="index-if-statements"></span>
<span id="index-else-statements"></span>

You can use the `if` statement to conditionally execute part of your
program, based on the truth value of a given expression. Here is the
general form of an `if` statement:

<div class="example">

``` example
if (test)
  then-statement
else
  else-statement
```

</div>

If `test` evaluates to true, then `then-statement` is executed and
`else-statement` is not. If `test` evaluates to false, then
`else-statement` is executed and `then-statement` is not. The `else`
clause is optional.

Here is an actual example:

<div class="example">

``` example
if (x == 10)
  puts ("x is 10");
```

</div>

If `x == 10` evaluates to true, then the statement `puts ("x is 10");`
is executed. If `x == 10` evaluates to false, then the statement
`puts ("x is 10");` is not executed.

Here is an example using `else`:

<div class="example">

``` example
if (x == 10)
  puts ("x is 10");
else
  puts ("x is not 10");
```

</div>

You can use a series of `if` statements to test for multiple conditions:

<div class="example">

``` example
if (x == 1)
  puts ("x is 1");
else if (x == 2)
  puts ("x is 2");
else if (x == 3)
  puts ("x is 3");
else
  puts ("x is something else");
```

</div>

This function calculates and displays the date of Easter for the given
year `y`:

<div class="example">

``` example
void
easterDate (int y)
{
  int n = 0;
  int g = (y % 19) + 1;
  int c = (y / 100) + 1;
  int x = ((3 * c) / 4) - 12;
  int z = (((8 * c) + 5) / 25) - 5;
  int d = ((5 * y) / 4) - x - 10;
  int e = ((11 * g) + 20 + z - x) % 30;

  if (((e == 25) && (g > 11)) || (e == 24))
    e++;

  n = 44 - e;

  if (n < 21)
    n += 30;

  n = n + 7 - ((d + n) % 7);

  if (n > 31)
    printf ("Easter: %d April %d", n - 31, y);
  else
    printf ("Easter: %d March %d", n, y);
}
```

</div>

------------------------------------------------------------------------

<span id="The-switch-Statement"></span>

<div class="header">

Next: <a href="#The-while-Statement" accesskey="n" rel="next">The while
Statement</a>, Previous:
<a href="#The-if-Statement" accesskey="p" rel="prev">The if
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-switch-Statement-1"></span>

### 4.4 The `switch` Statement

<span id="index-switch-statement"></span>

You can use the `switch` statement to compare one expression with
others, and then execute a series of sub-statements based on the result
of the comparisons. Here is the general form of a `switch` statement:

<div class="example">

``` example
switch (test)
  {
    case compare-1:
      if-equal-statement-1
    case compare-2:
      if-equal-statement-2
    …
    default:
      default-statement
  }
```

</div>

The `switch` statement compares `test` to each of the `compare`
expressions, until it finds one that is equal to `test`. Then, the
statements following the successful case are executed. All of the
expressions compared must be of an integer type, and the `compare-N`
expressions must be of a constant integer type (e.g., a literal integer
or an expression built of literal integers).

Optionally, you can specify a default case. If `test` doesn’t match any
of the specific cases listed prior to the default case, then the
statements for the default case are executed. Traditionally, the default
case is put after the specific cases, but that isn’t required.

<div class="example">

``` example
switch (x)
  {
    case 0:
      puts ("x is 0");
      break;
    case 1:
      puts ("x is 1");
      break;
    default:
      puts ("x is something else");
      break;
  }
```

</div>

Notice the usage of the `break` statement in each of the cases. This is
because, once a matching case is found, not only are its statements
executed, but so are the statements for all following cases:

<div class="example">

``` example
int x = 0;
switch (x)
  {
    case 0:
      puts ("x is 0");
    case 1:
      puts ("x is 1");
    default:
      puts ("x is something else");
  }
```

</div>

The output of that example is:

<div class="example">

``` example
x is 0
x is 1
x is something else
```

</div>

This is often not desired. Including a `break` statement at the end of
each case redirects program flow to after the `switch` statement.

As a GNU C extension, you can also specify a range of consecutive
integer values in a single `case` label, like this:

<div class="example">

``` example
case low ... high:
```

</div>

This has the same effect as the corresponding number of individual
`case` labels, one for each integer value from `low` to `high`,
inclusive.

This feature is especially useful for ranges of ASCII character codes:

<div class="example">

``` example
case 'A' ... 'Z':
```

</div>

Be careful to include spaces around the `...`; otherwise it may be
parsed incorrectly when you use it with integer values. For example,
write this:

<div class="example">

``` example
case 1 ... 5:
```

</div>

instead of this:

<div class="example">

``` example
case 1...5:
```

</div>

It is common to use a `switch` statement to handle various possible
values of `errno`. In this case a portable program should watch out for
the possibility that two macros for `errno` values in fact have the same
value, for example `EWOULDBLOCK` and `EAGAIN`.

------------------------------------------------------------------------

<span id="The-while-Statement"></span>

<div class="header">

Next: <a href="#The-do-Statement" accesskey="n" rel="next">The do
Statement</a>, Previous:
<a href="#The-switch-Statement" accesskey="p" rel="prev">The switch
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-while-Statement-1"></span>

### 4.5 The `while` Statement

<span id="index-while-statement"></span>

The `while` statement is a loop statement with an exit test at the
beginning of the loop. Here is the general form of the `while`
statement:

<div class="example">

``` example
while (test)
  statement
```

</div>

The `while` statement first evaluates `test`. If `test` evaluates to
true, `statement` is executed, and then `test` is evaluated again.
`statement` continues to execute repeatedly as long as `test` is true
after each execution of `statement`.

This example prints the integers from zero through nine:

<div class="example">

``` example
int counter = 0;
while (counter < 10)
  printf ("%d ", counter++);
```

</div>

A `break` statement can also cause a `while` loop to exit.

------------------------------------------------------------------------

<span id="The-do-Statement"></span>

<div class="header">

Next: <a href="#The-for-Statement" accesskey="n" rel="next">The for
Statement</a>, Previous:
<a href="#The-while-Statement" accesskey="p" rel="prev">The while
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-do-Statement-1"></span>

### 4.6 The `do` Statement

<span id="index-do-statement"></span>

The `do` statement is a loop statement with an exit test at the end of
the loop. Here is the general form of the `do` statement:

<div class="example">

``` example
do
  statement
while (test);
```

</div>

The `do` statement first executes `statement`. After that, it evaluates
`test`. If `test` is true, then `statement` is executed again.
`statement` continues to execute repeatedly as long as `test` is true
after each execution of `statement`.

This example also prints the integers from zero through nine:

<div class="example">

``` example
int x = 0;
do
  printf ("%d ", x++);
while (x < 10);
```

</div>

A `break` statement can also cause a `do` loop to exit.

------------------------------------------------------------------------

<span id="The-for-Statement"></span>

<div class="header">

Next: <a href="#Blocks" accesskey="n" rel="next">Blocks</a>, Previous:
<a href="#The-do-Statement" accesskey="p" rel="prev">The do
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-for-Statement-1"></span>

### 4.7 The `for` Statement

<span id="index-for-statement"></span>

The `for` statement is a loop statement whose structure allows easy
variable initialization, expression testing, and variable modification.
It is very convenient for making counter-controlled loops. Here is the
general form of the `for` statement:

<div class="example">

``` example
for (initialize; test; step)
  statement
```

</div>

The `for` statement first evaluates the expression `initialize`. Then it
evaluates the expression `test`. If `test` is false, then the loop ends
and program control resumes after `statement`. Otherwise, if `test` is
true, then `statement` is executed. Finally, `step` is evaluated, and
the next iteration of the loop begins with evaluating `test` again.

Most often, `initialize` assigns values to one or more variables, which
are generally used as counters, `test` compares those variables to a
predefined expression, and `step` modifies those variables’ values. Here
is another example that prints the integers from zero through nine:

<div class="example">

``` example
int x;
for (x = 0; x < 10; x++)
  printf ("%d ", x);
```

</div>

First, it evaluates `initialize`, which assigns `x` the value 0. Then,
as long as `x` is less than 10, the value of `x` is printed (in the body
of the loop). Then `x` is incremented in the `step` clause and the test
re-evaluated.

All three of the expressions in a `for` statement are optional, and any
combination of the three is valid. Since the first expression is
evaluated only once, it is perhaps the most commonly omitted expression.
You could also write the above example as:

<div class="example">

``` example
int x = 1;
for (; x <= 10; x++)
  printf ("%d ", x);
```

</div>

In this example, `x` receives its value prior to the beginning of the
`for` statement.

If you leave out the `test` expression, then the `for` statement is an
infinite loop (unless you put a `break` or `goto` statement somewhere in
`statement`). This is like using `1` as `test`; it is never false.

This `for` statement starts printing numbers at 1 and then continues
indefinitely, always printing `x` incremented by 1:

<div class="example">

``` example
for (x = 1; ; x++)
  printf ("%d ", x);
```

</div>

If you leave out the `step` expression, then no progress is made toward
completing the loop—at least not as is normally expected with a `for`
statement.

This example prints the number 1 over and over, indefinitely:

<div class="example">

``` example
for (x = 1; x <= 10;)
  printf ("%d ", x);
```

</div>

Perhaps confusingly, you cannot use the comma operator (see [The Comma
Operator](#The-Comma-Operator)) for monitoring multiple variables in a
`for` statement, because as usual the comma operator discards the result
of its left operand. This loop:

<div class="example">

``` example
int x, y;
for (x = 1, y = 10; x <= 10, y >= 1; x+=2, y--)
  printf ("%d %d\n", x, y);
```

</div>

Outputs:

<div class="example">

``` example
1 10
3 9
5 8
7 7
9 6
11 5
13 4
15 3
17 2
19 1
```

</div>

If you need to test two conditions, you will need to use the `&&`
operator:

<div class="example">

``` example
int x, y;
for (x = 1, y = 10; x <= 10 && y >= 1; x+=2, y--)
  printf ("%d %d\n", x, y);
```

</div>

A `break` statement can also cause a `for` loop to exit.

Here is an example of a function that computes the summation of squares,
given a starting integer to square and an ending integer to square:

<div class="example">

``` example
int
sum_of_squares (int start, int end)
{
  int i, sum = 0;
  for (i = start; i <= end; i++)
    sum += i * i;
  return sum;
}
```

</div>

------------------------------------------------------------------------

<span id="Blocks"></span>

<div class="header">

Next: <a href="#The-Null-Statement" accesskey="n" rel="next">The Null
Statement</a>, Previous:
<a href="#The-for-Statement" accesskey="p" rel="prev">The for
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Blocks-1"></span>

### 4.8 Blocks

<span id="index-blocks"></span>
<span id="index-compound-statements"></span>

A *block* is a set of zero or more statements enclosed in braces. Blocks
are also known as *compound statements*. Often, a block is used as the
body of an `if` statement or a loop statement, to group statements
together.

<div class="example">

``` example
for (x = 1; x <= 10; x++)
  {
    printf ("x is %d\n", x);
    
    if ((x % 2) == 0)
      printf ("%d is even\n", x);
    else
      printf ("%d is odd\n", x);
  }
```

</div>

You can also put blocks inside other blocks:

<div class="example">

``` example
for (x = 1; x <= 10; x++)
  {
    if ((x % 2) == 0)
      {
        printf ("x is %d\n", x);
        printf ("%d is even\n", x);
      }
    else
      {
        printf ("x is %d\n", x);
        printf ("%d is odd\n", x);
      }
  }
```

</div>

You can declare variables inside a block; such variables are local to
that block. In C89, declarations must occur before other statements, and
so sometimes it is useful to introduce a block simply for this purpose:

<div class="example">

``` example
{
  int x = 5;
  printf ("%d\n", x);
}
printf ("%d\n", x);   /* Compilation error! x exists only
                       in the preceding block. */
```

</div>

------------------------------------------------------------------------

<span id="The-Null-Statement"></span>

<div class="header">

Next: <a href="#The-goto-Statement" accesskey="n" rel="next">The goto
Statement</a>, Previous:
<a href="#Blocks" accesskey="p" rel="prev">Blocks</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-Null-Statement-1"></span>

### 4.9 The Null Statement

<span id="index-null-statement"></span>
<span id="index-statement_002c-null"></span>

The *null statement* is merely a semicolon alone.

<div class="example">

``` example
;
```

</div>

A null statement does not do anything. It does not store a value
anywhere. It does not cause time to pass during the execution of your
program.

Most often, a null statement is used as the body of a loop statement, or
as one or more of the expressions in a `for` statement. Here is an
example of a `for` statement that uses the null statement as the body of
the loop (and also calculates the integer square root of `n`, just for
fun):

<div class="example">

``` example
for (i = 1; i*i < n; i++)
  ;
```

</div>

Here is another example that uses the null statement as the body of a
`for` loop and also produces output:

<div class="example">

``` example
for (x = 1; x <= 5; printf ("x is now %d\n", x), x++)
  ;
```

</div>

A null statement is also sometimes used to follow a label that would
otherwise be the last thing in a block.

------------------------------------------------------------------------

<span id="The-goto-Statement"></span>

<div class="header">

Next: <a href="#The-break-Statement" accesskey="n" rel="next">The break
Statement</a>, Previous:
<a href="#The-Null-Statement" accesskey="p" rel="prev">The Null
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-goto-Statement-1"></span>

### 4.10 The `goto` Statement

<span id="index-goto-statement"></span>

You can use the `goto` statement to unconditionally jump to a different
place in the program. Here is the general form of a `goto` statement:

<div class="example">

``` example
goto label;
```

</div>

You have to specify a label to jump to; when the `goto` statement is
executed, program control jumps to that label. See [Labels](#Labels).
Here is an example:

<div class="example">

``` example
goto end_of_program;
…
end_of_program:
```

</div>

The label can be anywhere in the same function as the `goto` statement
that jumps to it, but a `goto` statement cannot jump to a label in a
different function.

You *can* use `goto` statements to simulate loop statements, but we do
not recommend it—it makes the program harder to read, and GCC cannot
optimize it as well. You should use `for`, `while`, and `do` statements
instead of `goto` statements, when possible.

As an extension, GCC allows a goto statement to jump to an address
specified by a `void*` variable. To make this work, you also need to
take the address of a label by using the unary operator `&&` (not `&`).
Here is a contrived example:

<div class="example">

``` example
enum Play { ROCK=0, PAPER=1, SCISSORS=2 };
enum Result { WIN, LOSE, DRAW };

static enum Result turn (void) 
{
  const void * const jumptable[] = {&&rock, &&paper, &&scissors};
  enum Play opp;                /* opponent’s play */
  goto *jumptable[select_option (&opp)];
 rock:
  return opp == ROCK ? DRAW : (opp == PAPER ? LOSE : WIN);
 paper:
  return opp == ROCK ? WIN  : (opp == PAPER ? DRAW : LOSE);
 scissors:
  return opp == ROCK ? LOSE : (opp == PAPER ? WIN  : DRAW);
}
```

</div>

------------------------------------------------------------------------

<span id="The-break-Statement"></span>

<div class="header">

Next:
<a href="#The-continue-Statement" accesskey="n" rel="next">The continue
Statement</a>, Previous:
<a href="#The-goto-Statement" accesskey="p" rel="prev">The goto
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-break-Statement-1"></span>

### 4.11 The `break` Statement

<span id="index-break-statement"></span>

You can use the `break` statement to terminate a `while`, `do`, `for`,
or `switch` statement. Here is an example:

<div class="example">

``` example
int x;
for (x = 1; x <= 10; x++)
  {
    if (x == 8)
      break;
    else
      printf ("%d ", x);
  }
```

</div>

That example prints numbers from 1 to 7. When `x` is incremented to 8,
`x == 8` is true, so the `break` statement is executed, terminating the
`for` loop prematurely.

If you put a `break` statement inside of a loop or `switch` statement
which itself is inside of a loop or `switch` statement, the `break` only
terminates the innermost loop or `switch` statement.

------------------------------------------------------------------------

<span id="The-continue-Statement"></span>

<div class="header">

Next:
<a href="#The-return-Statement" accesskey="n" rel="next">The return
Statement</a>, Previous:
<a href="#The-break-Statement" accesskey="p" rel="prev">The break
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-continue-Statement-1"></span>

### 4.12 The `continue` Statement

<span id="index-continue-statement"></span>

You can use the `continue` statement in loops to terminate an iteration
of the loop and begin the next iteration. Here is an example:

<div class="example">

``` example
for (x = 0; x < 100; x++)
  {
    if (x % 2 == 0)
      continue;
    else
      sum_of_odd_numbers + = x;
  }
```

</div>

If you put a `continue` statement inside a loop which itself is inside a
loop, then it affects only the innermost loop.

------------------------------------------------------------------------

<span id="The-return-Statement"></span>

<div class="header">

Next:
<a href="#The-typedef-Statement" accesskey="n" rel="next">The typedef
Statement</a>, Previous:
<a href="#The-continue-Statement" accesskey="p" rel="prev">The continue
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-return-Statement-1"></span>

### 4.13 The `return` Statement

<span id="index-return-statement"></span>

You can use the `return` statement to end the execution of a function
and return program control to the function that called it. Here is the
general form of the `return` statement:

<div class="example">

``` example
return return-value;
```

</div>

`return-value` is an optional expression to return. If the function’s
return type is `void`, then it is invalid to return an expression. You
can, however, use the `return` statement without a return value.

If the function’s return type is not the same as the type of
`return-value`, and automatic type conversion cannot be performed, then
returning `return-value` is invalid.

If the function’s return type is not `void` and no return value is
specified, then the `return` statement is valid unless the function is
called in a context that requires a return value. For example:

<div class="example">

``` example
x = cosine (y);
```

</div>

In that case, the function `cosine` was called in a context that
required a return value, so the value could be assigned to `x`.

Even in contexts where a return value is not required, it is a bad idea
for a non-`void` function to omit the return value. With GCC, you can
use the command line option
<span class="nolinebreak">`-Wreturn`</span>`-type` to issue a warning if
you omit the return value in such functions.

Here are some examples of using the `return` statement, in both a `void`
and non-`void` function:

<div class="example">

``` example
void
print_plus_five (int x)
{
  printf ("%d ", x + 5);
  return;
}
```

</div>

<div class="example">

``` example
int
square_value (int x)
{
  return x * x;
}
```

</div>

------------------------------------------------------------------------

<span id="The-typedef-Statement"></span>

<div class="header">

Previous:
<a href="#The-return-Statement" accesskey="p" rel="prev">The return
Statement</a>, Up:
<a href="#Statements" accesskey="u" rel="up">Statements</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-typedef-Statement-1"></span>

### 4.14 The `typedef` Statement

<span id="index-typedef-statement"></span>

You can use the `typedef` statement to create new names for data types.
Here is the general form of the `typedef` statement:

<div class="example">

``` example
typedef old-type-name new-type-name
```

</div>

`old-type-name` is the existing name for the type, and may consist of
more than one token (e.g., `unsigned long int`). `new-type-name` is the
resulting new name for the type, and must be a single identifier.
Creating this new name for the type does not cause the old name to cease
to exist. Here are some examples:

<div class="example">

``` example
typedef unsigned char byte_type;
typedef double real_number_type;
```

</div>

In the case of custom data types, you can use `typedef` to make a new
name for the type while defining the type:

<div class="example">

``` example
typedef struct fish
{
  float weight;
  float length;
  float probability_of_being_caught;
} fish_type;
```

</div>

To make a type definition of an array, you first provide the type of the
element, and then establish the number of elements at the end of the
type definition:

<div class="example">

``` example
typedef char array_of_bytes [5];
array_of_bytes five_bytes = {0, 1, 2, 3, 4};
```

</div>

When selecting names for types, you should avoid ending your type names
with a `_t` suffix. The compiler will allow you to do this, but the
POSIX standard reserves use of the `_t` suffix for standard library type
names.

------------------------------------------------------------------------

<span id="Functions"></span>

<div class="header">

Next:
<a href="#Program-Structure-and-Scope" accesskey="n" rel="next">Program
Structure and Scope</a>, Previous:
<a href="#Statements" accesskey="p" rel="prev">Statements</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Functions-1"></span>

## 5 Functions

<span id="index-functions"></span>

You can write functions to separate parts of your program into distinct
subprocedures. To write a function, you must at least create a function
definition. It is a good idea also to have an explicit function
declaration; you don’t have to, but if you leave it out, then the
default implicit declaration might not match the function itself, and
you will get some compile-time warnings.

Every program requires at least one function, called `main`. That is
where the program’s execution begins.

|  |  |  |
|:---|----|:---|
| • <a href="#Function-Declarations" accesskey="1">Function Declarations</a>: |    |  |
| • <a href="#Function-Definitions" accesskey="2">Function Definitions</a>: |    |  |
| • <a href="#Calling-Functions" accesskey="3">Calling Functions</a>: |    |  |
| • <a href="#Function-Parameters" accesskey="4">Function Parameters</a>: |    |  |
| • <a href="#Variable-Length-Parameter-Lists" accesskey="5">Variable Length
Parameter Lists</a>: |    |  |
| • <a href="#Calling-Functions-Through-Function-Pointers"
accesskey="6">Calling Functions Through Function Pointers</a>: |    |  |
| • <a href="#The-main-Function" accesskey="7">The main Function</a>: |    |  |
| • <a href="#Recursive-Functions" accesskey="8">Recursive Functions</a>: |    |  |
| • <a href="#Static-Functions" accesskey="9">Static Functions</a>: |    |  |
| • [Nested Functions](#Nested-Functions): |    |  |

------------------------------------------------------------------------

<span id="Function-Declarations"></span>

<div class="header">

Next: <a href="#Function-Definitions" accesskey="n" rel="next">Function
Definitions</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Function-Declarations-1"></span>

### 5.1 Function Declarations

<span id="index-function-declarations"></span>
<span id="index-declarations_002c-function"></span>

You write a function declaration to specify the name of a function, a
list of parameters, and the function’s return type. A function
declaration ends with a semicolon. Here is the general form:

<div class="example">

``` example
return-type function-name (parameter-list);
```

</div>

`return-type` indicates the data type of the value returned by the
function. You can declare a function that doesn’t return anything by
using the return type `void`.

`function-name` can be any valid identifier (see
[Identifiers](#Identifiers)).

`parameter-list` consists of zero or more parameters, separated by
commas. A typical parameter consists of a data type and an optional name
for the parameter. You can also declare a function that has a variable
number of parameters (see [Variable Length Parameter
Lists](#Variable-Length-Parameter-Lists)), or no parameters using
`void`. Leaving out `parameter-list` entirely also indicates no
parameters, but it is better to specify it explicitly with `void`.

Here is an example of a function declaration with two parameters:

<div class="example">

``` example
int foo (int, double);
```

</div>

If you include a name for a parameter, the name immediately follows the
data type, like this:

<div class="example">

``` example
int foo (int x, double y);
```

</div>

The parameter names can be any identifier (see
[Identifiers](#Identifiers)), and if you have more than one parameter,
you can’t use the same name more than once within a single declaration.
The parameter names in the declaration need not match the names in the
definition.

You should write the function declaration above the first use of the
function. You can put it in a header file and use the `#include`
directive to include that function declaration in any source code files
that use the function.

------------------------------------------------------------------------

<span id="Function-Definitions"></span>

<div class="header">

Next: <a href="#Calling-Functions" accesskey="n" rel="next">Calling
Functions</a>, Previous:
<a href="#Function-Declarations" accesskey="p" rel="prev">Function
Declarations</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Function-Definitions-1"></span>

### 5.2 Function Definitions

<span id="index-function-definitions"></span>
<span id="index-definitions_002c-function"></span>

You write a function definition to specify what a function actually
does. A function definition consists of information regarding the
function’s name, return type, and types and names of parameters, along
with the body of the function. The function body is a series of
statements enclosed in braces; in fact it is simply a block (see
[Blocks](#Blocks)).

Here is the general form of a function definition:

<div class="example">

``` example
return-type
function-name (parameter-list)
{
  function-body
}
```

</div>

`return-type` and `function-name` are the same as what you use in the
function declaration (see [Function
Declarations](#Function-Declarations)).

`parameter-list` is the same as the parameter list used in the function
declaration (see [Function Declarations](#Function-Declarations)),
except you *must* include names for the parameters in a function
definition.

Here is an simple example of a function definition—it takes two integers
as its parameters and returns the sum of them as its return value:

<div class="example">

``` example
int
add_values (int x, int y)
{
  return x + y;
}
```

</div>

For compatibility with the original design of C, you can also specify
the type of the function parameters *after* the closing parenthesis of
the parameter list, like this:

<div class="example">

``` example
int
add_values (x, y)
    int x, int y;
{
  return x + y;
}
```

</div>

However, we strongly discourage this style of coding; it can cause
subtle problems with type casting, among other problems.

------------------------------------------------------------------------

<span id="Calling-Functions"></span>

<div class="header">

Next: <a href="#Function-Parameters" accesskey="n" rel="next">Function
Parameters</a>, Previous:
<a href="#Function-Definitions" accesskey="p" rel="prev">Function
Definitions</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Calling-Functions-1"></span>

### 5.3 Calling Functions

<span id="index-calling-functions"></span>
<span id="index-functions_002c-calling"></span>

You can call a function by using its name and supplying any needed
parameters. Here is the general form of a function call:

<div class="example">

``` example
function-name (parameters)
```

</div>

A function call can make up an entire statement, or it can be used as a
subexpression. Here is an example of a standalone function call:

<div class="example">

``` example
foo (5);
```

</div>

In that example, the function ‘`foo`’ is called with the parameter `5`.

Here is an example of a function call used as a subexpression:

<div class="example">

``` example
a = square (5);
```

</div>

Supposing that the function ‘`square`’ squares its parameter, the above
example assigns the value 25 to `a`.

If a parameter takes more than one argument, you separate parameters
with commas:

<div class="example">

``` example
a = quux (5, 10);
```

</div>

------------------------------------------------------------------------

<span id="Function-Parameters"></span>

<div class="header">

Next: <a href="#Variable-Length-Parameter-Lists" accesskey="n"
rel="next">Variable Length Parameter Lists</a>, Previous:
<a href="#Calling-Functions" accesskey="p" rel="prev">Calling
Functions</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Function-Parameters-1"></span>

### 5.4 Function Parameters

<span id="index-function-parameters"></span>
<span id="index-parameters_002c-function"></span>

Function parameters can be any expression—a literal value, a value
stored in variable, an address in memory, or a more complex expression
built by combining these.

Within the function body, the parameter is a local copy of the value
passed into the function; you cannot change the value passed in by
changing the local copy.

<div class="example">

``` example
int x = 23;
foo (x);
…
/* Definition for function foo. */
int foo (int a)
{
  a = 2 * a;
  return a;
}
```

</div>

In that example, even though the parameter `a` is modified in the
function ‘`foo`’, the variable `x` that is passed to the function does
not change. If you wish to use the function to change the original value
of `x`, then you would have to incorporate the function call into an
assignment statement:

<div class="example">

``` example
x = foo (x);
```

</div>

If the value that you pass to a function is a memory address (that is, a
pointer), then you can access (and change) the data stored at the memory
address. This achieves an effect similar to pass-by-reference in other
languages, but is not the same: the memory address is simply a value,
just like any other value, and cannot itself be changed. The difference
between passing a pointer and passing an integer lies in what you can do
using the value within the function.

Here is an example of calling a function with a pointer parameter:

<div class="example">

``` example
void
foo (int *x)
{
  *x = *x + 42;
}
…
int a = 15;
foo (&a);
```

</div>

The formal parameter for the function is of type pointer-to-`int`, and
we call the function by passing it the address of a variable of type
`int`. By dereferencing the pointer within the function body, we can
both see and change the value stored in the address. The above changes
the value of `a` to ‘`57`’.

Even if you don’t want to change the value stored in the address,
passing the address of a variable rather than the variable itself can be
useful if the variable type is large and you need to conserve memory
space or limit the performance impact of parameter copying. For example:

<div class="example">

``` example
struct foo
{
  int x;
  float y;
  double z;
};

void bar (const struct foo *a);
```

</div>

In this case, unless you are working on a computer with very large
memory addresses, it will take less memory to pass a pointer to the
structure than to pass an instance of the structure.

One type of parameter that is always passed as a pointer is any sort of
array:

<div class="example">

``` example
void foo (int a[]);
…
int x[100];
foo (x);
```

</div>

In this example, calling the function `foo` with the parameter `a` does
not copy the entire array into a new local parameter within `foo`;
rather, it passes `x` as a pointer to the first element in `x`. Be
careful, though: within the function, you cannot use `sizeof` to
determine the size of the array `x`—`sizeof` instead tells you the size
of the pointer `x`. Indeed, the above code is equivalent to:

<div class="example">

``` example
void foo (int *a);
…
int x[100];
foo (x);
```

</div>

Explicitly specifying the length of the array in the parameter
declaration will not help. If you really need to pass an array by value,
you can wrap it in a `struct`, though doing this will rarely be useful
(passing a `const`-qualified pointer is normally sufficient to indicate
that the caller should not modify the array).

------------------------------------------------------------------------

<span id="Variable-Length-Parameter-Lists"></span>

<div class="header">

Next:
<a href="#Calling-Functions-Through-Function-Pointers" accesskey="n"
rel="next">Calling Functions Through Function Pointers</a>, Previous:
<a href="#Function-Parameters" accesskey="p" rel="prev">Function
Parameters</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Variable-Length-Parameter-Lists-1"></span>

### 5.5 Variable Length Parameter Lists

<span id="index-variable-length-parameter-lists"></span>
<span id="index-parameters-lists_002c-variable-length"></span>
<span id="index-function-parameter-lists_002c-variable-length"></span>

You can write a function that takes a variable number of arguments;
these are called *variadic functions*. To do this, the function needs to
have at least one parameter of a known data type, but the remaining
parameters are optional, and can vary in both quantity and data type.

You list the initial parameters as normal, but then after that, use an
ellipsis: ‘`...`’. Here is an example function prototype:

<div class="example">

``` example
int add_multiple_values (int number, ...);
```

</div>

To work with the optional parameters in the function definition, you
need to use macros that are defined in the library header file
‘`<stdarg.h>`’, so you must `#include` that file. For a detailed
description of these macros, see The GNU C Library manual’s section on
variadic functions.

Here is an example:

<div class="example">

``` example
int
add_multiple_values (int number, ...)
{
  int counter, total = 0;
  
  /* Declare a variable of type ‘va_list’. */
  va_list parameters;

  /* Call the ‘va_start’ function. */
  va_start (parameters, number);

  for (counter = 0; counter < number; counter++)
    {
      /* Get the values of the optional parameters. */
      total += va_arg (parameters, int);
    }

  /* End use of the ‘parameters’ variable. */
  va_end (parameters);

  return total;
}
```

</div>

To use optional parameters, you need to have a way to know how many
there are. This can vary, so it can’t be hard-coded, but if you don’t
know how many optional parameters you have, then you could have
difficulty knowing when to stop using the ‘`va_arg`’ function. In the
above example, the first parameter to the ‘`add_multiple_values`’
function, ‘`number`’, is the number of optional parameters actually
passed. So, we might call the function like this:

<div class="example">

``` example
sum = add_multiple_values (3, 12, 34, 190);
```

</div>

The first parameter indicates how many optional parameters follow it.

Also, note that you don’t actually need to use ‘`va_end`’ function. In
fact, with GCC it doesn’t do anything at all. However, you might want to
include it to maximize compatibility with other compilers.

See [Variadic
Functions](http://www.gnu.org/software/libc/manual/html_mono/libc.html#Variadic-Functions)
in The GNU C Library Reference Manual.

------------------------------------------------------------------------

<span id="Calling-Functions-Through-Function-Pointers"></span>

<div class="header">

Next: <a href="#The-main-Function" accesskey="n" rel="next">The main
Function</a>, Previous:
<a href="#Variable-Length-Parameter-Lists" accesskey="p"
rel="prev">Variable Length Parameter Lists</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Calling-Functions-Through-Function-Pointers-1"></span>

### 5.6 Calling Functions Through Function Pointers

<span id="index-function-pointers_002c-calling-through"></span>

You can also call a function identified by a pointer. The indirection
operator `*` is optional when doing this.

<div class="example">

``` example
#include <stdio.h>

void foo (int i)
{
  printf ("foo %d!\n", i);
}
```

``` example
```

``` example
void bar (int i)
{
  printf ("%d bar!\n", i);
}
```

``` example
```

``` example
void message (void (*func)(int), int times)
{
  int j;
  for (j=0; j<times; ++j)
    func (j);  /* (*func) (j); would be equivalent. */
}

void example (int want_foo) 
{
  void (*pf)(int) = &bar; /* The & is optional. */
  if (want_foo)
    pf = foo;
  message (pf, 5);
}
```

</div>

------------------------------------------------------------------------

<span id="The-main-Function"></span>

<div class="header">

Next: <a href="#Recursive-Functions" accesskey="n" rel="next">Recursive
Functions</a>, Previous:
<a href="#Calling-Functions-Through-Function-Pointers" accesskey="p"
rel="prev">Calling Functions Through Function Pointers</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="The-main-Function-1"></span>

### 5.7 The `main` Function

<span id="index-main-function"></span>
<span id="index-function_002c-main"></span>

Every program requires at least one function, called ‘`main`’. This is
where the program begins executing. You do not need to write a
declaration or prototype for `main`, but you do need to define it.

The return type for `main` is always `int`. You do not have to specify
the return type for `main`, but you can. However, you *cannot* specify
that it has a return type other than `int`.

<span id="index-exit-status"></span>
<span id="index-EXIT_005fFAILURE"></span>
<span id="index-EXIT_005fSUCCESS"></span>
<span id="index-return-value-of-main"></span>

In general, the return value from `main` indicates the program’s *exit
status*. A value of zero or EXIT_SUCCESS indicates success and
EXIT_FAILURE indicates an error. Otherwise, the significance of the
value returned is implementation-defined.

Reaching the `}` at the end of `main` without a return, or executing a
`return` statement with no value (that is, `return;`) are both
equivalent. In C89, the effect of this is undefined, but in C99 the
effect is equivalent to `return 0;`.

You can write your `main` function to have no parameters (that is, as
`int main (void)`), or to accept parameters from the command line. Here
is a very simple `main` function with no parameters:

<div class="example">

``` example
int
main (void)
{
  puts ("Hi there!");
  return 0;
}
```

</div>

To accept command line parameters, you need to have two parameters in
the `main` function, `int argc` followed by `char *argv[]`. You can
change the names of those parameters, but they must have those data
types—`int` and array of pointers to `char`. `argc` is the number of
command line parameters, including the name of the program itself.
`argv` is an array of the parameters, as character strings. `argv[0]`,
the first element in the array, is the name of the program as typed at
the command line<a href="#FOOT4" id="DOCF4"><sup>4</sup></a>; any
following array elements are the parameters that followed the name of
the program.

Here is an example `main` function that accepts command line parameters,
and prints out what those parameters are:

<div class="example">

``` example
int
main (int argc, char *argv[])
{
  int counter;

  for (counter = 0; counter < argc; counter++)
    printf ("%s\n", argv[counter]);
  
  return 0;
}
```

</div>

------------------------------------------------------------------------

<span id="Recursive-Functions"></span>

<div class="header">

Next: <a href="#Static-Functions" accesskey="n" rel="next">Static
Functions</a>, Previous:
<a href="#The-main-Function" accesskey="p" rel="prev">The main
Function</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Recursive-Functions-1"></span>

### 5.8 Recursive Functions

<span id="index-recursive-functions"></span>
<span id="index-functions_002c-recursive"></span>

You can write a function that is recursive—a function that calls itself.
Here is an example that computes the factorial of an integer:

<div class="example">

``` example
int
factorial (int x)
{
  if (x < 1)
    return 1;
  else
    return (x * factorial (x - 1));
}
```

</div>

Be careful that you do not write a function that is infinitely
recursive. In the above example, once `x` is 1, the recursion stops.
However, in the following example, the recursion does not stop until the
program is interrupted or runs out of memory:

<div class="example">

``` example
int
watermelon (int x)
{
  return (watermelon (x));
}
```

</div>

Functions can also be indirectly recursive, of course.

------------------------------------------------------------------------

<span id="Static-Functions"></span>

<div class="header">

Next: <a href="#Nested-Functions" accesskey="n" rel="next">Nested
Functions</a>, Previous:
<a href="#Recursive-Functions" accesskey="p" rel="prev">Recursive
Functions</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Static-Functions-1"></span>

### 5.9 Static Functions

<span id="index-static-functions"></span>
<span id="index-functions_002c-static"></span>
<span id="index-static-linkage"></span>

You can define a function to be static if you want it to be callable
only within the source file where it is defined:

<div class="example">

``` example
static int
foo (int x)
{
  return x + 42;
}
```

</div>

This is useful if you are building a reusable library of functions and
need to include some subroutines that should not be callable by the end
user.

Functions which are defined in this way are said to have *static
linkage*. Unfortunately the `static` keyword has multiple meanings;
[Storage Class Specifiers](#Storage-Class-Specifiers).

------------------------------------------------------------------------

<span id="Nested-Functions"></span>

<div class="header">

Previous: <a href="#Static-Functions" accesskey="p" rel="prev">Static
Functions</a>, Up:
<a href="#Functions" accesskey="u" rel="up">Functions</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Nested-Functions-1"></span>

### 5.10 Nested Functions

<span id="index-nested-functions"></span>
<span id="index-functions_002c-nested"></span>

As a GNU C extension, you can define functions within other functions, a
technique known as nesting functions.

Here is an example of a tail-recursive factorial function, defined using
a nested function:

<div class="example">

``` example
int
factorial (int x)
{
  int
  factorial_helper (int a, int b)
  {
    if (a < 1)
    {
      return b;
    }
    else
    {
      return factorial_helper ((a - 1), (a * b));
    }
  }

 return factorial_helper (x, 1);
}
```

</div>

Note that nested functions must be defined along with variable
declarations at the beginning of a function, and all other statements
follow.

------------------------------------------------------------------------

<span id="Program-Structure-and-Scope"></span>

<div class="header">

Next: <a href="#A-Sample-Program" accesskey="n" rel="next">A Sample
Program</a>, Previous:
<a href="#Functions" accesskey="p" rel="prev">Functions</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Program-Structure-and-Scope-1"></span>

## 6 Program Structure and Scope

Now that we have seen all of the fundamental elements of C programs,
it’s time to look at the big picture.

|  |  |  |
|:---|----|:---|
| • <a href="#Program-Structure" accesskey="1">Program Structure</a>: |    |  |
| • <a href="#Scope" accesskey="2">Scope</a>: |    |  |

------------------------------------------------------------------------

<span id="Program-Structure"></span>

<div class="header">

Next: <a href="#Scope" accesskey="n" rel="next">Scope</a>, Up:
<a href="#Program-Structure-and-Scope" accesskey="u" rel="up">Program
Structure and Scope</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Program-Structure-1"></span>

### 6.1 Program Structure

<span id="index-program-structure"></span>
<span id="index-structure_002c-program"></span>

A C program may exist entirely within a single source file, but more
commonly, any non-trivial program will consist of several custom header
files and source files, and will also include and link with files from
existing libraries.

By convention, header files (with a “.h” extension) contain variable and
function declarations, and source files (with a “.c” extension) contain
the corresponding definitions. Source files may also store declarations,
if these declarations are not for objects which need to be seen by other
files. However, header files almost certainly should not contain any
definitions.

For example, if you write a function that computes square roots, and you
wanted this function to be accessible to files other than where you
define the function, then you would put the function declaration into a
header file (with a “.h” file extension):

<div class="example">

``` example
/* sqrt.h */

double
computeSqrt (double x);
```

</div>

This header file could be included by other source files which need to
use your function, but do not need to know how it was implemented.

The implementation of the function would then go into a corresponding
source file (with a “.c” file extension):

<div class="example">

``` example
/* sqrt.c */
#include "sqrt.h"

double
computeSqrt (double x)
{
  double result;
  …
  return result;
}
```

</div>

------------------------------------------------------------------------

<span id="Scope"></span>

<div class="header">

Previous: <a href="#Program-Structure" accesskey="p" rel="prev">Program
Structure</a>, Up:
<a href="#Program-Structure-and-Scope" accesskey="u" rel="up">Program
Structure and Scope</a>   \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Scope-1"></span>

### 6.2 Scope

<span id="index-scope"></span>

Scope refers to what parts of the program can “see” a declared object. A
declared object can be visible only within a particular function, or
within a particular file, or may be visible to an entire set of files by
way of including header files and using `extern` declarations.

Unless explicitly stated otherwise, declarations made at the top-level
of a file (i.e., not within a function) are visible to the entire file,
including from within functions, but are not visible outside of the
file.

Declarations made within functions are visible only within those
functions.

A declaration is not visible to declarations that came before it; for
example:

<div class="example">

``` example
int x = 5;
int y = x + 10;
```

</div>

will work, but:

<div class="example">

``` example
int x = y + 10;
int y = 5;
```

</div>

will not.

See [Storage Class Specifiers](#Storage-Class-Specifiers), for more
information on changing the scope of declared objects. Also see [Static
Functions](#Static-Functions).

------------------------------------------------------------------------

<span id="A-Sample-Program"></span>

<div class="header">

Next: <a href="#Overflow" accesskey="n" rel="next">Overflow</a>,
Previous:
<a href="#Program-Structure-and-Scope" accesskey="p" rel="prev">Program
Structure and Scope</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="A-Sample-Program-1"></span>

## 7 A Sample Program

<span id="index-sample-program"></span>
<span id="index-hello-program"></span>

To conclude our description of C, here is a complete program written in
C, consisting of both a C source file and a header file. This program is
an expanded version of the quintessential “hello world” program, and
serves as an example of how to format and structure C code for use in
programs for FSF Project GNU. (You can always download the most recent
version of this program, including sample makefiles and other examples
of how to produce GNU software, from
`http://www.gnu.org/software/hello`.)

This program uses features of the preprocessor; for a description of
preprocessor macros, see The C Preprocessor, available as part of the
GCC documentation.

|                                                       |     |     |
|:------------------------------------------------------|-----|:----|
| • <a href="#hello_002ec" accesskey="1">hello.c</a>:   |     |     |
| • <a href="#system_002eh" accesskey="2">system.h</a>: |     |     |

------------------------------------------------------------------------

<span id="hello_002ec"></span>

<div class="header">

Next: <a href="#system_002eh" accesskey="n" rel="next">system.h</a>, Up:
<a href="#A-Sample-Program" accesskey="u" rel="up">A Sample Program</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="hello_002ec-1"></span>

### 7.1 `hello.c`

<span id="index-hello_002ec"></span>

<div class="smallexample">

``` smallexample
/* hello.c -- print a greeting message and exit.

   Copyright (C) 1992, 1995, 1996, 1997, 1998, 1999, 2000, 2001, 2002,
   2005, 2006, 2007 Free Software Foundation, Inc.

   This program is free software; you can redistribute it and/or modify
   it under the terms of the GNU General Public License as published by
   the Free Software Foundation; either version 3, or (at your option)
   any later version.

   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU General Public License for more details.

   You should have received a copy of the GNU General Public License
   along with this program; if not, write to the Free Software Foundation,
   Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.  */

#include <config.h>
#include "system.h"

/* String containing name the program is called with.  */
const char *program_name;

static const struct option longopts[] =
{
  { "greeting", required_argument, NULL, 'g' },
  { "help", no_argument, NULL, 'h' },
  { "next-generation", no_argument, NULL, 'n' },
  { "traditional", no_argument, NULL, 't' },
  { "version", no_argument, NULL, 'v' },
  { NULL, 0, NULL, 0 }
};

static void print_help (void);
static void print_version (void);

int
main (int argc, char *argv[])
{
  int optc;
  int t = 0, n = 0, lose = 0;
  const char *greeting = NULL;

  program_name = argv[0];

  /* Set locale via LC_ALL.  */
  setlocale (LC_ALL, "");

#if ENABLE_NLS
  /* Set the text message domain.  */
  bindtextdomain (PACKAGE, LOCALEDIR);
  textdomain (PACKAGE);
#endif

  /* Even exiting has subtleties.  The /dev/full device on GNU/Linux
     can be used for testing whether writes are checked properly.  For
     instance, hello >/dev/full should exit unsuccessfully.  On exit,
     if any writes failed, change the exit status.  This is
     implemented in the Gnulib module "closeout".  */
  atexit (close_stdout);

  while ((optc = getopt_long (argc, argv, "g:hntv", longopts, NULL)) != -1)
    switch (optc)
      {
      /* One goal here is having --help and --version exit immediately,
         per GNU coding standards.  */
      case 'v':
        print_version ();
        exit (EXIT_SUCCESS);
        break;
      case 'g':
        greeting = optarg;
        break;
      case 'h':
        print_help ();
        exit (EXIT_SUCCESS);
        break;
      case 'n':
        n = 1;
        break;
      case 't':
        t = 1;
        break;
      default:
        lose = 1;
        break;
      }

  if (lose || optind < argc)
    {
      /* Print error message and exit.  */
      if (optind < argc)
        fprintf (stderr, _("%s: extra operand: %s\n"),
         program_name, argv[optind]);
      fprintf (stderr, _("Try `%s --help' for more information.\n"),
               program_name);
      exit (EXIT_FAILURE);
    }

  /* Print greeting message and exit. */
  if (t)
    printf (_("hello, world\n"));

  else if (n)
    /* TRANSLATORS: Use box drawing characters or other fancy stuff
       if your encoding (e.g., UTF-8) allows it.  If done so add the
       following note, please:

       [Note: For best viewing results use a UTF-8 locale, please.]
    */
    printf (_("\
+---------------+\n\
| Hello, world! |\n\
+---------------+\n\
"));

  else
    {
      if (!greeting)
        greeting = _("Hello, world!");
      puts (greeting);
    }
  
  exit (EXIT_SUCCESS);
}



/* Print help info.  This long message is split into
   several pieces to help translators be able to align different
   blocks and identify the various pieces.  */

static void
print_help (void)
{
  /* TRANSLATORS: --help output 1 (synopsis)
     no-wrap */
        printf (_("\
Usage: %s [OPTION]...\n"), program_name);

  /* TRANSLATORS: --help output 2 (brief description)
     no-wrap */
  fputs (_("\
Print a friendly, customizable greeting.\n"), stdout);

  puts ("");
  /* TRANSLATORS: --help output 3: options 1/2
     no-wrap */
  fputs (_("\
  -h, --help          display this help and exit\n\
  -v, --version       display version information and exit\n"), stdout);

  puts ("");
  /* TRANSLATORS: --help output 4: options 2/2
     no-wrap */
  fputs (_("\
  -t, --traditional       use traditional greeting format\n\
  -n, --next-generation   use next-generation greeting format\n\
  -g, --greeting=TEXT     use TEXT as the greeting message\n"), stdout);

  printf ("\n");
  /* TRANSLATORS: --help output 5 (end)
     TRANSLATORS: the placeholder indicates the bug-reporting address
     for this application.  Please add _another line_ with the
     address for translation bugs.
     no-wrap */
  printf (_("\
Report bugs to <%s>.\n"), PACKAGE_BUGREPORT);
}



/* Print version and copyright information.  */

static void
print_version (void)
{
  printf ("hello (GNU %s) %s\n", PACKAGE, VERSION);
  /* xgettext: no-wrap */
  puts ("");
  
  /* It is important to separate the year from the rest of the message,
     as done here, to avoid having to retranslate the message when a new
     year comes around.  */
  printf (_("\
Copyright (C) %s Free Software Foundation, Inc.\n\
License GPLv3+: GNU GPL version 3 or later\
<http://gnu.org/licenses/gpl.html>\n\
This is free software: you are free to change and redistribute it.\n\
There is NO WARRANTY, to the extent permitted by law.\n"),
              "2007");
}
```

</div>

------------------------------------------------------------------------

<span id="system_002eh"></span>

<div class="header">

Previous: <a href="#hello_002ec" accesskey="p" rel="prev">hello.c</a>,
Up:
<a href="#A-Sample-Program" accesskey="u" rel="up">A Sample Program</a>
  \[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="system_002eh-1"></span>

### 7.2 `system.h`

<span id="index-system_002eh"></span>

<div class="smallexample">

``` smallexample
/* system.h: system-dependent declarations; include this first.
   Copyright (C) 1996, 2005, 2006, 2007 Free Software Foundation, Inc.

   This program is free software; you can redistribute it and/or modify
   it under the terms of the GNU General Public License as published by
   the Free Software Foundation; either version 3, or (at your option)
   any later version.

   This program is distributed in the hope that it will be useful,
   but WITHOUT ANY WARRANTY; without even the implied warranty of
   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
   GNU General Public License for more details.

   You should have received a copy of the GNU General Public License
   along with this program; if not, write to the Free Software Foundation,
   Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.  */

#ifndef HELLO_SYSTEM_H
#define HELLO_SYSTEM_H

/* Assume ANSI C89 headers are available.  */
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

/* Use POSIX headers.  If they are not available, we use the substitute
   provided by gnulib.  */
#include <getopt.h>
#include <unistd.h>

/* Internationalization.  */
#include "gettext.h"
#define _(str) gettext (str)
#define N_(str) gettext_noop (str)

/* Check for errors on write.  */
#include "closeout.h"

#endif /* HELLO_SYSTEM_H */
```

</div>

------------------------------------------------------------------------

<span id="Overflow"></span>

<div class="header">

Next:
<a href="#GNU-Free-Documentation-License" accesskey="n" rel="next">GNU
Free Documentation License</a>, Previous:
<a href="#A-Sample-Program" accesskey="p" rel="prev">A Sample
Program</a>, Up: <a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Overflow-1"></span>

## Appendix A Overflow

\[This appendix, written principally by Paul Eggert, is from the GNU
Autoconf manual. We thought that it would be helpful to include here.
–TJR\]

In practice many portable C programs assume that signed integer overflow
wraps around reliably using two’s complement arithmetic. Yet the C
standard says that program behavior is undefined on overflow, and in a
few cases C programs do not work on some modern implementations because
their overflows do not wrap around as their authors expected.
Conversely, in signed integer remainder, the C standard requires
overflow behavior that is commonly not implemented.

|  |  |  |
|:---|----|:---|
| • <a href="#Integer-Overflow-Basics" accesskey="1">Integer Overflow
Basics</a>: |    | Why integer overflow is a problem |
| • <a href="#Signed-Overflow-Examples" accesskey="2">Signed Overflow
Examples</a>: |    | Examples of code assuming wraparound |
| • <a href="#Optimization-and-Wraparound" accesskey="3">Optimization and
Wraparound</a>: |    | Optimizations that break uses of wraparound |
| • <a href="#Signed-Overflow-Advice" accesskey="4">Signed Overflow
Advice</a>: |    | Practical advice for signed overflow issues |
| • <a href="#Signed-Integer-Division" accesskey="5">Signed Integer
Division</a>: |    | `INT_MIN / -1` and `INT_MIN % -1` |

------------------------------------------------------------------------

<span id="Integer-Overflow-Basics"></span>

<div class="header">

Next:
<a href="#Signed-Overflow-Examples" accesskey="n" rel="next">Signed
Overflow Examples</a>, Up:
<a href="#Overflow" accesskey="u" rel="up">Overflow</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Basics-of-Integer-Overflow"></span>

### A.1 Basics of Integer Overflow

<span id="index-integer-overflow"></span>
<span id="index-overflow_002c-signed-integer"></span>
<span id="index-signed-integer-overflow"></span>
<span id="index-wraparound-arithmetic"></span>

In languages like C, unsigned integer overflow reliably wraps around;
e.g., `UINT_MAX + 1` yields zero. This is guaranteed by the C standard
and is portable in practice, unless you specify aggressive, nonstandard
optimization options suitable only for special applications.

In contrast, the C standard says that signed integer overflow leads to
undefined behavior where a program can do anything, including dumping
core or overrunning a buffer. The misbehavior can even precede the
overflow. Such an overflow can occur during addition, subtraction,
multiplication, division, and left shift.

Despite this requirement of the standard, many C programs assume that
signed integer overflow silently wraps around modulo a power of two,
using two’s complement arithmetic, so long as you cast the resulting
value to a signed integer type or store it into a signed integer
variable. If you use conservative optimization flags, such programs are
generally portable to the vast majority of modern platforms, with a few
exceptions discussed later.

For historical reasons the C standard also allows implementations with
ones’ complement or signed magnitude arithmetic, but it is safe to
assume two’s complement nowadays.

Also, overflow can occur when converting an out-of-range value to a
signed integer type. Here a standard implementation must define what
happens, but this might include raising an exception. In practice all
known implementations support silent wraparound in this case, so you
need not worry about other possibilities.

------------------------------------------------------------------------

<span id="Signed-Overflow-Examples"></span>

<div class="header">

Next: <a href="#Optimization-and-Wraparound" accesskey="n"
rel="next">Optimization and Wraparound</a>, Previous:
<a href="#Integer-Overflow-Basics" accesskey="p" rel="prev">Integer
Overflow Basics</a>, Up:
<a href="#Overflow" accesskey="u" rel="up">Overflow</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Examples-of-Code-Assuming-Wraparound-Overflow"></span>

### A.2 Examples of Code Assuming Wraparound Overflow

<span id="index-integer-overflow-1"></span>
<span id="index-overflow_002c-signed-integer-1"></span>
<span id="index-signed-integer-overflow-1"></span>
<span id="index-wraparound-arithmetic-1"></span>

There has long been a tension between what the C standard requires for
signed integer overflow, and what C programs commonly assume. The
standard allows aggressive optimizations based on assumptions that
overflow never occurs, but many practical C programs rely on overflow
wrapping around. These programs do not conform to the standard, but they
commonly work in practice because compiler writers are understandably
reluctant to implement optimizations that would break many programs,
unless perhaps a user specifies aggressive optimization.

The C Standard says that if a program has signed integer overflow its
behavior is undefined, and the undefined behavior can even precede the
overflow. To take an extreme example:

<div class="example">

``` example
if (password == expected_password)
  allow_superuser_privileges ();
else if (counter++ == INT_MAX)
  abort ();
else
  printf ("%d password mismatches\n", counter);
```

</div>

If the `int` variable `counter` equals `INT_MAX`, `counter++` must
overflow and the behavior is undefined, so the C standard allows the
compiler to optimize away the test against `INT_MAX` and the `abort`
call. Worse, if an earlier bug in the program lets the compiler deduce
that `counter == INT_MAX` or that `counter` previously overflowed, the C
standard allows the compiler to optimize away the password test and
generate code that allows superuser privileges unconditionally.

Despite this requirement by the standard, it has long been common for C
code to assume wraparound arithmetic after signed overflow, and all
known practical C implementations support some C idioms that assume
wraparound signed arithmetic, even if the idioms do not conform strictly
to the standard. If your code looks like the following examples it will
almost surely work with real-world compilers.

Here is an example derived from the 7th Edition Unix implementation of
`atoi` (1979-01-10):

<div class="example">

``` example
char *p;
int f, n;
…
while (*p >= '0' && *p <= '9')
  n = n * 10 + *p++ - '0';
return (f ? -n : n);
```

</div>

Even if the input string is in range, on most modern machines this has
signed overflow when computing the most negative integer (the `-n`
overflows) or a value near an extreme integer (the first `+` overflows).

Here is another example, derived from the 7th Edition implementation of
`rand` (1979-01-10). Here the programmer expects both multiplication and
addition to wrap on overflow:

<div class="example">

``` example
static long int randx = 1;
…
randx = randx * 1103515245 + 12345;
return (randx >> 16) & 077777;
```

</div>

In the following example, derived from the GNU C Library 2.5
implementation of `mktime` (2006-09-09), the code assumes wraparound
arithmetic in `+` to detect signed overflow:

<div class="example">

``` example
time_t t, t1, t2;
int sec_requested, sec_adjustment;
…
t1 = t + sec_requested;
t2 = t1 + sec_adjustment;
if (((t1 < t) != (sec_requested < 0))
    || ((t2 < t1) != (sec_adjustment < 0)))
  return -1;
```

</div>

If your code looks like these examples, it is probably safe even though
it does not strictly conform to the C standard. This might lead one to
believe that one can generally assume wraparound on overflow, but that
is not always true, as can be seen in the next section.

------------------------------------------------------------------------

<span id="Optimization-and-Wraparound"></span>

<div class="header">

Next: <a href="#Signed-Overflow-Advice" accesskey="n" rel="next">Signed
Overflow Advice</a>, Previous:
<a href="#Signed-Overflow-Examples" accesskey="p" rel="prev">Signed
Overflow Examples</a>, Up:
<a href="#Overflow" accesskey="u" rel="up">Overflow</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Optimizations-That-Break-Wraparound-Arithmetic"></span>

### A.3 Optimizations That Break Wraparound Arithmetic

<span id="index-loop-induction"></span>

Compilers sometimes generate code that is incompatible with wraparound
integer arithmetic. A simple example is an algebraic simplification: a
compiler might translate `(i * 2000) / 1000` to `i * 2` because it
assumes that `i * 2000` does not overflow. The translation is not
equivalent to the original when overflow occurs: e.g., in the typical
case of 32-bit signed two’s complement wraparound `int`, if `i` has type
`int` and value `1073742`, the original expression returns -2147483 but
the optimized version returns the mathematically correct value 2147484.

More subtly, loop induction optimizations often exploit the undefined
behavior of signed overflow. Consider the following contrived function
`sumc`:

<div class="example">

``` example
int
sumc (int lo, int hi)
{
  int sum = 0;
  int i;
  for (i = lo; i <= hi; i++)
    sum ^= i * 53;
  return sum;
}
```

</div>

To avoid multiplying by 53 each time through the loop, an optimizing
compiler might internally transform `sumc` to the equivalent of the
following:

<div class="example">

``` example
int
transformed_sumc (int lo, int hi)
{
  int sum = 0;
  int hic = hi * 53;
  int ic;
  for (ic = lo * 53; ic <= hic; ic += 53)
    sum ^= ic;
  return sum;
}
```

</div>

This transformation is allowed by the C standard, but it is invalid for
wraparound arithmetic when `INT_MAX / 53 < hi`, because then the
overflow in computing expressions like `hi * 53` can cause the
expression `i <= hi` to yield a different value from the transformed
expression `ic <= hic`.

For this reason, compilers that use loop induction and similar
techniques often do not support reliable wraparound arithmetic when a
loop induction variable like `ic` is involved. Since loop induction
variables are generated by the compiler, and are not visible in the
source code, it is not always trivial to say whether the problem affects
your code.

Hardly any code actually depends on wraparound arithmetic in cases like
these, so in practice these loop induction optimizations are almost
always useful. However, edge cases in this area can cause problems. For
example:

<div class="example">

``` example
int j;
for (j = 1; 0 < j; j *= 2)
  test (j);
```

</div>

Here, the loop attempts to iterate through all powers of 2 that `int`
can represent, but the C standard allows a compiler to optimize away the
comparison and generate an infinite loop, under the argument that
behavior is undefined on overflow. As of this writing this optimization
is not done by any production version of GCC with `-O2`, but it might be
performed by other compilers, or by more aggressive GCC optimization
options, and the GCC developers have not decided whether it will
continue to work with GCC and `-O2`.

------------------------------------------------------------------------

<span id="Signed-Overflow-Advice"></span>

<div class="header">

Next: <a href="#Signed-Integer-Division" accesskey="n" rel="next">Signed
Integer Division</a>, Previous:
<a href="#Optimization-and-Wraparound" accesskey="p"
rel="prev">Optimization and Wraparound</a>, Up:
<a href="#Overflow" accesskey="u" rel="up">Overflow</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Practical-Advice-for-Signed-Overflow-Issues"></span>

### A.4 Practical Advice for Signed Overflow Issues

<span id="index-integer-overflow-2"></span>
<span id="index-overflow_002c-signed-integer-2"></span>
<span id="index-signed-integer-overflow-2"></span>
<span id="index-wraparound-arithmetic-2"></span>

Ideally the safest approach is to avoid signed integer overflow
entirely. For example, instead of multiplying two signed integers, you
can convert them to unsigned integers, multiply the unsigned values,
then test whether the result is in signed range.

Rewriting code in this way will be inconvenient, though, particularly if
the signed values might be negative. Also, it may hurt performance.
Using unsigned arithmetic to check for overflow is particularly painful
to do portably and efficiently when dealing with an integer type like
`uid_t` whose width and signedness vary from platform to platform.

Furthermore, many C applications pervasively assume wraparound behavior
and typically it is not easy to find and remove all these assumptions.
Hence it is often useful to maintain nonstandard code that assumes
wraparound on overflow, instead of rewriting the code. The rest of this
section attempts to give practical advice for this situation.

If your code wants to detect signed integer overflow in `sum = a + b`,
it is generally safe to use an expression like `(sum < a) != (b < 0)`.

If your code uses a signed loop index, make sure that the index cannot
overflow, along with all signed expressions derived from the index. Here
is a contrived example of problematic code with two instances of
overflow.

<div class="example">

``` example
for (i = INT_MAX - 10; i <= INT_MAX; i++)
  if (i + 1 < 0)
    {
      report_overflow ();
      break;
    }
```

</div>

Because of the two overflows, a compiler might optimize away or
transform the two comparisons in a way that is incompatible with the
wraparound assumption.

If your code uses an expression like `(i * 2000) / 1000` and you
actually want the multiplication to wrap around on overflow, use
unsigned arithmetic to do it, e.g., `((int) (i * 2000u)) / 1000`.

If your code assumes wraparound behavior and you want to insulate it
against any GCC optimizations that would fail to support that behavior,
you should use GCC’s `-fwrapv` option, which causes signed overflow to
wrap around reliably (except for division and remainder, as discussed in
the next section).

If you need to port to platforms where signed integer overflow does not
reliably wrap around (e.g., due to hardware overflow checking, or to
highly aggressive optimizations), you should consider debugging with
GCC’s `-ftrapv` option, which causes signed overflow to raise an
exception.

------------------------------------------------------------------------

<span id="Signed-Integer-Division"></span>

<div class="header">

Previous:
<a href="#Signed-Overflow-Advice" accesskey="p" rel="prev">Signed
Overflow Advice</a>, Up:
<a href="#Overflow" accesskey="u" rel="up">Overflow</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Signed-Integer-Division-and-Integer-Overflow"></span>

### A.5 Signed Integer Division and Integer Overflow

<span id="index-division_002c-integer"></span>

Overflow in signed integer division is not always harmless: for example,
on CPUs of the i386 family, dividing `INT_MIN` by `-1` yields a SIGFPE
signal which by default terminates the program. Worse, taking the
remainder of these two values typically yields the same signal on these
CPUs, even though the C standard requires `INT_MIN % -1` to yield zero
because the expression does not overflow.

------------------------------------------------------------------------

<span id="GNU-Free-Documentation-License"></span>

<div class="header">

Next: <a href="#Index" accesskey="n" rel="next">Index</a>, Previous:
<a href="#Overflow" accesskey="p" rel="prev">Overflow</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="GNU-Free-Documentation-License-1"></span>

## GNU Free Documentation License

<div align="center">

Version 1.3, 3 November 2008

</div>

<div class="display">

``` display
Copyright © 2000, 2001, 2002, 2007, 2008 Free Software Foundation, Inc.
http://fsf.org/

Everyone is permitted to copy and distribute verbatim copies
of this license document, but changing it is not allowed.
```

</div>

1.  PREAMBLE

    The purpose of this License is to make a manual, textbook, or other
    functional and useful document *free* in the sense of freedom: to
    assure everyone the effective freedom to copy and redistribute it,
    with or without modifying it, either commercially or
    noncommercially. Secondarily, this License preserves for the author
    and publisher a way to get credit for their work, while not being
    considered responsible for modifications made by others.

    This License is a kind of “copyleft”, which means that derivative
    works of the document must themselves be free in the same sense. It
    complements the GNU General Public License, which is a copyleft
    license designed for free software.

    We have designed this License in order to use it for manuals for
    free software, because free software needs free documentation: a
    free program should come with manuals providing the same freedoms
    that the software does. But this License is not limited to software
    manuals; it can be used for any textual work, regardless of subject
    matter or whether it is published as a printed book. We recommend
    this License principally for works whose purpose is instruction or
    reference.

2.  APPLICABILITY AND DEFINITIONS

    This License applies to any manual or other work, in any medium,
    that contains a notice placed by the copyright holder saying it can
    be distributed under the terms of this License. Such a notice grants
    a world-wide, royalty-free license, unlimited in duration, to use
    that work under the conditions stated herein. The “Document”, below,
    refers to any such manual or work. Any member of the public is a
    licensee, and is addressed as “you”. You accept the license if you
    copy, modify or distribute the work in a way requiring permission
    under copyright law.

    A “Modified Version” of the Document means any work containing the
    Document or a portion of it, either copied verbatim, or with
    modifications and/or translated into another language.

    A “Secondary Section” is a named appendix or a front-matter section
    of the Document that deals exclusively with the relationship of the
    publishers or authors of the Document to the Document’s overall
    subject (or to related matters) and contains nothing that could fall
    directly within that overall subject. (Thus, if the Document is in
    part a textbook of mathematics, a Secondary Section may not explain
    any mathematics.) The relationship could be a matter of historical
    connection with the subject or with related matters, or of legal,
    commercial, philosophical, ethical or political position regarding
    them.

    The “Invariant Sections” are certain Secondary Sections whose titles
    are designated, as being those of Invariant Sections, in the notice
    that says that the Document is released under this License. If a
    section does not fit the above definition of Secondary then it is
    not allowed to be designated as Invariant. The Document may contain
    zero Invariant Sections. If the Document does not identify any
    Invariant Sections then there are none.

    The “Cover Texts” are certain short passages of text that are
    listed, as Front-Cover Texts or Back-Cover Texts, in the notice that
    says that the Document is released under this License. A Front-Cover
    Text may be at most 5 words, and a Back-Cover Text may be at most 25
    words.

    A “Transparent” copy of the Document means a machine-readable copy,
    represented in a format whose specification is available to the
    general public, that is suitable for revising the document
    straightforwardly with generic text editors or (for images composed
    of pixels) generic paint programs or (for drawings) some widely
    available drawing editor, and that is suitable for input to text
    formatters or for automatic translation to a variety of formats
    suitable for input to text formatters. A copy made in an otherwise
    Transparent file format whose markup, or absence of markup, has been
    arranged to thwart or discourage subsequent modification by readers
    is not Transparent. An image format is not Transparent if used for
    any substantial amount of text. A copy that is not “Transparent” is
    called “Opaque”.

    Examples of suitable formats for Transparent copies include plain
    <span class="small">ASCII</span> without markup, Texinfo input
    format, LaTeX input format, SGML or XML using a publicly available
    DTD, and standard-conforming simple HTML, PostScript or PDF designed
    for human modification. Examples of transparent image formats
    include PNG, XCF and JPG. Opaque formats include proprietary formats
    that can be read and edited only by proprietary word processors,
    SGML or XML for which the DTD and/or processing tools are not
    generally available, and the machine-generated HTML, PostScript or
    PDF produced by some word processors for output purposes only.

    The “Title Page” means, for a printed book, the title page itself,
    plus such following pages as are needed to hold, legibly, the
    material this License requires to appear in the title page. For
    works in formats which do not have any title page as such, “Title
    Page” means the text near the most prominent appearance of the
    work’s title, preceding the beginning of the body of the text.

    The “publisher” means any person or entity that distributes copies
    of the Document to the public.

    A section “Entitled XYZ” means a named subunit of the Document whose
    title either is precisely XYZ or contains XYZ in parentheses
    following text that translates XYZ in another language. (Here XYZ
    stands for a specific section name mentioned below, such as
    “Acknowledgements”, “Dedications”, “Endorsements”, or “History”.) To
    “Preserve the Title” of such a section when you modify the Document
    means that it remains a section “Entitled XYZ” according to this
    definition.

    The Document may include Warranty Disclaimers next to the notice
    which states that this License applies to the Document. These
    Warranty Disclaimers are considered to be included by reference in
    this License, but only as regards disclaiming warranties: any other
    implication that these Warranty Disclaimers may have is void and has
    no effect on the meaning of this License.

3.  VERBATIM COPYING

    You may copy and distribute the Document in any medium, either
    commercially or noncommercially, provided that this License, the
    copyright notices, and the license notice saying this License
    applies to the Document are reproduced in all copies, and that you
    add no other conditions whatsoever to those of this License. You may
    not use technical measures to obstruct or control the reading or
    further copying of the copies you make or distribute. However, you
    may accept compensation in exchange for copies. If you distribute a
    large enough number of copies you must also follow the conditions in
    section 3.

    You may also lend copies, under the same conditions stated above,
    and you may publicly display copies.

4.  COPYING IN QUANTITY

    If you publish printed copies (or copies in media that commonly have
    printed covers) of the Document, numbering more than 100, and the
    Document’s license notice requires Cover Texts, you must enclose the
    copies in covers that carry, clearly and legibly, all these Cover
    Texts: Front-Cover Texts on the front cover, and Back-Cover Texts on
    the back cover. Both covers must also clearly and legibly identify
    you as the publisher of these copies. The front cover must present
    the full title with all words of the title equally prominent and
    visible. You may add other material on the covers in addition.
    Copying with changes limited to the covers, as long as they preserve
    the title of the Document and satisfy these conditions, can be
    treated as verbatim copying in other respects.

    If the required texts for either cover are too voluminous to fit
    legibly, you should put the first ones listed (as many as fit
    reasonably) on the actual cover, and continue the rest onto adjacent
    pages.

    If you publish or distribute Opaque copies of the Document numbering
    more than 100, you must either include a machine-readable
    Transparent copy along with each Opaque copy, or state in or with
    each Opaque copy a computer-network location from which the general
    network-using public has access to download using public-standard
    network protocols a complete Transparent copy of the Document, free
    of added material. If you use the latter option, you must take
    reasonably prudent steps, when you begin distribution of Opaque
    copies in quantity, to ensure that this Transparent copy will remain
    thus accessible at the stated location until at least one year after
    the last time you distribute an Opaque copy (directly or through
    your agents or retailers) of that edition to the public.

    It is requested, but not required, that you contact the authors of
    the Document well before redistributing any large number of copies,
    to give them a chance to provide you with an updated version of the
    Document.

5.  MODIFICATIONS

    You may copy and distribute a Modified Version of the Document under
    the conditions of sections 2 and 3 above, provided that you release
    the Modified Version under precisely this License, with the Modified
    Version filling the role of the Document, thus licensing
    distribution and modification of the Modified Version to whoever
    possesses a copy of it. In addition, you must do these things in the
    Modified Version:

    1.  Use in the Title Page (and on the covers, if any) a title
        distinct from that of the Document, and from those of previous
        versions (which should, if there were any, be listed in the
        History section of the Document). You may use the same title as
        a previous version if the original publisher of that version
        gives permission.
    2.  List on the Title Page, as authors, one or more persons or
        entities responsible for authorship of the modifications in the
        Modified Version, together with at least five of the principal
        authors of the Document (all of its principal authors, if it has
        fewer than five), unless they release you from this requirement.
    3.  State on the Title page the name of the publisher of the
        Modified Version, as the publisher.
    4.  Preserve all the copyright notices of the Document.
    5.  Add an appropriate copyright notice for your modifications
        adjacent to the other copyright notices.
    6.  Include, immediately after the copyright notices, a license
        notice giving the public permission to use the Modified Version
        under the terms of this License, in the form shown in the
        Addendum below.
    7.  Preserve in that license notice the full lists of Invariant
        Sections and required Cover Texts given in the Document’s
        license notice.
    8.  Include an unaltered copy of this License.
    9.  Preserve the section Entitled “History”, Preserve its Title, and
        add to it an item stating at least the title, year, new authors,
        and publisher of the Modified Version as given on the Title
        Page. If there is no section Entitled “History” in the Document,
        create one stating the title, year, authors, and publisher of
        the Document as given on its Title Page, then add an item
        describing the Modified Version as stated in the previous
        sentence.
    10. Preserve the network location, if any, given in the Document for
        public access to a Transparent copy of the Document, and
        likewise the network locations given in the Document for
        previous versions it was based on. These may be placed in the
        “History” section. You may omit a network location for a work
        that was published at least four years before the Document
        itself, or if the original publisher of the version it refers to
        gives permission.
    11. For any section Entitled “Acknowledgements” or “Dedications”,
        Preserve the Title of the section, and preserve in the section
        all the substance and tone of each of the contributor
        acknowledgements and/or dedications given therein.
    12. Preserve all the Invariant Sections of the Document, unaltered
        in their text and in their titles. Section numbers or the
        equivalent are not considered part of the section titles.
    13. Delete any section Entitled “Endorsements”. Such a section may
        not be included in the Modified Version.
    14. Do not retitle any existing section to be Entitled
        “Endorsements” or to conflict in title with any Invariant
        Section.
    15. Preserve any Warranty Disclaimers.

    If the Modified Version includes new front-matter sections or
    appendices that qualify as Secondary Sections and contain no
    material copied from the Document, you may at your option designate
    some or all of these sections as invariant. To do this, add their
    titles to the list of Invariant Sections in the Modified Version’s
    license notice. These titles must be distinct from any other section
    titles.

    You may add a section Entitled “Endorsements”, provided it contains
    nothing but endorsements of your Modified Version by various
    parties—for example, statements of peer review or that the text has
    been approved by an organization as the authoritative definition of
    a standard.

    You may add a passage of up to five words as a Front-Cover Text, and
    a passage of up to 25 words as a Back-Cover Text, to the end of the
    list of Cover Texts in the Modified Version. Only one passage of
    Front-Cover Text and one of Back-Cover Text may be added by (or
    through arrangements made by) any one entity. If the Document
    already includes a cover text for the same cover, previously added
    by you or by arrangement made by the same entity you are acting on
    behalf of, you may not add another; but you may replace the old one,
    on explicit permission from the previous publisher that added the
    old one.

    The author(s) and publisher(s) of the Document do not by this
    License give permission to use their names for publicity for or to
    assert or imply endorsement of any Modified Version.

6.  COMBINING DOCUMENTS

    You may combine the Document with other documents released under
    this License, under the terms defined in section 4 above for
    modified versions, provided that you include in the combination all
    of the Invariant Sections of all of the original documents,
    unmodified, and list them all as Invariant Sections of your combined
    work in its license notice, and that you preserve all their Warranty
    Disclaimers.

    The combined work need only contain one copy of this License, and
    multiple identical Invariant Sections may be replaced with a single
    copy. If there are multiple Invariant Sections with the same name
    but different contents, make the title of each such section unique
    by adding at the end of it, in parentheses, the name of the original
    author or publisher of that section if known, or else a unique
    number. Make the same adjustment to the section titles in the list
    of Invariant Sections in the license notice of the combined work.

    In the combination, you must combine any sections Entitled “History”
    in the various original documents, forming one section Entitled
    “History”; likewise combine any sections Entitled
    “Acknowledgements”, and any sections Entitled “Dedications”. You
    must delete all sections Entitled “Endorsements.”

7.  COLLECTIONS OF DOCUMENTS

    You may make a collection consisting of the Document and other
    documents released under this License, and replace the individual
    copies of this License in the various documents with a single copy
    that is included in the collection, provided that you follow the
    rules of this License for verbatim copying of each of the documents
    in all other respects.

    You may extract a single document from such a collection, and
    distribute it individually under this License, provided you insert a
    copy of this License into the extracted document, and follow this
    License in all other respects regarding verbatim copying of that
    document.

8.  AGGREGATION WITH INDEPENDENT WORKS

    A compilation of the Document or its derivatives with other separate
    and independent documents or works, in or on a volume of a storage
    or distribution medium, is called an “aggregate” if the copyright
    resulting from the compilation is not used to limit the legal rights
    of the compilation’s users beyond what the individual works permit.
    When the Document is included in an aggregate, this License does not
    apply to the other works in the aggregate which are not themselves
    derivative works of the Document.

    If the Cover Text requirement of section 3 is applicable to these
    copies of the Document, then if the Document is less than one half
    of the entire aggregate, the Document’s Cover Texts may be placed on
    covers that bracket the Document within the aggregate, or the
    electronic equivalent of covers if the Document is in electronic
    form. Otherwise they must appear on printed covers that bracket the
    whole aggregate.

9.  TRANSLATION

    Translation is considered a kind of modification, so you may
    distribute translations of the Document under the terms of
    section 4. Replacing Invariant Sections with translations requires
    special permission from their copyright holders, but you may include
    translations of some or all Invariant Sections in addition to the
    original versions of these Invariant Sections. You may include a
    translation of this License, and all the license notices in the
    Document, and any Warranty Disclaimers, provided that you also
    include the original English version of this License and the
    original versions of those notices and disclaimers. In case of a
    disagreement between the translation and the original version of
    this License or a notice or disclaimer, the original version will
    prevail.

    If a section in the Document is Entitled “Acknowledgements”,
    “Dedications”, or “History”, the requirement (section 4) to Preserve
    its Title (section 1) will typically require changing the actual
    title.

10. TERMINATION

    You may not copy, modify, sublicense, or distribute the Document
    except as expressly provided under this License. Any attempt
    otherwise to copy, modify, sublicense, or distribute it is void, and
    will automatically terminate your rights under this License.

    However, if you cease all violation of this License, then your
    license from a particular copyright holder is reinstated (a)
    provisionally, unless and until the copyright holder explicitly and
    finally terminates your license, and (b) permanently, if the
    copyright holder fails to notify you of the violation by some
    reasonable means prior to 60 days after the cessation.

    Moreover, your license from a particular copyright holder is
    reinstated permanently if the copyright holder notifies you of the
    violation by some reasonable means, this is the first time you have
    received notice of violation of this License (for any work) from
    that copyright holder, and you cure the violation prior to 30 days
    after your receipt of the notice.

    Termination of your rights under this section does not terminate the
    licenses of parties who have received copies or rights from you
    under this License. If your rights have been terminated and not
    permanently reinstated, receipt of a copy of some or all of the same
    material does not give you any rights to use it.

11. FUTURE REVISIONS OF THIS LICENSE

    The Free Software Foundation may publish new, revised versions of
    the GNU Free Documentation License from time to time. Such new
    versions will be similar in spirit to the present version, but may
    differ in detail to address new problems or concerns. See
    <http://www.gnu.org/copyleft/>.

    Each version of the License is given a distinguishing version
    number. If the Document specifies that a particular numbered version
    of this License “or any later version” applies to it, you have the
    option of following the terms and conditions either of that
    specified version or of any later version that has been published
    (not as a draft) by the Free Software Foundation. If the Document
    does not specify a version number of this License, you may choose
    any version ever published (not as a draft) by the Free Software
    Foundation. If the Document specifies that a proxy can decide which
    future versions of this License can be used, that proxy’s public
    statement of acceptance of a version permanently authorizes you to
    choose that version for the Document.

12. RELICENSING

    “Massive Multiauthor Collaboration Site” (or “MMC Site”) means any
    World Wide Web server that publishes copyrightable works and also
    provides prominent facilities for anybody to edit those works. A
    public wiki that anybody can edit is an example of such a server. A
    “Massive Multiauthor Collaboration” (or “MMC”) contained in the site
    means any set of copyrightable works thus published on the MMC site.

    “CC-BY-SA” means the Creative Commons Attribution-Share Alike 3.0
    license published by Creative Commons Corporation, a not-for-profit
    corporation with a principal place of business in San Francisco,
    California, as well as future copyleft versions of that license
    published by that same organization.

    “Incorporate” means to publish or republish a Document, in whole or
    in part, as part of another Document.

    An MMC is “eligible for relicensing” if it is licensed under this
    License, and if all works that were first published under this
    License somewhere other than this MMC, and subsequently incorporated
    in whole or in part into the MMC, (1) had no cover texts or
    invariant sections, and (2) were thus incorporated prior to November
    1, 2008.

    The operator of an MMC Site may republish an MMC contained in the
    site under CC-BY-SA on the same site at any time before August 1,
    2009, provided the MMC is eligible for relicensing.

<span id="ADDENDUM_003a-How-to-use-this-License-for-your-documents"></span>

### ADDENDUM: How to use this License for your documents

To use this License in a document you have written, include a copy of
the License in the document and put the following copyright and license
notices just after the title page:

<div class="smallexample">

``` smallexample
  Copyright (C)  year  your name.
  Permission is granted to copy, distribute and/or modify this document
  under the terms of the GNU Free Documentation License, Version 1.3
  or any later version published by the Free Software Foundation;
  with no Invariant Sections, no Front-Cover Texts, and no Back-Cover
  Texts.  A copy of the license is included in the section entitled ``GNU
  Free Documentation License''.
```

</div>

If you have Invariant Sections, Front-Cover Texts and Back-Cover Texts,
replace the “with…Texts.” line with this:

<div class="smallexample">

``` smallexample
    with the Invariant Sections being list their titles, with
    the Front-Cover Texts being list, and with the Back-Cover Texts
    being list.
```

</div>

If you have Invariant Sections without Cover Texts, or some other
combination of the three, merge those two alternatives to suit the
situation.

If your document contains nontrivial examples of program code, we
recommend releasing these examples in parallel under your choice of free
software license, such as the GNU General Public License, to permit
their use in free software.

------------------------------------------------------------------------

<span id="Index"></span>

<div class="header">

Previous:
<a href="#GNU-Free-Documentation-License" accesskey="p" rel="prev">GNU
Free Documentation License</a>, Up:
<a href="#Top" accesskey="u" rel="up">Top</a>  
\[<a href="#SEC_Contents" rel="contents"
title="Table of contents">Contents</a>\]\[<a href="#Index" rel="index" title="Index">Index</a>\]

</div>

<span id="Index-1"></span>

## Index

|  |  |
|----|----|
| Jump to:   | <a href="#Index_cp_letter-A"
class="summary-letter"><strong>A</strong></a>   <a href="#Index_cp_letter-B"
class="summary-letter"><strong>B</strong></a>   <a href="#Index_cp_letter-C"
class="summary-letter"><strong>C</strong></a>   <a href="#Index_cp_letter-D"
class="summary-letter"><strong>D</strong></a>   <a href="#Index_cp_letter-E"
class="summary-letter"><strong>E</strong></a>   <a href="#Index_cp_letter-F"
class="summary-letter"><strong>F</strong></a>   <a href="#Index_cp_letter-G"
class="summary-letter"><strong>G</strong></a>   <a href="#Index_cp_letter-H"
class="summary-letter"><strong>H</strong></a>   <a href="#Index_cp_letter-I"
class="summary-letter"><strong>I</strong></a>   <a href="#Index_cp_letter-K"
class="summary-letter"><strong>K</strong></a>   <a href="#Index_cp_letter-L"
class="summary-letter"><strong>L</strong></a>   <a href="#Index_cp_letter-M"
class="summary-letter"><strong>M</strong></a>   <a href="#Index_cp_letter-N"
class="summary-letter"><strong>N</strong></a>   <a href="#Index_cp_letter-O"
class="summary-letter"><strong>O</strong></a>   <a href="#Index_cp_letter-P"
class="summary-letter"><strong>P</strong></a>   <a href="#Index_cp_letter-Q"
class="summary-letter"><strong>Q</strong></a>   <a href="#Index_cp_letter-R"
class="summary-letter"><strong>R</strong></a>   <a href="#Index_cp_letter-S"
class="summary-letter"><strong>S</strong></a>   <a href="#Index_cp_letter-T"
class="summary-letter"><strong>T</strong></a>   <a href="#Index_cp_letter-U"
class="summary-letter"><strong>U</strong></a>   <a href="#Index_cp_letter-V"
class="summary-letter"><strong>V</strong></a>   <a href="#Index_cp_letter-W"
class="summary-letter"><strong>W</strong></a>   |

<table class="index-cp" data-border="0">
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr>
<td></td>
<td style="text-align: left;">Index Entry</td>
<td> </td>
<td style="text-align: left;">Section</td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-A">A</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-accessing-array-elements">accessing array
elements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Accessing-Array-Elements">Accessing Array Elements</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-accessing-structure-members">accessing structure
members</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Accessing-Structure-Members">Accessing Structure Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-accessing-union-members">accessing union members</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Accessing-Union-Members">Accessing Union Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arithmetic-operators">arithmetic operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arithmetic-Operators">Arithmetic Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-array-elements_002c-accessing">array elements,
accessing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Accessing-Array-Elements">Accessing Array Elements</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-array-subscripts">array subscripts</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Array-Subscripts">Array Subscripts</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays">arrays</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays">Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays-as-strings">arrays as strings</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-as-Strings">Arrays as Strings</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays-of-structures">arrays of structures</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-of-Structures">Arrays of Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays-of-unions">arrays of unions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-of-Unions">Arrays of Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays_002c-declaring">arrays, declaring</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Arrays">Declaring Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays_002c-initializing">arrays, initializing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Arrays">Initializing Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-arrays_002c-multidimensional">arrays,
multidimensional</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Multidimensional-Arrays">Multidimensional Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-assignment-operators">assignment operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Assignment-Operators">Assignment Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-auto-storage-class-specifier"><code>auto</code> storage
class specifier</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Storage-Class-Specifiers">Storage Class Specifiers</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-B">B</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-bit-fields">bit fields</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Bit-Fields">Bit Fields</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-bit-shifting">bit shifting</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Bit-Shifting">Bit Shifting</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-bitwise-logical-operators">bitwise logical
operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Bitwise-Logical-Operators">Bitwise Logical Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-blocks">blocks</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Blocks">Blocks</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-break-statement"><code>break</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-break-Statement">The break Statement</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-C">C</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-calling-functions">calling functions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Calling-Functions">Calling Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-casts">casts</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Type-Casts">Type Casts</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-char-data-type"><code>char</code> data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-character-constants">character constants</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Character-Constants">Character Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-comma-operator">comma operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-Comma-Operator">The Comma Operator</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-comparison-operators">comparison operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Comparison-Operators">Comparison Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-complex-conjugation">complex conjugation</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Complex-Conjugation">Complex Conjugation</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-complex-number-types">complex number types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Complex-Number-Types">Complex Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-compound-statements">compound statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Blocks">Blocks</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-conditional-expressions">conditional expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Conditional-Expressions">Conditional Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-conjugation">conjugation</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Complex-Conjugation">Complex Conjugation</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-const-type-qualifier"><code>const</code> type
qualifier</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Type-Qualifiers">Type Qualifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-constants">constants</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Constants">Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-constants_002c-character">constants, character</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Character-Constants">Character Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-constants_002c-floating-point">constants, floating
point</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Constants">Real Number Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-constants_002c-integer">constants, integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Constants">Integer Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-constants_002c-real-number">constants, real
number</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Constants">Real Number Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-continue-statement"><code>continue</code>
statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-continue-Statement">The continue Statement</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-D">D</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types">data types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Data-Types">Data Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-array">data types, array</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays">Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-complex-number">data types, complex
number</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Complex-Number-Types">Complex Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-enumeration">data types,
enumeration</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Enumerations">Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-floating-point">data types, floating
point</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-integer">data types, integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-pointer">data types, pointer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers">Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-primitive">data types, primitive</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Primitive-Types">Primitive Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-real-number">data types, real
number</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-structure">data types, structure</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Structures">Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-data-types_002c-union">data types, union</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Unions">Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declarations-inside-expressions">declarations inside
expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Statements-and-Declarations-in-Expressions">Statements and
Declarations in Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declarations_002c-function">declarations,
function</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Declarations">Function Declarations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-arrays">declaring arrays</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Arrays">Declaring Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-enumerations">declaring enumerations</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Enumerations">Declaring Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-pointers">declaring pointers</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Pointers">Declaring Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-string-arrays">declaring string arrays</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-as-Strings">Arrays as Strings</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-structure-variables">declaring structure
variables</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Structure-Variables">Declaring Structure
Variables</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-structure-variables-after-definition">declaring
structure variables after definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Structure-Variables-After-Definition">Declaring
Structure Variables After Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-structure-variables-at-definition">declaring
structure variables at definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Structure-Variables-at-Definition">Declaring Structure
Variables at Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-union-variables">declaring union
variables</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Union-Variables">Declaring Union Variables</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-union-variables-after-definition">declaring union
variables after definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Union-Variables-After-Definition">Declaring Union
Variables After Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-declaring-union-variables-at-definition">declaring union
variables at definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Union-Variables-at-Definition">Declaring Union
Variables at Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-decrement-operator">decrement operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incrementing-and-Decrementing">Incrementing and
Decrementing</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-defining-enumerations">defining enumerations</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Defining-Enumerations">Defining Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-defining-structures">defining structures</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Defining-Structures">Defining Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-defining-unions">defining unions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Defining-Unions">Defining Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-definitions_002c-function">definitions, function</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Definitions">Function Definitions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-division_002c-integer">division, integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Integer-Division">Signed Integer Division</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-do-statement"><code>do</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-do-Statement">The do Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-double-data-type"><code>double</code> data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-E">E</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-else-statements"><code>else</code> statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-if-Statement">The if Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-enumerations">enumerations</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Enumerations">Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-enumerations_002c-declaring">enumerations,
declaring</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Enumerations">Declaring Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-enumerations_002c-defining">enumerations,
defining</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Defining-Enumerations">Defining Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-enumerations_002c-incomplete">enumerations,
incomplete</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incomplete-Types">Incomplete Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-exit-status">exit status</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-main-Function">The main Function</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-EXIT_005fFAILURE"><code>EXIT_FAILURE</code></a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-main-Function">The main Function</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-EXIT_005fSUCCESS"><code>EXIT_SUCCESS</code></a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-main-Function">The main Function</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-expression-statements">expression statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Expression-Statements">Expression Statements</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-expressions">expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Expressions">Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-expressions-containing-statements">expressions containing
statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Statements-and-Declarations-in-Expressions">Statements and
Declarations in Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-expressions_002c-conditional">expressions,
conditional</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Conditional-Expressions">Conditional Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-extern-storage-class-specifier"><code>extern</code> storage
class specifier</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Storage-Class-Specifiers">Storage Class Specifiers</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-F">F</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-fields_002c-bit">fields, bit</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Bit-Fields">Bit Fields</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-float-data-type"><code>float</code> data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-floating-point-constants">floating point
constants</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Constants">Real Number Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-floating-point-types">floating point types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-for-statement"><code>for</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-for-Statement">The for Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function-calls_002c-as-expressions">function calls, as
expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Calls-as-Expressions">Function Calls as
Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function-declarations">function declarations</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Declarations">Function Declarations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function-definitions">function definitions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Definitions">Function Definitions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function-parameter-lists_002c-variable-length">function
parameter lists, variable length</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Variable-Length-Parameter-Lists">Variable Length Parameter
Lists</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function-parameters">function parameters</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Parameters">Function Parameters</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function-pointers_002c-calling-through">function pointers,
calling through</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Calling-Functions-Through-Function-Pointers">Calling Functions
Through Function Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-function_002c-main">function, main</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-main-Function">The main Function</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-functions">functions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Functions">Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-functions_002c-calling">functions, calling</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Calling-Functions">Calling Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-functions_002c-nested">functions, nested</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Nested-Functions">Nested Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-functions_002c-recursive">functions, recursive</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Recursive-Functions">Recursive Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-functions_002c-static">functions, static</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Static-Functions">Static Functions</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-G">G</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-goto-statement"><code>goto</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-goto-Statement">The goto Statement</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-H">H</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-hello-program">hello program</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#A-Sample-Program">A Sample Program</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-hello_002ec">hello.c</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#hello_002ec">hello.c</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-I">I</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-identifiers">identifiers</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Identifiers">Identifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-if-statements"><code>if</code> statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-if-Statement">The if Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-incomplete-types">incomplete types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incomplete-Types">Incomplete Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-increment-operator">increment operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incrementing-and-Decrementing">Incrementing and
Decrementing</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-indirect-member-access-operator">indirect member access
operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Member-Access-Expressions">Member Access Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-initializing-arrays">initializing arrays</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Arrays">Initializing Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-initializing-pointers">initializing pointers</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Pointers">Initializing Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-initializing-string-arrays">initializing string
arrays</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-as-Strings">Arrays as Strings</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-initializing-structure-members">initializing structure
members</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Structure-Members">Initializing Structure
Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-initializing-union-members">initializing union
members</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Union-Members">Initializing Union Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-int-data-type"><code>int</code> data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-integer-constants">integer constants</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Constants">Integer Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-integer-overflow">integer overflow</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Overflow-Basics">Integer Overflow Basics</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-integer-overflow-1">integer overflow</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Examples">Signed Overflow Examples</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-integer-overflow-2">integer overflow</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Advice">Signed Overflow Advice</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-integer-types">integer types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-K">K</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-keywords">keywords</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Keywords">Keywords</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-L">L</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-labeled-statements">labeled statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Labels">Labels</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-labels">labels</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Labels">Labels</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-lexical-elements">lexical elements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Lexical-Elements">Lexical Elements</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-logical-operators">logical operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Logical-Operators">Logical Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-logical-operators_002c-bitwise">logical operators,
bitwise</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Bitwise-Logical-Operators">Bitwise Logical Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-long-double-data-type"><code>long double</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-long-int-data-type"><code>long int</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-long-long-int-data-type"><code>long long int</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-loop-induction">loop induction</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Optimization-and-Wraparound">Optimization and Wraparound</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-M">M</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-macros_002c-statements-in-expressions">macros, statements
in expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Statements-and-Declarations-in-Expressions">Statements and
Declarations in Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-main-function">main function</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-main-Function">The main Function</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-member-access-expressions">member access
expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Member-Access-Expressions">Member Access Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-multidimensional-arrays">multidimensional arrays</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Multidimensional-Arrays">Multidimensional Arrays</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-N">N</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-nested-functions">nested functions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Nested-Functions">Nested Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-null-statement">null statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-Null-Statement">The Null Statement</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-O">O</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operator-precedence">operator precedence</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Operator-Precedence">Operator Precedence</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operator_002c-decrement">operator, decrement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incrementing-and-Decrementing">Incrementing and
Decrementing</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operator_002c-increment">operator, increment</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incrementing-and-Decrementing">Incrementing and
Decrementing</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operators">operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Expressions">Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operators-as-lexical-elements">operators as lexical
elements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Operators">Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operators_002c-arithmetic">operators, arithmetic</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arithmetic-Operators">Arithmetic Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operators_002c-assignment">operators, assignment</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Assignment-Operators">Assignment Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-operators_002c-comparison">operators, comparison</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Comparison-Operators">Comparison Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-overflow_002c-signed-integer">overflow, signed
integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Overflow-Basics">Integer Overflow Basics</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-overflow_002c-signed-integer-1">overflow, signed
integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Examples">Signed Overflow Examples</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-overflow_002c-signed-integer-2">overflow, signed
integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Advice">Signed Overflow Advice</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-P">P</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-parameters-lists_002c-variable-length">parameters lists,
variable length</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Variable-Length-Parameter-Lists">Variable Length Parameter
Lists</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-parameters_002c-function">parameters, function</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Function-Parameters">Function Parameters</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-pointer-operators">pointer operators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointer-Operators">Pointer Operators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-pointers">pointers</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers">Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-pointers-to-structures">pointers to structures</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers-to-Structures">Pointers to Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-pointers-to-unions">pointers to unions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers-to-Unions">Pointers to Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-pointers_002c-declaring">pointers, declaring</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Pointers">Declaring Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-pointers_002c-initializing">pointers,
initializing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Pointers">Initializing Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-precedence_002c-operator">precedence, operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Operator-Precedence">Operator Precedence</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-preface">preface</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Preface">Preface</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-primitive-data-types">primitive data types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Primitive-Types">Primitive Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-program-structure">program structure</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Program-Structure">Program Structure</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-Q">Q</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-qualifiers_002c-type">qualifiers, type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Type-Qualifiers">Type Qualifiers</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-R">R</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-real-number-constants">real number constants</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Constants">Real Number Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-real-number-types">real number types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-recursive-functions">recursive functions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Recursive-Functions">Recursive Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-register-storage-class-specifier"><code>register</code>
storage class specifier</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Storage-Class-Specifiers">Storage Class Specifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-renaming-types">renaming types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Renaming-Types">Renaming Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-return-statement"><code>return</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-return-Statement">The return Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-return-value-of-main">return value of
<code>main</code></a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-main-Function">The main Function</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-S">S</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-sample-program">sample program</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#A-Sample-Program">A Sample Program</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-scope">scope</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Scope">Scope</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-separators">separators</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Separators">Separators</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-sequence-point">sequence point</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Sequence-Points">Sequence Points</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-shifting">shifting</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Bit-Shifting">Bit Shifting</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-short-int-data-type"><code>short int</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-side-effect">side effect</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Side-Effects">Side Effects</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-side-effects_002c-macro-argument">side effects, macro
argument</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Statements-and-Declarations-in-Expressions">Statements and
Declarations in Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-signed-char-data-type"><code>signed char</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-signed-integer-overflow">signed integer overflow</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Overflow-Basics">Integer Overflow Basics</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-signed-integer-overflow-1">signed integer
overflow</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Examples">Signed Overflow Examples</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-signed-integer-overflow-2">signed integer
overflow</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Advice">Signed Overflow Advice</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-size-of-structures">size of structures</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Size-of-Structures">Size of Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-size-of-unions">size of unions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Size-of-Unions">Size of Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-sizeof-operator">sizeof operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-sizeof-Operator">The sizeof Operator</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-specifiers_002c-storage-class">specifiers, storage
class</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Storage-Class-Specifiers">Storage Class Specifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-statement_002c-null">statement, null</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-Null-Statement">The Null Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-statements">statements</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Statements">Statements</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-statements-inside-expressions">statements inside
expressions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Statements-and-Declarations-in-Expressions">Statements and
Declarations in Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-statements_002c-expression">statements,
expression</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Expression-Statements">Expression Statements</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-statements_002c-labeled">statements, labeled</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Labels">Labels</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-static-functions">static functions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Static-Functions">Static Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-static-linkage">static linkage</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Static-Functions">Static Functions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-static-storage-class-specifier"><code>static</code> storage
class specifier</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Storage-Class-Specifiers">Storage Class Specifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-storage-class-specifiers">storage class
specifiers</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Storage-Class-Specifiers">Storage Class Specifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-string-arrays_002c-declaring">string arrays,
declaring</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-as-Strings">Arrays as Strings</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-string-arrays_002c-initializing">string arrays,
initializing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-as-Strings">Arrays as Strings</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-string-constants">string constants</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#String-Constants">String Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-string-literals">string literals</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#String-Constants">String Constants</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-strings_002c-arrays-as">strings, arrays as</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-as-Strings">Arrays as Strings</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structure-members_002c-accessing">structure members,
accessing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Accessing-Structure-Members">Accessing Structure Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structure-members_002c-initializing">structure members,
initializing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Structure-Members">Initializing Structure
Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structure-variables_002c-declaring">structure variables,
declaring</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Structure-Variables">Declaring Structure
Variables</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structure-variables_002c-declaring-after-definition">structure
variables, declaring after definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Structure-Variables-After-Definition">Declaring
Structure Variables After Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structure-variables_002c-declaring-at-definition">structure
variables, declaring at definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Structure-Variables-at-Definition">Declaring Structure
Variables at Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structure_002c-program">structure, program</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Program-Structure">Program Structure</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structures">structures</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Structures">Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structures_002c-arrays-of">structures, arrays of</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-of-Structures">Arrays of Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structures_002c-defining">structures, defining</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Defining-Structures">Defining Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structures_002c-incomplete">structures,
incomplete</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incomplete-Types">Incomplete Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structures_002c-pointers-to">structures, pointers
to</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers-to-Structures">Pointers to Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-structures_002c-size-of">structures, size of</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Size-of-Structures">Size of Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-switch-statement"><code>switch</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-switch-Statement">The switch Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-system_002eh">system.h</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#system_002eh">system.h</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-T">T</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-ternary-operator">ternary operator</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Conditional-Expressions">Conditional Expressions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-type-casts">type casts</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Type-Casts">Type Casts</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-type-qualifiers">type qualifiers</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Type-Qualifiers">Type Qualifiers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-typedef-statement"><code>typedef</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-typedef-Statement">The typedef Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types">types</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Data-Types">Data Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-array">types, array</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays">Arrays</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-complex-number">types, complex number</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Complex-Number-Types">Complex Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-enumeration">types, enumeration</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Enumerations">Enumerations</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-floating-point">types, floating point</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-incomplete">types, incomplete</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incomplete-Types">Incomplete Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-integer">types, integer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-pointer">types, pointer</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers">Pointers</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-primitive">types, primitive</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Primitive-Types">Primitive Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-real-number">types, real number</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Real-Number-Types">Real Number Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-renaming">types, renaming</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Renaming-Types">Renaming Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-structure">types, structure</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Structures">Structures</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-types_002c-union">types, union</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Unions">Unions</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-U">U</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-union-members_002c-accessing">union members,
accessing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Accessing-Union-Members">Accessing Union Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-union-members_002c-initializing">union members,
initializing</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Initializing-Union-Members">Initializing Union Members</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-union-variables_002c-declaring">union variables,
declaring</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Union-Variables">Declaring Union Variables</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-union-variables_002c-declaring-after-definition">union
variables, declaring after definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Union-Variables-After-Definition">Declaring Union
Variables After Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-union-variables_002c-declaring-at-definition">union
variables, declaring at definition</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Declaring-Union-Variables-at-Definition">Declaring Union
Variables at Definition</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unions">unions</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Unions">Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unions_002c-arrays-of">unions, arrays of</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Arrays-of-Unions">Arrays of Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unions_002c-defining">unions, defining</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Defining-Unions">Defining Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unions_002c-incomplete">unions, incomplete</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Incomplete-Types">Incomplete Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unions_002c-pointers-to">unions, pointers to</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Pointers-to-Unions">Pointers to Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unions_002c-size-of">unions, size of</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Size-of-Unions">Size of Unions</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unsigned-char-data-type"><code>unsigned char</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unsigned-int-data-type"><code>unsigned int</code> data
type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unsigned-long-int-data-type"><code>unsigned long int</code>
data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unsigned-long-long-int-data-type"><code>unsigned long long int</code>
data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unsigned-short-int-data-type"><code>unsigned short int</code>
data type</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Types">Integer Types</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-unspecified-behaviour">unspecified behaviour</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Sequence-Points-Constrain-Expressions">Sequence Points Constrain
Expressions</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-V">V</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-variable-length-parameter-lists">variable length parameter
lists</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Variable-Length-Parameter-Lists">Variable Length Parameter
Lists</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-volatile-type-qualifier"><code>volatile</code> type
qualifier</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Type-Qualifiers">Type Qualifiers</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
<tr>
<td><span id="Index_cp_letter-W">W</span></td>
<td style="text-align: left;"></td>
<td></td>
<td style="text-align: left;"></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-while-statement"><code>while</code> statement</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#The-while-Statement">The while Statement</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-white-space">white space</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#White-Space">White Space</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-wraparound-arithmetic">wraparound arithmetic</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Integer-Overflow-Basics">Integer Overflow Basics</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-wraparound-arithmetic-1">wraparound arithmetic</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Examples">Signed Overflow Examples</a></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;" data-valign="top"><a
href="#index-wraparound-arithmetic-2">wraparound arithmetic</a>:</td>
<td> </td>
<td style="text-align: left;" data-valign="top"><a
href="#Signed-Overflow-Advice">Signed Overflow Advice</a></td>
</tr>
<tr>
<td colspan="4"><hr /></td>
</tr>
</tbody>
</table>

|  |  |
|----|----|
| Jump to:   | <a href="#Index_cp_letter-A"
class="summary-letter"><strong>A</strong></a>   <a href="#Index_cp_letter-B"
class="summary-letter"><strong>B</strong></a>   <a href="#Index_cp_letter-C"
class="summary-letter"><strong>C</strong></a>   <a href="#Index_cp_letter-D"
class="summary-letter"><strong>D</strong></a>   <a href="#Index_cp_letter-E"
class="summary-letter"><strong>E</strong></a>   <a href="#Index_cp_letter-F"
class="summary-letter"><strong>F</strong></a>   <a href="#Index_cp_letter-G"
class="summary-letter"><strong>G</strong></a>   <a href="#Index_cp_letter-H"
class="summary-letter"><strong>H</strong></a>   <a href="#Index_cp_letter-I"
class="summary-letter"><strong>I</strong></a>   <a href="#Index_cp_letter-K"
class="summary-letter"><strong>K</strong></a>   <a href="#Index_cp_letter-L"
class="summary-letter"><strong>L</strong></a>   <a href="#Index_cp_letter-M"
class="summary-letter"><strong>M</strong></a>   <a href="#Index_cp_letter-N"
class="summary-letter"><strong>N</strong></a>   <a href="#Index_cp_letter-O"
class="summary-letter"><strong>O</strong></a>   <a href="#Index_cp_letter-P"
class="summary-letter"><strong>P</strong></a>   <a href="#Index_cp_letter-Q"
class="summary-letter"><strong>Q</strong></a>   <a href="#Index_cp_letter-R"
class="summary-letter"><strong>R</strong></a>   <a href="#Index_cp_letter-S"
class="summary-letter"><strong>S</strong></a>   <a href="#Index_cp_letter-T"
class="summary-letter"><strong>T</strong></a>   <a href="#Index_cp_letter-U"
class="summary-letter"><strong>U</strong></a>   <a href="#Index_cp_letter-V"
class="summary-letter"><strong>V</strong></a>   <a href="#Index_cp_letter-W"
class="summary-letter"><strong>W</strong></a>   |

<div class="footnote">

------------------------------------------------------------------------

#### Footnotes

### <a href="#DOCF1" id="FOOT1">(1)</a>

C++ also has complex number support, but it is incompatible with the ISO
C99 types.

### <a href="#DOCF2" id="FOOT2">(2)</a>

a full declarator is a declaration of a function or an object which is
not part of another object

### <a href="#DOCF3" id="FOOT3">(3)</a>

However if for example `MAX` is `INT_MAX` and `x` is of type `int`, we
clearly have a problem with overflow. See [Overflow](#Overflow).

### <a href="#DOCF4" id="FOOT4">(4)</a>

Rarely, `argv[0]` can be a null pointer (in this case `argc` is 0) or
`argv[0][0]` can be the null character. In any case, `argv[argc]` is a
null pointer.

</div>

------------------------------------------------------------------------
