# Echo Check — Word Repetition & Pattern Analysis

Analyzes a piece of writing for word echoes, clustering, and repetitive sentence patterns.

## When to Use

- During Substack post prep (called from `/prep-hey-claude-post` or `/prep-cheshire-cat-post`)
- When reviewing book scenes or chapters
- On any piece of writing where repetition might be an issue

---

## Step 1: Identify the Text

If the text isn't already loaded in context (e.g., from a prep workflow), ask:

**"What would you like me to analyze?"**

Accepted inputs:
- **Ulysses document** — Read Content.xml from the specified or most recent document
- **Scrivener scene/chapter** — Read RTF content from the Scrivener project
- **Pasted text** — User pastes content directly
- **Already in context** — If running within a prep workflow, use the post content already loaded

Extract plain text by stripping all markup/formatting tags before analysis.

---

## Step 2: Word Frequency Analysis

### 2a: Count total words
Report the total word count of the piece.

### 2b: Generate content word frequency
Strip out **function words** (articles, pronouns, prepositions, conjunctions, auxiliary verbs — e.g., the, a, I, it, to, and, of, in, is, was, that, but, for, with, etc.) and XML/markup tags.

Count remaining **content words** (nouns, main verbs, adjectives, adverbs). Include morphological variants together where useful for readability (e.g., "build" and "building" can be noted together, but report individual counts too).

Present the **top 15 content words** in a table:

| Word | Count | Density | Type |
|------|-------|---------|------|
| [word] | Nx | X.XX% | Thematic / Non-thematic |

### 2c: Classify each top word

For each top word, determine:
- **Thematic** — Central to the topic. The post/chapter is *about* this thing. Expected to repeat. (e.g., "process" in a post about process, "imagination" in a book about imagination)
- **Non-thematic** — Not central to the topic. Repetition may indicate a verbal habit or missed variety opportunity. (e.g., "fascinating" appearing 5x, "discover" in every section)

**Classification principle:** Ask "If I replaced every instance of this word with a synonym, would the piece lose clarity or identity?" If yes → thematic. If no → non-thematic.

---

## Step 3: Echo Detection (Clustering)

For each word appearing **5+ times**, scan for **clusters** — instances where the same word appears within a **2-3 paragraph window** (~200-300 words).

### What to flag:

| Rule | Applies to | Threshold |
|------|-----------|-----------|
| Same word 3+ times in a single paragraph | All content words (thematic and non-thematic) | Always flag |
| Same word in consecutive paragraphs | Non-thematic words | Flag |
| Same word in consecutive paragraphs | Thematic words | Flag only if 3+ consecutive paragraphs |
| Distinctive/unusual word used 2+ times | Any word that feels "noticeable" | Flag with distance |

### Output format:

For each flagged cluster:
| Word | Where | Occurrences | Issue |
|------|-------|-------------|-------|
| [word] | paragraphs X-Y | 3x in ~200 words | Thematic clustering / Non-thematic echo |

**Include a brief recommendation** for each: whether to vary the word, restructure sentences, or leave as-is (with reasoning).

---

## Step 4: Sentence-Start Repetition

Scan all sentences for **consecutive sentences starting with the same word**.

### What to flag:

| Pattern | Severity |
|---------|----------|
| 3+ consecutive sentences starting with the same word | Flag — almost always worth varying |
| 2 consecutive sentences starting with the same word | Note only if the word is distinctive (not "The" or "I") |
| 3+ sentences in a paragraph starting with "I" | Flag — "galloping I" pattern, common in personal essays |

### Output format:

| Starting word | Where | Count | Suggestion |
|---------------|-------|-------|------------|
| [word] | paragraph X | 3 consecutive | Vary openers — try starting with a clause, question, or action |

---

## Step 5: Summary & Recommendations

Present a brief overall assessment:

### Document stats:
- **Word count:** X
- **Unique content words:** X
- **Top thematic terms:** [list]

### Findings:
- **Word echoes found:** X clusters flagged (Y thematic, Z non-thematic)
- **Sentence-start repetitions:** X patterns flagged
- **Overall assessment:** One of:
  - **Clean** — No significant repetition issues. Thematic words are doing their job.
  - **Minor echoes** — A few clusters worth reviewing, but nothing that breaks the reading flow.
  - **Needs attention** — Noticeable repetition that may fatigue the reader. Specific suggestions provided.

### Action items:
Only list items that are actually worth changing. For thematic words that cluster in relevant sections, explicitly say "this is fine — the word is doing its job here."

---

## Important Principles

- **Thematic words get a pass on total frequency** — "process" appearing 20x in a post about process is expected. Only flag if clustering is extreme (3+ in one paragraph).
- **Non-thematic words are the real echoes** — These are what readers actually notice. A stray "fascinating" or "discover" appearing every few paragraphs is more distracting than a thematic keyword appearing 40 times.
- **Context matters** — Conversational blog posts naturally repeat more than formal writing. Book chapters in close third-person will repeat character names. Don't apply academic density standards to conversational prose.
- **Don't over-correct** — Replacing every "process" with "workflow," "approach," "methodology," and "system" creates its own problem (thesaurus syndrome). Sometimes repeating the right word is better than forcing variety.
- **Blockquotes/quotes** — Words inside quoted material (blockquotes, dialogue, cited text) should be counted but flagged separately. The author may not want to change quoted content.
- **Genre-appropriate density** — For conversational blog posts (Hey Claude), expect lexical density ~40-49%. For literary essays (Cheshire Cat Lab), expect ~48-55%. For book chapters, depends on the style.
