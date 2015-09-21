# Installing a package

The command for managing installed packages is `nix-env`. We're going
to install a program called `hello` which commonly used as the
simplest example for packaging and exists in many distributions. It's
only function is to print "Hello, world!".

```
$ nix-env -i hello --no-build-output
installing ‘hello-2.10’
building path(s) ‘/nix/store/rck77h9jvv1r9c80csk34icdjqg1iskd-user-environment’
```

> **Note** <br> We add `--no-build-output` because the output of
> nix-env is quite verbose and drowns out the important details.

The newly installed package is in our `PATH` and we can just run it:

```
$ hello
Hello, world!
```
