The Nix language is *lazy*, *purely functional* with only a small
number of simple constructs and built-in functions.

*Lazy* means that the interpreter only evaluates expressions whose
value was requested by the user.

*Purely functional* means that there is no mutation of state and there
are no statements. Everything is an expression.

These properties make it possible to have a single expression with
tens of thousands of packages, and then to pick out one specific one
with its dependencies. Packages not needed to fulfil the installion
are never evaluated due to lazyness.
