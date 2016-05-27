# REPL

Like many languages Nix has a REPL, where REPL stands for "read eval
print loop". The REPL is convenient tool that reads a nix-expression
and prints the evaluated result.

You can install it:

```
nix-env -iA nixpkgs.nix-repl
```

Now test that it works by running `nix-repl` and entering the simple
expression `1 + 1`:

```
$ nix-repl
Welcome to Nix version 1.10. Type :? for help.

nix-repl> 1 + 1
2
```
