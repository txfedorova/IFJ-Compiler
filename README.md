# IFJ / Formal Languages and Compilers

University team project implementing a compiler for the imperative language IFJ22 in C. The compiler processes source code from standard input and generates IFJcode22 target code.

The project was developed for the Brno University of Technology course **Formal Languages and Compilers (IFJ)**.

Official course page: https://www.fit.vut.cz/study/course/IFJ/

## Project overview

The implementation contains the main stages of a compiler pipeline:

- lexical analysis using a finite-state scanner;
- tokenization of identifiers, keywords, literals and operators;
- syntax analysis and expression parsing;
- symbol-table handling;
- semantic checks;
- target-code generation for IFJcode22;
- error handling and debugging support.

The source code is organized into separate modules for scanning, parsing, expression processing, symbol tables and code generation.

## Main source files

```text
src/
├── main.c
├── scanner.c / scanner.h
├── parser.c / parser.h
├── expression.c / expression.h
├── symtable.c / symtable.h
├── codegen.c / codegen.h
├── string_t.c / string_t.h
└── debug.c / debug.h
```

Additional project documentation is available in [`doc/dokumentace.pdf`](doc/dokumentace.pdf).

## Build and run

The project uses GCC and a Makefile.

Build the compiler with:

```bash
make
```

Run it with source code on standard input:

```bash
./ifj22 < input.php
```

To save the generated IFJcode22 output:

```bash
./ifj22 < input.php > output.ifjcode22
```

Clean generated build files with:

```bash
make clean
```

## Repository structure

```text
.
├── README.md
├── Makefile
├── src/
├── doc/
│   └── dokumentace.pdf
├── scripts/
├── misc/
├── ifj22-tester/
├── input.php
└── code.ifjc22
```

## Notes

This was a four-person university team project for IFJ 2022/23. The original source code, documentation and coursework files are preserved; this README was updated later to make the repository easier to understand from GitHub.
