# 🌱 Blockchain Commons bc-seedtool-cli

A tool for creating and transforming cryptographic seeds.

## Prerequisites

If any of the following prerequisites are not installed, the `configure` step below will fail.

* [`bc-crypto-base`](https://github.com/blockchaincommons/bc-crypto-base)
* [`bc-shamir`](https://github.com/blockchaincommons/bc-shamir)
* [`bc-slip39`](https://github.com/blockchaincommons/bc-slip39)
* [`bc-bip39`](https://github.com/blockchaincommons/bc-bip39)
* [`GNU argp`](https://www.gnu.org/software/libc/manual/html_node/Argp.html) This may be installed via `brew install argp-standalone`.

## Installation

```bash
$ ./configure
$ make check
$ sudo make install
```

## Use

```
$ seedtool
8935a8068526d84da555cdb741a3b8a8

$ seedtool --in hex --out bip39 8935a8068526d84da555cdb741a3b8a8
matrix pull accuse apart horn chat next rifle resemble artist until eye

$ seedtool --in bip39 matrix pull accuse apart horn chat next rifle resemble artist until eye
8935a8068526d84da555cdb741a3b8a8
```

```
$ seedtool --help
```

See [`MANUAL.md`](MANUAL.md) for detail, examples, and version history.

## Notes for Maintainers

Before accepting a PR that can affect build or unit tests, make sure the following sequence of commands succeeds:

```bash
$ ./configure
$ make distcheck
$ make distclean
```

## Origin, Authors, Copyright & Licenses

Unless otherwise noted (either in this [/README.md](./README.md) or in the file's header comments) the contents of this repository are Copyright © 2020 by Blockchain Commons, LLC, and are [licensed](./LICENSE) under the [spdx:BSD-2-Clause Plus Patent License](https://spdx.org/licenses/BSD-2-Clause-Patent.html).

In most cases, the authors, copyright, and license for each file reside in header comments in the source code. When it does not we have attempted to attribute it accurately in the table below.

This table below also establishes provenance (repository of origin, permalink, and commit id) for files included from repositories that are outside of this repository. Contributors to these files are listed in the commit history for each repository, first with changes found in the commit history of this repo, then in changes in the commit history of their repo of their origin.

| File      | From                                                         | Commit                                                       | Authors & Copyright (c)                                | License                                                     |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------ | ----------------------------------------------------------- |
| hkdf.c | [rustyrussell/ccan](https://github.com/rustyrussell/ccan/blob/master/ccan/crypto/hkdf_sha256/hkdf_sha256.c) | [d07f742](https://github.com/rustyrussell/ccan/commit/d07f742c5925b97ed558eb07aae285616f5df823) | 2016 [Rusty Russell](https://github.com/rustyrussell)<br/>2020 Wolf McNally | [MIT](https://github.com/rustyrussell/ccan/blob/master/ccan/crypto/hkdf_sha256/LICENSE)
| hkdf.h | [rustyrussell/ccan](https://github.com/rustyrussell/ccan/blob/master/ccan/crypto/hkdf_sha256/hkdf_sha256.h) | [d07f742](https://github.com/rustyrussell/ccan/commit/d07f742c5925b97ed558eb07aae285616f5df823) | 2016 [Rusty Russell](https://github.com/rustyrussell) | [MIT](https://github.com/rustyrussell/ccan/blob/master/ccan/crypto/hkdf_sha256/LICENSE)
| randombytes.c | [dsprenkels/randombytes](https://github.com/dsprenkels/randombytes/blob/master/randombytes.c) | [6db39aa](https://github.com/dsprenkels/randombytes/commit/6db39aaae6bb9ab97beca00d81bcfe935c56c88d) | 2017-2019 [Daan Sprenkels](https://github.com/dsprenkels/) | [MIT](https://github.com/dsprenkels/randombytes/commit/73ae9b4fce2e62babdd6a480b53ad449dd745ed9) |
| randombytes.h | [dsprenkels/randombytes](https://github.com/dsprenkels/randombytes/blob/master/randombytes.h) | [19fd002](https://github.com/dsprenkels/randombytes/commit/19fd002d9b7b001b333a671186a91231b60d821b) | 2017-2019 [Daan Sprenkels](https://github.com/dsprenkels/) | [MIT](https://github.com/dsprenkels/randombytes/commit/73ae9b4fce2e62babdd6a480b53ad449dd745ed9) |

### Dependencies

To build `seedtool` you'll need to use the following tools:

- autotools - Gnu Build System from Free Software Foundation ([intro](https://www.gnu.org/software/automake/manual/html_node/Autotools-Introduction.html)).

## Contributing

We encourage public contributions through issues and pull-requests! Please review [CONTRIBUTING.md](./CONTRIBUTING.md) for details on our development process. All contributions to this repository require a GPG signed [Contributor License Agreement](./CLA.md).

### Credits

The following people directly contributed to this repository. You can add your name here by getting involved — the first step is to learn how to contribute from our [CONTRIBUTING.md](./CONTRIBUTING.md) documentation.

| Name              | Role                | Github                                            | Email                                 | GPG Fingerprint                                    |
| ----------------- | ------------------- | ------------------------------------------------- | ------------------------------------- | -------------------------------------------------- |
| Christopher Allen | Principal Architect | [@ChristopherA](https://github.com/@ChristopherA) | \<ChristopherA@LifeWithAlacrity.com\> | FDFE 14A5 4ECB 30FC 5D22  74EF F8D3 6C91 3574 05ED |
| Wolf McNally      | Project Lead        | [@WolfMcNally](https://github.com/wolfmcnally)    | \<Wolf@WolfMcNally.com\>              | 9436 52EE 3844 1760 C3DC  3536 4B6C 2FCF 8947 80AE |

## Responsible Disclosure

We want to keep all our software safe for everyone. If you have discovered a security vulnerability, we appreciate your help in disclosing it to us in a responsible manner. We are unfortunately not able to offer bug bounties at this time.

We do ask that you offer us good faith and use best efforts not to leak information or harm any user, their data, or our developer community. Please give us a reasonable amount of time to fix the issue before you publish it. Do not defraud our users or us in the process of discovery. We promise not to bring legal action against researchers who point out a problem provided they do their best to follow the these guidelines.

## Reporting a Vulnerability

Please report suspected security vulnerabilities in private via email to ChristopherA@BlockchainCommons.com (do not use this email for support). Please do NOT create publicly viewable issues for suspected security vulnerabilities.

The following keys may be used to communicate sensitive information to developers:

| Name              | Fingerprint                                        |
| ----------------- | -------------------------------------------------- |
| Christopher Allen | FDFE 14A5 4ECB 30FC 5D22  74EF F8D3 6C91 3574 05ED |

You can import a key by running the following command with that individual’s fingerprint: `gpg --recv-keys "<fingerprint>"` Ensure that you put quotes around fingerprints that contain spaces.