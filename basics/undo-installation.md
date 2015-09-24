# Undo installation

Nix supports atomic *rollback* of your packages to a previous state. *Rollback* is the same as undoing your last action (or actions).

We can inspect changes to our packages with `--list-generations`:

```console
$ nix-env --list-generations
 1     2015-09-21 23:05:34
 2     2015-09-22 17:10:56
 3     2015-09-24 10:49:51   (current)
```

Let's undo our last change (e.g. the installation of `hello`):

```console
$ nix-env --rollback
switching from generation 3 to 2
```

Checking with `--list-generations` we can see that we're now the previous install (2). Note that generation 3 is still around.

```console
$ nix-env --list-generations
 1     2015-09-21 23:05:34
 2     2015-09-22 17:10:56   (current)
 3     2015-09-24 10:49:51
```

With generation 3 still around We can switch back to it like so:

```console
$ nix-env --switch-generation 3
```

With `--switch-generation` we can in fact switch to any generation, e.g. your install fro 4 weeks ago.
