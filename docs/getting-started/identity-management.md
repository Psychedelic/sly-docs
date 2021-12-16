---
date: "1"
---
# SLY - Identity Management

## SLY - Identity Management

As a command line program which is developed for easier interaction with the Internet Computer,
it is only trivial to have a set of commands which can help user to manage their different
identities. In SLY the `sly identity *` commands are there to give you control over all the identities
you have.

You can see the full list of commands by running `sly identity -h`. Here we go through
some topics you'll need to know.

1. [Creating Identities](#create)
2. [Importing Identities](#import)
3. [Using identities](#switching-identity)

##  Create

```
sly identity create <NAME>
```

By default, SLY creates a new identity for you the first time a command is executed, this 
identity is named `default`.

You can also create additional new identities by using this command. Even though we support
using `Ed25519`, Sly uses the `secp256k1` curve when creating new identities.

The newly created identity is not the default, you should remember to switch your identity.

## Import

```
sly identity import <NAME> <PEM>
```

Imports a new identity from a PEM file under the given name. You should bear in mind that
the newly imported identity is not set to be the default, and that you should switch your
identity.

## Switching identity

```
sly identity use <NAME>
```

Use this command if you want to change your default identity, you can verify the identity
you are using by either running one of the following commands:

1. `sly identity whoami` To view the name of the identity (Which you assigned).
2. `sly identity get-principal` To view the principal id of the current identity.

You can also use the top level option `--identity <IDENTITY>` to overwrite the default
identity and switch the identity in that command execution.
