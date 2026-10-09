<!-- SPDX-License-Identifier: GPL-3.0-only -->
# Type A repository guide

Copyright (C) 2026 RUSSELL PHILIP SMITHSON

This repository publishes **LCUF Type A**, corpus version **0.1.0**. The complete
byte-exact release is supplied as [LCUF_RESEARCH_CORPUS_A.zip](LCUF_RESEARCH_CORPUS_A.zip).
It contains **605 files** under the internal directory
`LCUF_RESEARCH_CORPUS_0.1.0/`. The repository also supplies all **12 shared
publication files**, including their supporting `licenses/` and `validation/`
directories. The [README](README.md) and [full description](FULL_DESCRIPTION.md)
describe Type A and Type B; this repository contains the Type A corpus archive.

## Download, extract and verify

Clone the repository, or download its files, and open PowerShell in the repository
directory. Extract into a directory where `LCUF_RESEARCH_CORPUS_0.1.0/` does not
already exist:

```powershell
Expand-Archive -LiteralPath './LCUF_RESEARCH_CORPUS_A.zip' -DestinationPath '.'
Set-Location './LCUF_RESEARCH_CORPUS_0.1.0'
python -B tools/verify_release.py --deep
```

The extraction creates the versioned corpus directory. The verifier checks its
sealed manifest, hashes and data/Python syntax. It does not authenticate the
author. The archive's current filename, SHA-256, byte count and checked member
population are recorded separately in [ARCHIVE_INTEGRITY.json](ARCHIVE_INTEGRITY.json).
The older sealed package receipt retains its original versioned archive basename;
this new integrity receipt describes the A archive currently published here.

Archive SHA-256:

```text
41b8c831af8a62ce399f1054d4eb0739d21e4d45fa950ae2b470e6c900668959
```

Archive size: **12,287,343 bytes**. The archive's CRC check passed, and every
member was compared by SHA-256 with the preserved 0.1.0 release before publication.

## Run Type A

From the extracted `LCUF_RESEARCH_CORPUS_0.1.0` directory:

```text
python -B runtime/lcuf.py check runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py compile runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py simulate runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py plan runtime/examples/federated_sum.lcuf
```

The example computes and copies 42 across declared model sites in one host process.
The plan contains null bootable images. Native boot and authenticated network
federation remain design contracts with separate acceptance requirements.
Read the extracted corpus `README.md` and `REPRODUCIBILITY.md` for navigation,
dependency compatibility, validation commands and evidence interpretation.

## Copyright and license scope

Copyright (C) 2026 RUSSELL PHILIP SMITHSON.

The publication documents identified in [COPYRIGHT](COPYRIGHT), and this repository
guide, use **GNU GPL version 3 only**, SPDX identifier `GPL-3.0-only`.
See [LICENSE](LICENSE), [NOTICE](NOTICE) and [LICENSING.md](LICENSING.md).
The grant applies to those publication documents. The preserved corpus sources,
supplied research, frozen references, figures and bundled dependencies retain
their existing notices and terms. Inclusion does not transfer their copyright or
designate material without an express license GPL.
