# REPL

REPL stands for "read eval print loop". It's a convenient tool that
reads a nix-expression and prints the evaluated result.

Nix has such a REPL:

```
nix-env -iA nixpkgs.nix-repl
```

Test that it works by running `nix-repl` and entering the simple expression `1 + 1`:

```
$ nix-repl
Welcome to Nix version 1.10. Type :? for help.

nix-repl> 1 + 1
2
```
