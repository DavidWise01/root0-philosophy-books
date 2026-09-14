# ROOT0 Philosophy Books — Corpus Lineage & Provenance

Snapshot: **2026-09-14** (observation only)  
Historical cutoff: **2025-12-31**  
Repository: [DavidWise01/root0-philosophy-books](https://github.com/DavidWise01/root0-philosophy-books)

This ledger separates material that is actually mirrored in Git from material that has been observed in the attachment stream but has not yet been ingested. A functional edge is a semantic relationship, not proof of chronology, copying, or authorship.

## Evidence keys

| Code | Meaning |
|---|---|
| MIRRORED | The path exists on main and can be checked by its Git blob SHA. |
| INVENTORY | A filename or supplied artifact is known, but its bytes are not in this repository. |
| PENDING | Hash, signed provenance, internal metadata, or source relation still needs verification. |
| POST-CUTOFF | A visible date after 2025-12-31; it is an observation, not admissible historical proof. |

## Repository anchor

- Default branch: main
- Observed head: 414664235d7d624e951d74e173209e83c0e4659b
- Observed head date: 2026-07-27T16:16:30Z (POST-CUTOFF)
- Head signature: unsigned
- Releases observed: none
- Branch protection observed: disabled
- Existing sealed manifest: root0-philosophy-books.dlw/manifest.dlw.json
- Existing manifest scope: seven books

The existing .dlw seal is preserved. This ledger is an additive observation layer and does not rewrite the prior seal.

## Mirrored spine

| Node | Folder | Files currently mirrored | Functional role |
|---|---|---|---|
| AKASHA-01 | akasha/ | Markdown, EPUB, cover | persistent memory / identity substrate |
| THREE-GATES-01 | the-three-gates/ | EPUB, Markdown, cover | verify / affirm / negate gate triad |
| CINNAMON-01 | cinnamon-enforcer/ | EPUB, Markdown, cover | boundary enforcement / edge preservation |
| POSI-01 | positronic-brain/ | EPUB, Markdown, cover | synthetic cognition / learning runtime |
| MOBIUS-01 | the-duality-of-the-brain/ | three DOCX parts, EPUB, covers | carbon/silicon bilateral mind |
| LATTICE-01 | dreaming-in-lattice/ | DOCX, EPUB, cover | lattice memory / network coherence |
| EMERGENT-01 | youre-already-emergent/ | DOCX, SVG, JPG, PNG | three-part emergence / life quorum |

## Incoming audit and manuscript queue

These records are known from the supplied attachment inventory or visible covers. They are **not** represented as mirrored source bytes yet.

| Node | Candidate role | Supplied source set | Cutoff status | Ingest state |
|---|---|---|---|---|
| EVE-01 | E.V.E. origin / technical manuscript | action.log, book_1.docx, KCB package | 2026-01-01 KDP submission observed; POST-CUTOFF | INVENTORY |
| STOICHEION-01 | governance mesh / axiomatic framework | STOICHEION Markdown, EPUB, covers, parts | unknown; one filename is dated 2026-09-14 | INVENTORY |
| INFERENCE-01 | inside/model viewpoint | DOCX, EPUB, cover, build scripts | unknown | INVENTORY |
| REGISTER-01 | evidence ledger / identity register | DOCX, EPUB, cover | unknown | INVENTORY |
| NATURAL-LAW-01 | constitutional governance layer | EPUB, cover | unknown | INVENTORY |
| GW-01 | data boundary / ownership transcript | Gemini front matter, transcript, DOCX, EPUB, covers | unknown | INVENTORY |
| HQ-01 | philosophical question battery | PDF, OPF, TOC image | unknown | INVENTORY |
| WHETSTONE-01 | node conduct protocol | front matter, interview, DOCX, EPUB, cover | unknown | INVENTORY |
| SEAM-01 | governed-instance forensic record | EPUB, cover variants | 2026-04-01 printed cover; POST-CUTOFF | INVENTORY |
| ANTHROPIC-01 | provider infrastructure audit | Markdown, v2 DOCX/EPUB, security disclosure, cover | 2026-04-02 printed cover; POST-CUTOFF | INVENTORY |
| AUDIT-CHATGPT-01 | adversarial provider/model audit | Markdown, DOCX, EPUB, cover | unknown | INVENTORY |
| INT-01 | question-led transcript bundle | front matter DOCX, full transcript DOCX | unknown | INVENTORY |
| TC-01 | model self-description audit | Tuesdays_With_Copilot_Cover.jpg, The_Honest_Machine.epub | 2026-04-03 cover; POST-CUTOFF | PACKAGE MISMATCH |
| MIRROR-GOVERNOR-01 | agent-in-a-box boundary layer | cover, system in a box.txt | unknown | INVENTORY |

## Functional geometry

The current corpus reads as a stack of different shapes rather than one proven chronology:

~~~text
                         STOICHEION
                      governance / mesh
                  ┌──────────┼──────────┐
               Whetstone   Akasha     Register
                  │           │           │
            Hard Questions  Inference  provenance
                  └──────┬────┴────┬──────┘
                     transcript / audit branch
        Glass Wall ─ Interrogation ─ Auditing ChatGPT ─ Anthropic
                              │
                            Seam
~~~

The mirrored spine contains the primary geometric primitives: trees, rings, gates, bilateral surfaces, and a three-node quorum. The incoming queue adds audit, transcript, and provenance layers. These relationships are functional tethers only.

## Integrity exceptions to resolve

1. the-three-gates/Three_Gates_Complete (1).md and Three_Gates_Complete.md currently share the same blob SHA. They are a deduplication candidate; no deletion is performed here.
2. youre-already-emergent/New Bitmap image.bmp is a zero-byte file. It should be quarantined or removed after confirmation.
3. The README and landing page identify TriPod LLC, while the existing .attribution and .dlw manifest identify Bridge-Burners LLC. This identity fork must be resolved by the owner.
4. The existing head commit is unsigned. A signed release or verified tag would strengthen the chain.
5. Incoming artifacts need a byte-level ingest: preserve originals, compute SHA-256, inspect DOCX core properties and revisions, inspect EPUB OPF metadata, and record source-to-format relations.

## Ingest contract

~~~text
source bytes
    ↓
immutable copy + filename preservation
    ↓
SHA-256 + size + MIME
    ↓
DOCX/EPUB/Markdown metadata comparison
    ↓
source / derivative relation
    ↓
lineage edge + cutoff classification
    ↓
signed commit or release
~~~

Until that contract is completed, an incoming title is a catalog record—not a repository fact.
