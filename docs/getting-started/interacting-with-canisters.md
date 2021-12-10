---
date: "1"
---
# SLY - Interacting with Canisters

## SLY - Interacting with Canisters

Using SLY, you can make **update or query calls to canisters**, this calls can be directed to the
local or main net by providing the top level `--network=ic/local` option, you can also provide
any arbitrary http url for the `--network` option. By default, the local network is used.

> Note: The commands described here are subject to change in near future.

## Update calls

`sly --network=ic call --candid <CANDID> update <CANISTER-ID> <METHOD-NAME> [ARGUMENT]`

Use this structure to make an update call to a canister. Use `sly call -h` for more help.

## Query calls

`sly --network=ic call --candid <CANDID> query <CANISTER-ID> <METHOD-NAME> [ARGUMENT]`

Use a command like this to make query calls.