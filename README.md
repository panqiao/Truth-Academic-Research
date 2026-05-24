# Truth Academic Research

## AI-Powered Scientific Knowledge Tree Pruning

**Truth Academic Research** is building an AI system to map, evaluate, and prune unreliable branches in scientific literature.

Modern science grows like a tree. Some branches are strong, supported by reproducible evidence. Others are built on weak claims, circular citations, selective reporting, image manipulation, or conclusions that were never independently verified.

Our goal is to help researchers, funders, institutions, and biotech teams identify which scientific claims are reliable — and which branches of the literature need to be re-examined.

![Scientific Knowledge Tree](assets/scientific-knowledge-tree.png)

---

## Why This Matters

Life science research has produced transformative discoveries, including DNA structure, CRISPR, mRNA vaccines, single-cell sequencing, and synthetic biology.

However, the same field also faces serious reproducibility and integrity challenges:

- Foundational claims may be cited thousands of times without independent validation.
- Negative results are often unpublished or underweighted.
- Papers may rely on repeated use of the same datasets, images, cell lines, or assumptions.
- Some areas are vulnerable to image manipulation, statistical overfitting, selective reporting, or exaggerated therapeutic claims.
- AI language models can summarize literature, but they often compress away methodological flaws, contradictory evidence, and hidden dependency chains.

We believe scientific discovery needs a new infrastructure layer:

> Not just search.  
> Not just summarization.  
> A claim-level reliability map.

---

## Core Idea

Truth Academic Research constructs a **Scientific Knowledge Tree** for a research field.

Each node represents a scientific claim.  
Each edge represents an evidence relationship.

Examples of evidence edges:

- `supports`
- `refutes`
- `replicates`
- `depends_on`
- `contradicts`
- `uses_same_dataset_as`
- `shares_authorship_with`
- `requires_independent_validation`

The system then identifies weak or suspicious branches and helps researchers decide which claims are reliable, uncertain, or potentially misleading.

---

## What the System Detects

### 1. Circular Citation Loops

A claim appears well-supported because many papers cite it, but the citations trace back to the same original source or a small group of dependent studies.

### 2. Unsupported Foundational Claims

A downstream field may be built on assumptions that were never rigorously validated.

### 3. Image and Data Integrity Risks

Common signals include:

- Reused or duplicated microscopy images
- Western blot band duplication
- Suspicious image splicing
- Repeated flow cytometry plots
- Missing raw data
- Inconsistent metadata
- Figure-level inconsistencies across papers

### 4. Statistical and Analytical Weaknesses

Examples include:

- P-hacking
- Underpowered animal studies
- Selective endpoint reporting
- Multiple testing without correction
- Overinterpretation of omics data
- Lack of independent validation cohorts

### 5. Overclaimed Translational Relevance

Especially common in high-pressure life science areas such as:

- Cancer biomarkers
- Stem cell therapy
- Gene therapy
- Neurodegeneration mechanisms
- Immunotherapy targets
- Microbiome-disease associations
- Anti-aging interventions
- Preclinical vaccine platforms
- AI-discovered drug targets

These areas are not inherently unreliable, but they often involve high publication pressure, complex data, expensive validation, and strong commercial incentives.

---

## Example: Life Science Risk Areas

| Research Direction | Common Risk Pattern |
|---|---|
| Cancer biomarkers | Small cohorts, weak validation, overfitted signatures |
| Western blot-heavy mechanistic biology | Image duplication, band splicing, selective presentation |
| Stem cell therapy | Overclaimed regeneration effects, weak functional validation |
| Neurodegeneration targets | Long citation chains built on fragile animal models |
| Microbiome studies | Correlation overinterpreted as causation |
| Single-cell omics | Cluster overinterpretation, batch effects, selective marker use |
| Gene therapy | Safety claims based on incomplete long-term data |
| Immunotherapy targets | Context-dependent effects generalized too broadly |
| Aging biology | Broad claims from limited model systems |
| AI drug discovery | Benchmark leakage, weak wet-lab confirmation |

---

## System Workflow

```text
Scientific Literature
        ↓
Claim Extraction
        ↓
Evidence Graph Construction
        ↓
Citation Dependency Mapping
        ↓
Risk Signal Detection
        ↓
Reliability Scoring
        ↓
Knowledge Tree Pruning
