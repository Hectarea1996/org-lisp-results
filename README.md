# org-lisp-results

The purpose of this file is to print better results of Common Lisp code from org-mode source code blocks. This file only redefines the function `org-babel-execute-src-block`.

## Installation

You can place the file wherever you want and `require` it.

Also, you can just copy the function definition and paste it into your `.emacs` or `.emacs.d/init.el` file.

In both cases make sure that this definition runs after org-mode is `require`d.

## Example

* Before:

```org
#+begin_src lisp
(values 3 (princ "CASA") 5)
#+end_src

#+RESULTS:
: 3
```

* After:

```org
#+begin_src lisp
(values 3 (princ "CASA") 5)
#+end_src

#+RESULTS:
: CASA
: 3
: "CASA"
: 5
```
