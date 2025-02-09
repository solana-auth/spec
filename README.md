# Solana Auth Specification

Welcome to the Solana Auth Specification repository. This document serves as the base working document to sketch out
what we want to build before starting development.

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [TODO](#todo)
4. [Contributing](#contributing)

## Introduction

Solana Auth aims to provide a robust, open-source authentication solution with first-party support for Solana. This
specification outlines the core features for the first iteration of the Solana Auth library.

The goal is to provide an easy-to-use, secure, and flexible package that can be integrated into any application or
service that requires users to authenticate with their Solana wallets.

At this point in time we will focus on formalizing existing best practices and standards instead of creating a new
authentication protocol from scratch.

## Features

### 1. Sign in with Solana

Authenticate users using [SIWS](https://github.com/phantom/sign-in-with-solana), currently supported
by the browser extensions [Backpack](https://backpack.app)
and [Phantom](https://phantom.com/).

**Example Use Case:** A web application that requires users to authenticate using their Solana wallets.

### 2. Sign in by Signing a Message

Authenticate users by signing a message using their Solana wallet. This method is suitable for browser extensions that
don't support SIWS (like [Solflare](https://solflare.com/) and others). It is also suitable for command-line
applications and scripts, APIs or AI agents that require a secure way to verify
their identity.

**Example Use Case:** A command-line tool that needs to authenticate users securely.

### 3. Sign in by Signing a Transaction

Authenticate users by signing a transaction using their Solana wallet. This method is suitable for browser extensions in
combination with a Ledger wallet. In this flow, the transaction is signed but not sent to the network.

**Example Use Case:** A web application that uses Ledger wallets for secure transactions.

### 4. Sign in by Signing an Offchain Message

Authenticate users by [signing an offchain message](https://docs.anza.xyz/cli/examples/sign-offchain-message) using the
Solana cli.

**Example Use Case:** A script that needs to authenticate users offchain, without relying on a browser extension.

## TODO

This list is not exhaustive and is subject to change.

- [ ] Create specification.
    - [x] Setup repository and basic document structure.
    - [x] Specify features.
    - [ ] Specify api for the library based on the features.
- [ ] Create prototype to verify the specification.
    - [ ] Quick and dirty prototype of the library.
    - [ ] Example application that consumes the library.
- [ ] Spec out initial implementation.
    - [ ] Create detailed specification for the library, test, docs and examples.
    - [ ] Implement the library according to the specification.
    - [ ] Create the demo applications.
    - [ ] Write documentation.

## Contributing

### How to Contribute

- Get in tough with us on [Telegram](https://t.me/solana_auth) or [X](https://x.com/SolanaAuth) to discuss your ideas.
- Use pull requests (PRs) to propose changes to this spec.

---

This document is a work in progress. Please feel free to open pull requests (PRs) to propose changes and improvements.
