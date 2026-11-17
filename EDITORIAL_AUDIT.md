# Editorial and Publication Audit

**Publication:** Verified Reciprocal Evolution  
**Author:** James Paul Jackson  
**Review date:** 16 November 2026, Eastern time  
**Scope:** Focused editorial, scientific-claim, file-integrity, and publication review. This is not independent academic peer review or an experimental replication.

## Findings and disposition

**Critical: 0. Major: 2. Minor: 3. All identified issues below are corrected.** Counts describe distinct issues, not the number of affected files or glyphs.

| ID | Severity | Original problem | Exact correction |
|:--|:--|:--|:--|
| E01 | Major | Section 4.3 said “an isolated structural learner tied the learned transfer arm.” The cited fresh-input experiment used local source observations and did not transfer peer artifacts. | Replaced **“learned transfer arm”** with **“learned structural arms”** in Markdown and Word, and regenerated the PDF from the corrected Word manuscript. The isolated-learner tie and no-superiority caveat remain unchanged. |
| E02 | Major | The original PDF conversion rendered four expectation closing square brackets as parentheses in §§5.2–5.4 and added an unwanted closing parenthesis to the piecewise update in §5. The Markdown and Word equation definitions were correct. | Exported the existing Word equations through Microsoft Word. Verified the four square-bracket closures and open-right cases expression visually. No equation, symbol definition, coefficient, or mathematical claim was changed in the source. |
| E03 | Minor | Section 4.2 did not name the directories underlying its 180/184 Python-file comparison. | Replaced **“180 of 184 corresponding Python source files (97.8%)”** with **“180 of 184 Python files in colony/ and hive/ (97.8%)”** in all manuscript editions. Added the same scope to claim C07. The ratio is unchanged. |
| E04 | Minor | The supplied citation file lacked the canonical repository URL and an explicit preferred research-paper citation. | Added canonical URLs and `preferred-citation` with `type: report`, author, title, year 2026, publication date, and an accurate white-paper note. No DOI, institution, journal, acceptance, or ORCID was added. |
| E05 | Minor | The supplied PDF had empty title, author, subject, and keyword metadata. | Set those fields to the manuscript title, James Paul Jackson, independent research white-paper description, and relevant keywords. |

The E01 correction is supported by the [frozen SYMBIOTE engineering report](https://github.com/jacksonjp0311-gif/SYMBIOTE/blob/482bf104c89721965ec006cc9f5b9f37237278bd/docs/ENGINE_EVOLUTION_002.md). The separate receiver-feedback scenario remains distinct from this observation-trained structural workload. E03 was checked by comparing Git blob identities at the two manuscript-cited revisions; the [source-check record](reproducibility/SCIENTIFIC_SOURCE_CHECKS.json) records the scope and results.

## Exact manuscript and layout changes

Only the two prose substitutions listed in E01 and E03 alter manuscript wording. The abstract, research thesis, numerical findings, scientific caveats, bibliography, and conclusions were retained.

For Word, only `word/document.xml` changed inside the DOCX package. In addition to the two substitutions, `w:keepNext` was added to the two figure paragraphs and `w:keepLines` to the single pseudocode paragraph, keeping captions with their figures and the algorithm together during PDF export. All other DOCX package members and all equation XML are unchanged. The final PDF remains twelve pages; native Word export changes some line and page breaks while retaining the existing design and artwork.

For GitHub Markdown, image paths were changed from `assets/` to `../assets/`, the two Pandoc-only `{width=6.05in}` attributes and the `\newpage` directive were removed, and the title, subtitle, author, and historical date were displayed as a readable title block. These presentation changes do not alter the scientific manuscript.

Historical edition information within the manuscript was preserved. Published manuscript filenames and the repository root are evergreen.

## Review performed

- Verified every entry in the original SHA-256 manifest against the extracted archive; recorded the original archive and all source-file hashes in [source provenance](reproducibility/SOURCE_PROVENANCE.json). The original ZIP and original manuscript files were not modified.
- Opened the original PDF with independent PDF libraries, extracted text from every page, and inspected the cover, results, mathematics, figures, and final evidence/reference pages. The original cross-reference-table warning did not prevent reading; the regenerated PDF opens cleanly.
- After identifying the conversion defect, rendered and visually inspected every page of the final Word export. Checked equations, tables, captions, headings, pagination, references, and readability. Word was used because this Windows bundled runtime does not include LibreOffice; no replacement office package was installed.
- Validated DOCX ZIP integrity and parsed all XML/relationship parts. Checked title and author metadata, equations, embedded figures, absence of tracked changes, and the empty comments part.
- Compared the final manuscript source against the original to restrict changes to the documented substitutions and presentation constraints. Checked PDF text against Word prose and table text, manuscript section coverage, citation markers, local links, images, and final artifact hashes.
- Checked references [1]–[10] against publisher-deposited DOI metadata and the arXiv record. Existing authors, titles, years, volumes, and pages were consistent; no bibliography edits were needed. See the [reference review](reproducibility/REFERENCE_REVIEW.md).
- Inspected the original license declaration, which identifies the manuscript and graphics as original works by James Paul Jackson and licenses them under CC BY 4.0. Reused the existing artwork without modification and retained third-party rights exclusions. No executable code was included or relicensed.

## Scientific-claim assessment

The corrected paper distinguishes implemented mechanisms from unproven advantages:

1. Agent Colony is a working computational-swarm architecture, not an established general-intelligence result. Its historical activity counters were checked at the cited revision and are not treated as matched causal effects.
2. One Mind is an experimental policy fork. Its code proximity, inherited history, and relaxed policy do not establish independent superiority.
3. SYMBIOTE demonstrates bounded persistent conditional learning. The isolated learner tied; scoped GF(2) work reduction is not a whole-system efficiency result. Separate receiver adoption/use is not proof of positive bilateral economic benefit.
4. Verification counts, evolution cycles, and search depth do not automatically establish generalization.
5. The equations are explicitly proposed engineering definitions and test targets, not established learning or convergence theorems.
6. The failed Agent Colony safety criterion, absence of cross-version gain, isolated-learning tie, historical HOLD, and unproven reciprocal benefit remain visible.
7. Novelty is framed relative to digital evolution, cooperative coevolution, classifier systems, swarm intelligence, and automated scientific discovery. The contribution is an architecture and measurement discipline.

The [research status](RESEARCH_STATUS.md) and [claims register](reproducibility/CLAIMS_AND_EVIDENCE.md) retain these boundaries. Principal source checks use the frozen revisions, not current counters. No experiments, holdouts, or research test suites were rerun.

## Publication packaging

- Created the repository README and research-status overview with the existing hero and architecture artwork.
- Moved the paper editions, bibliography, protocols, and evidence register into the publication layout; corrected the register's relative protocol links.
- Preserved the original release notes, changelog, and original manifest as historical evidence. **Files under `reproducibility/history/` describe the original archive.** Their old manifest commands do not apply to this reorganized repository. `ORIGINAL_MANIFEST.sha256` retains original names and hashes; do not run it against the new layout.
- Current integrity checks run from the repository root: `sha256sum -c reproducibility/PUBLICATION_MANIFEST.sha256`. The current manifest covers publication files except itself and Git internals. PowerShell users can compare `Get-FileHash -Algorithm SHA256` with those recorded digests.
- Excluded the duplicate paper-preview image, superseded publication instructions, original README/citation copies, the source ZIP, scripts used for review, temporary exports, page renders, caches, and credentials. Their original identities remain in provenance where applicable.

## Limitations

This review does not independently replicate experiments, certify the live implementations, establish legal title beyond the author's supplied rights declaration, or establish peer-review acceptance. One Mind's complete historical workflow failures and the detailed supporting-system implementation claims were not independently re-audited; their cited historical context was preserved. Some original Appendix B links navigate to mutable repository pages, so reproduction should follow the explicit commit identifiers and pinned links in the claims register and source-check record. Cost coefficients and non-overlapping accounting boundaries must be preregistered in future experiments; the current utility definitions do not establish an empirical advantage.

No unresolved publication-blocking defect was identified after the documented corrections.
