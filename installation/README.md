# Installation

Nix supports Linux and OSX, but should also work on others like FreeBSD. Windows is not currently supported.


> **Note** <br>Nix installs itself in your root directory under `/nix` and can grow quite large. A fresh installation with a few packages is ~500MiB, but a long-running system with lots of packages can grow to 15-20 GiB.

The current recommended way to install Nix on all platforms is to run the following command into a terminal as your normal user (*not* root):

```bash
curl https://nixos.org/nix/install | sh
```

While this is *incredibly dangerous and generally discouraged*, using a package manager implies trusting the people who package the code so in this specific case it's OK to trust the first step as well.

You will see some output showing what's being downloaded, and then at the end this message:

```
Installation finished!  To ensure that the necessary environment
variables are set, either log in again, or type

  . /home/ubuntu/.nix-profile/etc/profile.d/nix.sh

in your shell.
```

Now run the command given by the output of the installation script, in
our case:

```bash
. /home/ubuntu/.nix-profile/etc/profile.d/nix.sh
```

And check that you have the `nix-env` command:

```
$ nix-env --version
nix-env (Nix) 1.11.2
```
