[![img](https://img.shields.io/badge/Lifecycle-Experimental-339999)](https://github.com/bcgov/repomountie/blob/master/doc/lifecycle-badges.md)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

# DTS Verifiable Credential Issuer Service

Digital Trust Verifiable Credential Issuer Service

## Repository Structure

- `api`: contains the .Net Core back-end code that defines the business logic for the DTS VC issuer.

- `frontend`: a VueJS frontend that provides users with a user interface to request Verifiable Credentials.

- `docker`: configurations and script to run the services in Docker on localhost.

- `ngrok`: configurations tp open an ngrok tunnel to some of the services, required in order to expose the agent instance to the internet.

## Pre-Requisites

Please ensure the following pre-requisites are met before attempting to run the project:

- Docker

- ngrok

- jq

## Getting Started

Please refer to the readme in the [docker](./docker/README.md) folder.
