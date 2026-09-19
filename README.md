# Selah content packs

This repository hosts downloadable SQLite content packs for the Selah mobile
app. It contains generated content artifacts only; the application source is
kept in the private `Ntermast/Selah` repository.

## Catalog

Selah reads [`catalog.json`](catalog.json), groups translations by language,
and shows both downloadable and requested editions. Entries marked
`available` can be downloaded. Entries marked `license_required` or
`preparing` are informational and have no download URL.

Before installation, Selah checks each download's byte length, SHA-256 digest,
pack identity, language, type and version.

| Pack | Language | Source and license information |
| --- | --- | --- |
| Berean Standard Bible (`bsb`) | English | [Berean Bible](https://berean.bible/) |
| King James Version (`kjv`) | English | [eBible.org](https://ebible.org/Scriptures/details.php?id=eng-kjv2006) |
| Darby Translation (`darby`) | English | [eBible.org](https://ebible.org/Scriptures/details.php?id=engDBY) |
| Bible Crampon 1923 (`bcc1923`) | French | [OSIS Bibles](https://github.com/bzerangue/osis-bibles/blob/master/fr/cramp23.xml), [public-domain declaration](https://www.crosswire.org/sword/copyright/ModInfoCopyright.jsp?modName=FreCrampon) |
| Bible J.N. Darby (`jnd`) | French | [eBible.org](https://ebible.org/Scriptures/details.php?id=frajnd) |
| Biblia Takatifu, ULB (`swh-ulb`) | Swahili | [eBible.org](https://ebible.org/Scriptures/details.php?id=swhulb) |

Most downloadable packs were generated from the
[HelloAO Free Use Bible API](https://bible.helloao.org/docs/); BCC1923 was
converted from its public-domain OSIS source. Each database
also stores its source identifier, source URL and license URL in `pack_info`.
Refer to the linked source page for the terms that apply to each translation.

## Integrity

Published hashes are recorded in both `catalog.json` and `SHA256SUMS`.
Pack files should be replaced only together with updated catalog metadata.
