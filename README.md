<!-- SPDX-License-Identifier: GPL-3.0-only -->
# LCUF Type A and Type B Research Corpus

Copyright (C) 2026 RUSSELL PHILIP SMITHSON

LCUF is the Columned Unikernel and Hyperfederated Fabric Language research corpus. It brings together explicit column-based source, a preserved JA mathematical foundation, reproducible host implementations, formal language specifications, systems architecture and evidence governance. **Type A is corpus version 0.1.0. Type B is corpus version 0.2.0.** These type names identify the two corpus editions; they are not source-language type constructors.

Type A establishes the formal and mathematical baseline. Type B preserves that baseline and applies twenty additional research articles to a separately identified language extension and architecture. Both editions provide executable host research. Native unikernel images, authenticated network federation and physical implementations remain development contracts with their own acceptance requirements.

These publication documents use **GNU GPL version 3 only**, identified as `GPL-3.0-only`. See [LICENSE](LICENSE), [NOTICE](NOTICE), [COPYRIGHT](COPYRIGHT) and [licensing scope](LICENSING.md). Existing corpus sources, supplied articles and dependencies retain their individual notices and rights.

## Full project description

The [full description](FULL_DESCRIPTION.md) explains the language model, mathematical foundation, two editions, applied research domains, evidence and architecture. This README supplies practical entry points, commands and release information.

LCUF source makes the intended site, operation, type, authority and dependency visible in each row. Admission checks establish whether a finite program conforms to the declared contract before the host executes it. The resulting normalized intermediate representation and local receipt chain bind admitted policy to an observed run. The architecture extends this pattern toward native execution and nested federations through explicit ABI, ownership, transport, durability and resource obligations.

## Type A and Type B

| Property | Type A | Type B |
|---|---|---|
| Corpus version | 0.1.0 | 0.2.0 |
| Implemented source header | `LCUF/0.1` | `LCUF-X/0.2` |
| Primary technical volumes | 18 | 23 total, including the preserved baseline |
| Curated documentation | 41,309 whitespace-separated words | 60,775 whitespace-separated words |
| Closed host operation set | 6 core operations | 21 total operations |
| Principal role | Formal core, JA foundation, systems and assurance baseline | Article-applied profiles and expanded architecture |
| New article analysis | Original corpus audit and source-to-profile mappings | 20 article reviews, 147 claim dispositions and 82 architecture requirements |
| Extension requirements | Formal core has 48 stable requirement IDs | Adds 24 separately identified extension requirements |
| Relationship | Standalone foundational release | Contains Type A byte-exact under `baseline/0.1.0/` |

Type B is an explicit extension with its own source header and reference implementation. Programs do not silently acquire new mathematical meanings or operations when an edition changes. Use the compiler corresponding to the source header.

## Mathematical foundation

Both editions preserve the **8S Penteract–S³ Master Coupled Mechanics Law**, its five base coordinates indexed **4 through 8**, and the coupled acceptance gate:

```text
eta_ind >= epsilon_ind AND Delta8S > epsilon_gain
```

The corpus distinguishes author-defined coupling, finite real matrix geometry, local S³ relationships and research admission policy. Interpretations of `Classify` and `Score` remain unresolved where the supplied authority does not determine them. Explicit engineering tolerances are recorded separately from the author's arithmetic.

Type B introduces finite p-adic addressing and quotient arithmetic as additional domains. They do not replace the real metric, reinterpret optimizer denominators as p-adic reciprocals, or identify storage axes with the five JA coordinates.

## Implemented language

Both host languages use the following twelve columns:

```text
id | site | profile | op | inputs | output | type | effects | caps | after | budget | evidence
```

The declarations and exact cell grammar belong to the versioned specification. Rows describe a dependency graph with explicit outputs, ownership, capabilities, effects, ordering and model budgets. The references check single writers, defined inputs, compatible types, declared authority, acyclic dependencies and finite resource measures before evaluating admitted programs. Ready rows follow deterministic lexical ordering.

Type A implements `const`, `add`, `mul`, `copy`, `assert_eq` and `emit`. Its value types are `i64`, `bool` and `text`; `unit` describes terminal results. It supplies signed integer bounds, authorized copies between declared model sites, canonical identities and local execution receipts.

Type B retains those operations and adds fifteen profile operations for finite residue arithmetic, explicit conversion and reduction, capped valuation, finite coset averaging, HRR convolution and correlation, cyclic permutation, bounded periodic diffusion, raster shifts, scaled-sign packing, wire extraction, residual extraction and sign decoding. Its additional constructors include `Zp[p,n]`, `Vec[f64,N]`, `PField[p,n]`, `Raster[u8,W,H,C]`, `Residual[N]`, `SignPacket[N]` and `EFBundle[N]`.

`PField` stores real samples at finite residue addresses. HRR correlation supports approximate recovery rather than a universal inverse. Raster operations act on decoded unsigned 8-bit arrays. Compression residuals and compound local state stay at their owning site; a separately typed wire packet can follow an explicitly authorized model copy.

## Download and extraction

The current distribution filenames map to the internal versioned directories as follows:

| Archive filename | Extracted corpus directory |
|---|---|
| `LCUF_RESEARCH_CORPUS_A.zip` | `LCUF_RESEARCH_CORPUS_0.1.0/` |
| `LCUF_RESEARCH_CORPUS_B.zip` | `LCUF_RESEARCH_CORPUS_0.2.0/` |

Older sibling package receipts retain the original versioned ZIP basenames. The new documentation package records the current A and B filename mapping and archive digests without rewriting those sealed receipts.

Extract an edition into its own directory and run the commands below from that corpus directory. This publication package contains the description, README and licensing files; obtain the corpus archives separately for their implementations, datasets and original evidence.

## Run Type A

From the extracted `LCUF_RESEARCH_CORPUS_0.1.0` directory:

```text
python -B tools/verify_release.py --deep
python -B runtime/lcuf.py check runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py compile runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py simulate runtime/examples/federated_sum.lcuf
python -B runtime/lcuf.py plan runtime/examples/federated_sum.lcuf
```

The example computes and copies 42 across declared model sites in one host process. Its plan contains null bootable images. The retained payload and reserved steps are model quantities rather than measurements of total Python memory, native memory, time or network consumption.

## Run Type B

From the extracted `LCUF_RESEARCH_CORPUS_0.2.0` directory:

```text
python -B tools/verify_release.py --deep
python -B extensions/lcuf_x.py check examples/accept_residue_add.lcufx
python -B extensions/lcuf_x.py run examples/accept_coset_prefix.lcufx
python -B extensions/lcuf_x.py run examples/accept_hrr_noninverse.lcufx
python -B extensions/lcuf_x.py run examples/accept_remote_wire.lcufx
```

The examples demonstrate exact modular arithmetic, real-valued low-digit averaging, approximate HRR unbinding and authorized wire-packet movement in the local model. The remote-wire example does not contact a network. Examples prefixed `reject_` are intentional admission failures.

The extension bounds vectors at 256 elements, decoded rasters at 4,096 samples, source at 1 MiB and programs at 1,024 rows. Admission includes modeled kernel scratch and retained output payload. These bounds describe the published host model rather than native allocator enforcement.

## Dependencies and reproducibility

The recorded environment is CPython 3.12.14 on Windows AMD64. The reference compilers, kernels and case builders use the Python standard library. Full record-schema validation requires `jsonschema`; an offline dependency tree is bundled with Type A and preserved inside Type B. Its native component targets CPython 3.12 Windows AMD64. Other platforms need compatible dependencies from the edition's pinned requirement files.

Fresh numerical cross-checks use optional NumPy 2.3.5. The edition-specific `REPRODUCIBILITY.md` documents exact installation boundaries, seeds, tolerances, regeneration and report-writing behavior. Preserve an untouched extraction before regenerating artifacts, because changed source or serialization can change recorded identities.

Type A core validation and tests:

```text
python -B tools/validate_core.py
python -B -m unittest discover -s runtime/tests -v
python -B -m unittest discover -s tools/tests -v
```

Type B extension validation and tests:

```text
python -B tools/validate_extensions.py
python -B -m unittest discover -s extensions -p test_extensions.py -v
python -B -m unittest discover -s tools -p test_validation.py -v
python -B tools/numerical_crosschecks.py
```

The last command requires the optional numerical dependency. Schema replay, numerical comparison and integrity verification are distinct checks with distinct receipts.

## Recorded evidence

| Evidence collection | Type A | Type B additions |
|---|---:|---:|
| Core conformance records | 10,144 | Baseline preserved |
| Mathematical operation and input cases | 1,619 | Baseline preserved |
| Numerical comparisons | 500 | 208 new comparisons |
| Unit tests | 92 | 60 new tests |
| Extension conformance | Not applicable | 352 records and 400 source evaluation slots |
| Extension construction families | Not applicable | 55 |
| Deliberate extension fault experiments | Not applicable | 5 specified faults detected |

Type B's extension population contains 272 accepted programs, 32 representative rejection mechanisms and 48 metamorphic pairs. Parameterized sources share construction templates. Counts describe published populations and recorded checks; they do not establish blind evaluation, statistical independence or machine-learning generalization.

The recorded Type B package checks include deterministic reconstruction of 58 extension artifacts, byte-exact preservation of 605 baseline files, independent implementation and validator reviews, and successful host replay from a fresh ZIP extraction. Package manifests support integrity comparison against a trusted copy. They are unsigned and do not authenticate authors or attest physical execution.

## Corpus navigation

Type A's principal directories are `specification/`, `research/`, `mathematics/`, `runtime/`, `datasets/`, `examples/`, `schemas/`, `tools/`, `validation/` and `provenance/`. Start with its research charter, formal specification index, mathematics volume and reproducibility guide.

Type B adds `design/`, `extensions/` and `research_sources/`, plus new datasets, examples, schemas and receipts. The five applied design volumes cover language admission; p-adic geometry and 8S; signal, image and holographic profiles; optimizer, unikernel and telemetry contracts; and integrated architecture and migration. `design/ARTICLE_APPLICATION_MATRIX.md` maps every supplied article to its implemented host subset and remaining architecture obligation. `design/ARCHITECTURE_PLAN.json` records current implementation states.

Each edition has `CORPUS_METADATA.json`, `CORPUS_CATALOG.json`, `RELEASE_MANIFEST.json` and `validation/VALIDATION_SUMMARY.json`. The publication package's [metadata](PUBLICATION_METADATA.json) binds the edition names to source and archive identities.

## Architecture status

Native execution requires qualified toolchains, dependency closure, ABIs, drivers, buffer lifetimes, actual images, boot receipts and resource enforcement. Authenticated hyperfederation requires participant identities, delegated authority, typed payloads, durable effect transactions, replay protection, recovery and revocation. The published host references supply finite local models for developing these contracts.

Type B also specifies full optimizer state and collective coordination, TIFF/GIF decoding contracts, calibrated optical operators, logical proof checking and hardware telemetry. Complete distributed 1-bit LAMB training, image-container decoders, native boot, authenticated federation, quantum hardware, biological actuation and measured RAM telemetry are not implemented by its host extension. The research documentation supplies the requirements needed to evaluate future implementations. No external institutional endorsement or completed peer review is claimed.

## Contributions and release changes

Use the stable requirements and article application matrix to identify the behavior a contribution changes. Update the applicable specification, implementation, independent expected results and evidence together. Keep author-defined arithmetic separate from engineering admission policies. Preserve original sources and third-party notices.

A change to a compiler or kernel requires a new source identity, regeneration, relevant validation and review. Modified publications should clearly identify the change and date. Submit experimental native or physical results with their actual observer, environment, calibration, assumptions and receipt rather than promoting a proposed scenario to an executed result.

## License and copyright

Copyright (C) 2026 RUSSELL PHILIP SMITHSON.

The new publication documents listed in [COPYRIGHT](COPYRIGHT) are free works: you may redistribute and modify them under the GNU General Public License as published by the Free Software Foundation, **version 3 only**. They are distributed without warranty, including implied warranties of merchantability or fitness for a particular purpose. The complete terms are in [LICENSE](LICENSE).

The licensing scope is explicit in [LICENSING.md](LICENSING.md). Supplied articles, preserved upstream sources, figures, frozen references and bundled dependencies retain their existing terms. The Free Software Foundation copyright in the GNU license text is preserved. [NOTICE](NOTICE) records attribution and provenance boundaries.
