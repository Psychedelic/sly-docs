---
date: "1"
---
# SLY - Candid Utility

## SLY - Candid Utility


The SLY command line program tries to bundle a set of useful utility commands which can be used to **improve the developer experience** for anyone who wishes to create services on the top of the Internet Computer.

One area that we could improve was related to **dealing with the Candid files**. A candid file
is used to describe the interface of a canister, and a client can use this interface in order
to interact with the canister. 

Developers can create the candid files for their canister
either manually or automatically which is beside the subject of this chapter.


We understand that producing **helpful diagnostic messages** is crucial for a better developer
experience, and that the lack of such error messages can cause frustration when you're already
trying to solve complex problems. Since the official Candid parser by the DFINITY foundation was
not producing concise and clear error messages, we forked it to create a custom
version that **captures and prints the diagnostic messages in a more helpful fashion**. This new parser is used
throughout Sly whenever you're dealing with a candid file.

## Available Commands

The Candid related utility commands bundled in SLY, assume that you already have a candid file,
and it helps you perform some common tasks on the files. This is the brief list of operations
that we have (you can also run `sly candid -h` to see the list.)

1. [Check](#check)
3. [Format](#format)
4. [Gen](#gen)


## Check

`sly candid check <FILENAME>`

This command can be used to verify the correctness of a candid file. It prints the diagnostic
messages and exits with a non-zero exit code when an error is detected.

You can use this as part of your CI/CD pipeline if you manually maintain your candid files.

## Format

`sly candid format [FILES]...`

Pretty print a candid file, this command overwrites the original files, use with caution.

## Gen

`sly candid gen --js --ts --motoko --outdir ./bindings [FILES]...`

Used to generate binding files in different languages for the provided candid files, it writes
the generated files to the directory specified with `--outdir/-o`.
