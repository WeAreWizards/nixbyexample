# Ubuntu

We chose Ubuntu trusty (14.04) for our example, but newer and older
versions would work just the same.

First some required dependencies:

```bash
sudo apt-get install libdbd-sqlite3-perl libdbi-perl libwww-curl-perl
```

We use the *incredibly dangerous and generally discouraged* way of
piping a random shell script from the Internet into bash. Using a
package manager implies trusting the people who package the code so in
this specific case it's OK to trust the first step as well.

```bash
bash <(curl https://nixos.org/nix/install)
```

You will see some output showing what's being downloaded, and then at
the end this message:

```
Installation finished!  To ensure that the necessary environment
variables are set, either log in again, or type

  . /home/ubuntu/.nix-profile/etc/profile.d/nix.sh

in your shell.
```

Now run:

```
. /home/ubuntu/.nix-profile/etc/profile.d/nix.sh
```

And check that you have the `nix-env` command:

```
$ nix-env --version
nix-env (Nix) 1.10
```
