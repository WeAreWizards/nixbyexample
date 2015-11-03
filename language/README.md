The Nix language is lazy and pure functional with only a small number
of simple constructs and builtin functions.

The lazy part means that the interpreter only evaluates results the
user requested. This allows packaging 100,000 packages in a single
expression but only evaluating a single package for installation. The
other packages are still there but not evaluated.

The purely functional part means that there is no mutation and there
are no statements. Every construct is an expression (a function).
