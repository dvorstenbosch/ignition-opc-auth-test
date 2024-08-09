# Ignition test project for OPC authorization

Ignition project to test authorization on OPC access for tag providers in Ignition.

This repository contains a demo project to test the authentication of the OPC server to different tag providers. There are two TagProviders: `ProviderA` and `ProviderB` and three OPC users `UserA`, `UserB` and `admin`. User A has only read permissions for Provider A (`Authenticated/Roles/ReadA`) and User B has only read permissions for Provider B (`Authenticated/Roles/ReadB`). User admin has access to both providers. 

In the current situation, when trying to browse the different tag providers via OPC, it is only possible to find tags if a user has permissions to access all the tag providers.


## How to run this project

Run `docker compose up` in the root of this project to start up the demo. It will automatically restore the gateway backup and become accessible on port `8088`. Credentials for the different users can be found below.

The actual gateway backup can be found in the `gw-backup` directory of this repository.


## Users

- username: **admin** / password: **password**
- username: **UserA** / password: **password**
- username: **UserB** / password: **password**
