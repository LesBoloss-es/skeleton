# skeleton

Generate skeletons of projects from templates.

```
$ skeleton list
Available langs:
  - lang latex [+beamer]
  - lang ocaml [+mystdlib +ppx]

$ skeleton init ocaml foo
$ tree foo
foo
├── Makefile
├── foo.opam
├── src
│   ├── dune
│   ├── lib.ml
│   └── main.ml
└── tests
    ├── dune
    └── runtest.ml
```
