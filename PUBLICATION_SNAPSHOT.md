# Publication snapshot and repository provenance

Node & Norm maintains the canonical active CDFI Framework repository at
<https://github.com/node-and-norm/cdfi-framework>. Development and issues belong there.
The historical <https://github.com/mj3b/cdfi-framework> address is retained as a GitHub
transfer redirect, preserving the URL cited in the 2026 SAICRED chapter,
*Can You Trust AI with Your Faith? Introducing SAICRED: A Standard for Assessing AI
for Catholic Reliability and Doctrinal Fidelity*.

This note records repository preservation for that chapter. SAICRED remains an external
collaborative project with its existing leadership and publication authority. Repository
maintenance does not revise the chapter or establish that every chapter statement
corresponds to the May 31 source snapshot.

## Fixed v1.5 publication record

| Identifier | Value |
| --- | --- |
| Version and release date | v1.5, 2026-05-31 |
| Version DOI | [10.5281/zenodo.20475185](https://doi.org/10.5281/zenodo.20475185) |
| Zenodo record | [20475185](https://zenodo.org/records/20475185) |
| Git tag | [`v1.5`](https://github.com/node-and-norm/cdfi-framework/tree/v1.5) |
| Exact commit | `5e81799c6bc030b2ce5736cc8f9af2aaec0dbdb6` |
| Git tree | `8bf305d082f0eed59fcea84ac99c5a7ff8b026de` |
| Original release | [Framework v1.5](https://github.com/node-and-norm/cdfi-framework/releases/tag/v1.5) |
| Deposited filename | `mj3b/cdfi-framework-v1.5.zip` |
| Deposited ZIP MD5 | `59a008b7d08a22acaee105a6987ed00d` |
| Deposited ZIP SHA-256 | `3c08eb4476291e6d9a6ccbdd2697449a0103bb4941136912312a10f543ced54b` |

On 2026-09-27, all 56 files in the Zenodo ZIP were compared byte for byte with the
Git tree at this commit. All matched, with no extra files. The ZIP MD5 also matched
Zenodo's recorded checksum. These ZIP checksums apply to the deposited file;
GitHub-generated archives can have different ZIP metadata and directory names.

The concept DOI, `10.5281/zenodo.20453237`, identifies the version family.
Use the version DOI above when citing this specific snapshot.

## Citation metadata and later changes

The original v1.5 `CITATION.cff` contains `ZENODO_DOI_PLACEHOLDER` and the historical
`mj3b` repository URLs. Those bytes are preserved in both the Git tag and Zenodo
deposit. Zenodo's published record supplies the assigned DOI. The current
[`CITATION.cff`](CITATION.cff) provides the corrected DOI and canonical repository
URLs while retaining the v1.5 author, title, version, and release date.

The current branch includes post-release changes, including limitation disclosures,
links, and repository placement. It is not the deposited v1.5 snapshot. Reproducing
v1.5 requires the fixed commit or deposited archive; later work should record its
own exact commit and use a new version for a future release. This preservation
note makes no additional claim of theological validation or scoring certification.

```sh
git clone https://github.com/node-and-norm/cdfi-framework.git
cd cdfi-framework
git checkout --detach 5e81799c6bc030b2ce5736cc8f9af2aaec0dbdb6
git rev-parse HEAD
git rev-parse 'HEAD^{tree}'
```

## Preservation policy

- Keep Node & Norm as the single active authoritative repository.
- Keep `mj3b/cdfi-framework` unoccupied so its transfer redirects continue to serve
  historical repository, file, tag, and release links. GitHub documents that
  [recreating a repository at the old location permanently deletes those redirects](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository).
- Preserve existing tag names, targets, release records, and deposited files.
  In particular, retain the historical spellings `v.1.2` and `v.1.4`.
- Protect published tags against update and deletion. Any future release should
  receive a new version and retain a traceable connection to its own source commit.
- Keep archival notices and metadata corrections on the active branch, leaving
  the historical source tree unchanged.
- Before the next release, verify the transferred repository's Zenodo integration
  in Zenodo's account settings. An existing GitHub webhook alone does not establish
  that future deposits will succeed.

The preserved DOI and fixed source commit provide the archival publication snapshot.
A second writable repository at the historical address would create competing
provenance and remove the existing redirect.
