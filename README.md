# Selah content packs

This repository hosts downloadable SQLite content packs for the Selah mobile
app. It contains generated content artifacts only; the application source is
kept in the private `Ntermast/Selah` repository.

## Catalog

Selah reads [`catalog.json`](catalog.json), downloads the selected pack, then
checks its byte length, SHA-256 digest, pack identity, language, type and
version before installing it.

| Pack | Language | Source and license information |
| --- | --- | --- |
| Berean Standard Bible (`bsb`) | English | [Berean Bible](https://berean.bible/) |
| Bible J.N. Darby (`jnd`) | French | [eBible.org](https://ebible.org/Scriptures/details.php?id=frajnd) |
| Biblia Takatifu, ULB (`swh-ulb`) | Swahili | [eBible.org](https://ebible.org/Scriptures/details.php?id=swhulb) |

The packs were generated from the
[HelloAO Free Use Bible API](https://bible.helloao.org/docs/). Each database
also stores its source identifier, source URL and license URL in `pack_info`.
Refer to the linked source page for the terms that apply to each translation.

## Integrity

Published hashes are recorded in both `catalog.json` and `SHA256SUMS`.
Pack files should be replaced only together with updated catalog metadata.
