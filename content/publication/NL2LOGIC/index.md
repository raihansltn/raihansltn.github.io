---
title: "NL2LOGIC: AST-Guided Translation of Natural Language into First-Order Logic with Large Language Models"
authors:
  - Rizky Ramadhana Putra
  - admin
  - Yutong Cheng
  - Peng Gao
date: "2026-01-04T00:00:00Z"
doi: 

# Schedule page publish date (NOT publication's date).
publishDate: "2026-01-04T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: Automated reasoning is critical in domains such as law and governance, where verifying claims against facts in documents requires both accuracy and interpretability. Recent work has adopted a structured reasoning paradigm that parses first-order logic (FOL) rules from natural language and delegates inference to automated solvers. With the rise of large language models (LLMs), methods such as GCD and CODE4LOGIC leverage their reasoning and code generation capabilities to enhance logic parsing. However, these approaches suffer from (1) fragile syntax control, due to weak enforcement of global grammar consistency, and (2) low semantic faithfulness, as they lack fine-grained clause-level semantic understanding. To address these challenges, we propose NL2LOGIC, a FOL translation framework that uses an AST as an intermediate layer, combining a recursive LLM-based semantic parser with an AST-guided generator that deterministically produces solver-ready code. On the FO- LIO, LogicNLI, and ProofWriter benchmarks, NL2LOGIC attains 99% syntactic accuracy and improves semantic correctness by 30% over state-of-the-art baselines. Moreover, integrating NL2LOGIC into Logic-LM yields near- perfect executability and improves downstream reasoning accuracy by 31% over Logic-LM’s original few-shot unconstrained FOL translation module

# Summary. An optional shortened abstract.
summary: 
tags:
- NLP
- Natural Language
- AST
- First Order Language

featured: true

# - name: Custom Link
#   url: http://example.org
url_pdf: https://www.arxiv.org/abs/2602.13237
url_code: 'https://github.com/peng-gao-lab/nl2logic'
# url_dataset: '#'
url_poster: 'https://drive.google.com/file/d/1C-HKYaHPiNal_VwPO3el_16W6PZocYJ2/view?usp=sharing'
# url_project: 'https://www.figma.com/design/vTypfrspxlCrNUiGJfnEoG/Jaklitera?node-id=53-1388&t=E9hRwvu900Xop4Ap-1'
url_slides: 'https://drive.google.com/file/d/1Q1Ud5jXmYFzGeq5FS0CYwDHdCbKunQ8s/view?usp=drive_link'
# url_source: '#'
# url_video: '#'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Authors'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: example
---
