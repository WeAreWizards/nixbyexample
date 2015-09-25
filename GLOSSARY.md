# attribute path

The Nix package database is a set of nested records, with the top-level record usually being `nixpkgs`.
Accessing attributes in nested records is done by chaining names with a dot, just like in many other languages (e.g. `nixpkgs.pythonPackages.django`).
This full "path" to a package is called the "attribute path".

# generation

Every time Nix modifies the system, e.g. by installing or removing a package, it creates a new generation. One can go back to a previous generation of the sytem with the command `nix-env --switch-generation $GENERATION`.
