DCPU16-Lisp
===========

A lisp compiler for the DCPU16 processor

Usage:
------

From bee-lisp

    < program.bl  compile.py 
        | assemble.py > program.obj


From other language
  
    < program.ext tokenize.py --ext 
        | astify.py --ext
        | compile.py 
        | assemble.py > program.obj

Tools:
------

###tokenize.py
**[future]** Takes a program in an other language and tokenises it (token stream is long list of s-exprs) 

###astify.py
**[future]** Turns a token stream into a valid bee-lisp program.

###compile.py
Compiles valid bee-lisp program into DCPU16 assembly from stdin to stdout

###assemble.py
Assembles a valid DCPU (.dasm or .dasm16) program into binary from stdin to stdout 

Bee-Lisp:
---------

    (defun my-add \[x y]
       (+ x y))
