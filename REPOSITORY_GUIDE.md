<!-- SPDX-License-Identifier: GPL-3.0-only -->
# Type A repository guide

Copyright (C) 2026 RUSSELL PHILIP SMITHSON

This repository contains **LCUF Type A**, corpus version **0.1.0**. The complete
versioned release is preserved under [LCUF_RESEARCH_CORPUS_0.1.0/](LCUF_RESEARCH_CORPUS_0.1.0/).
Its sources and sealed manifests remain byte-exact copies of the delivered release.

The shared [README](README.md) and [full description](FULL_DESCRIPTION.md)
describe both Type A and Type B. This repository supplies the Type A edition.
Type B is the separately published 0.2.0 edition with research-applied language
profiles and expanded architecture contracts. Start with the
[Type A corpus index](LCUF_RESEARCH_CORPUS_0.1.0/README.md) for version-specific navigation.

## Run the preserved release

Run these commands from the repository root, using a compatible local Python:

```text
cd LCUF_RESEARCH_CORPUS_0.1.0
python -B tools/verify_release.py --deep
python -B runtime/lcuf.py check runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py compile runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py simulate runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py plan runtime/examples/federated_sum.lcuf
```

These commands evaluate the local host model. The generated plan records null
bootable images. Native boot and authenticated network federation remain design
contracts with separate acceptance requirements. See the versioned
[reproducibility guide](LCUF_RESEARCH_CORPUS_0.1.0/REPRODUCIBILITY.md) for dependency
compatibility, tests, numerical comparisons and evidence interpretation.

## Copyright and license scope

Copyright (C) 2026 RUSSELL PHILIP SMITHSON.

The publication documents identified in [COPYRIGHT](COPYRIGHT), and this repository
guide, use **GNU GPL version 3 only**, SPDX identifier `GPL-3.0-only`.
See [LICENSE](LICENSE), [NOTICE](NOTICE) and [LICENSING.md](LICENSING.md).
The grant applies to those publication documents. Corpus sources, supplied
research, frozen reference materials, figures and bundled dependencies retain
their existing notices and terms. Their preserved inclusion does not assign
their copyright to the publication author or designate unlicensed material GPL.

The copies of the shared publication files are unchanged. Their original archive
mapping and package receipts describe the packaged releases. This repository
stores the complete extracted Type A release at the versioned path above.
