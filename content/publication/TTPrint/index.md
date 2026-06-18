---
title: "TTPrint: Evidence-Grounded TTP Extraction via Diverge-then-Converge Verification"
authors:
  - Yutong Cheng
  - Changze Li
  - admin
  - Qian Cui
  - Wei Ding
  - Peng Gao
date: "2026-05-25T00:00:00Z"
doi: 

# Schedule page publish date (NOT publication's date).
publishDate: "2026-05-25T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["preprint"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""
abstract: Extracting MITRE ATT&CK techniques from cyber threat intelligence (CTI) reports is an open-set, multi-label problem requiring both high recall (not missing techniques) and high precision (not hallucinating unsupported ones). Existing methods--rule-based, supervised, and LLM-based--struggle to achieve both: rule-based and supervised approaches lack generalizability across diverse attack descriptions, while LLM-based approaches that couple candidate generation and validation within a single inference step suffer from limited recall and precision simultaneously. We propose TTPrint, which addresses this challenge through a diverge-then-converge design inspired by how human analysts work: first extracting broadly, then verifying rigorously. In the divergent phase, reports are decomposed into atomic behaviors and candidate techniques are proposed broadly. A deterministic span localization stage then anchors each candidate to a specific evidence window in the source text. A convergent verification stage retains only candidates supported by both the localized evidence and the authoritative MITRE definition. We contribute two evaluation resources--a cleaned TRAM benchmark (TRAM-Clean) and a new annotated dataset (TTPrint-Bench)--to address known annotation noise in existing benchmarks and elevate the task to document-level TTP extraction. On TRAM-Clean and TTPrint-Bench, TTPrint achieves 76.48% and 87.39% macro-F1 respectively, outperforming the leading baseline by 63.5% and 29.4%. A multi-backbone analysis across six LLMs and a threshold sensitivity study further demonstrate generalizability across model choices and provide practical guidance for parameter selection.

# Summary. An optional shortened abstract.
summary: 
tags:
- NLP
- Natural Language
- TTP
- CTI

featured: true

# - name: Custom Link
#   url: http://example.org
url_pdf: https://arxiv.org/abs/2605.25836
# url_code: 'https://github.com/peng-gao-lab/nl2logic'
# url_dataset: '#'
# url_poster: 'https://drive.google.com/file/d/1C-HKYaHPiNal_VwPO3el_16W6PZocYJ2/view?usp=sharing'
# url_project: 'https://www.figma.com/design/vTypfrspxlCrNUiGJfnEoG/Jaklitera?node-id=53-1388&t=E9hRwvu900Xop4Ap-1'
# url_slides: 'https://drive.google.com/file/d/1Q1Ud5jXmYFzGeq5FS0CYwDHdCbKunQ8s/view?usp=drive_link'
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
