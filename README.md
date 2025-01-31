# EnfPal: a proactive real-time first-order enforcer

## Getting Started

To execute the project on your local machine, follow the instructions below.

### Prerequisites

We recommend that you install a recent verion of the OCaml compiler (>= 4.11) and necessary dependencies with [opam](https://opam.ocaml.org/doc/Install.html).

In particular, if you are a Debian/Ubuntu user

```
# apt-get install opam libgmp-dev
```

and then

```
$ opam init -y
$ opam switch create 4.13.1
$ eval $(opam env --switch=4.13.1)
$ opam install dune core_kernel base zarith menhir js_of_ocaml js_of_ocaml-ppx \
               zarith_stubs_js dune-build-info qcheck pyml calendar
```

should be enough.

### Running

From the root folder, you can compile the code with

```
$ dune build
```

to obtain the executable **enfpal.exe** inside the folder [bin](bin/). Moreover, you can run one of our predefined examples with

```
$ ./bin/enfpal.exe -sig examples/case_study/arfelt_et_al_2019.sig -formula examples/case_study/formulae_whyenf/limitation.mfotl -log examples/case_study/arfelt_et_al_2019.log
```

You can remove the binary and clean the working directory with

```
$ dune clean
```

## License

This project is licensed under the GNU Lesser GPL-3.0 license - see [LICENSE](LICENSE) for details.
