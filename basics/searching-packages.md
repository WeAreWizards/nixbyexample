# Searching packages

The simplest way to find a package is to use the web frontend on the
NixOS website: https://nixos.org/nixos/packages.html

On the command line packages can be searched with `nix-env`:

```bash
nix-env -qaP | grep hello
```

The flags `-qaP` stand for `--query --available --attr-path`, telling
`nix-env` to query all available packages, and to print their
attribute path.

`nix-env` doesn't have filtering built in so we use the standard grep
utility to filter the results to what we are looking for.
