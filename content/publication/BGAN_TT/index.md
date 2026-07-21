---
title: "Boundary-Seeking GAN-Augmented TabTransformer for Adversarially Robust Intrusion Detection"
authors:
  - admin
  - Aliyah Kurniasih
date: "2026-07-21T00:00:00Z"
doi: 

# Schedule page publish date (NOT publication's date).
publishDate: "2026-01-21T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: Machine learning-based intrusion detection systems (IDSs) often suffer from class imbalance and vulnerability to adversarial attacks, leading to degraded detection performance and reduced robustness. This study proposes a TabTransformer framework augmented by the Boundary-Seeking Generative Adversarial Network (BGAN) for flow-based intrusion detection using the CICIDS2017 dataset. BGAN serves a dual purpose by generating synthetic minority-class samples to mitigate data imbalance and producing adversarial samples to evaluate model robustness. Experimental results demonstrate that BGAN augmentation improves TabTransformer's Macro-F1 score from 82.96% to 86.50%, with the largest class-wise improvement observed for Web_Attack (F1 score: 0.29 to 0.61). Robustness evaluation shows that all non-augmented models experienced a 100% Performance Drop Rate (PDR) under adversarial testing, whereas all BGAN-augmented models achieved negative PDR values, indicating improved resilience. Furthermore, the augmented TabTransformer maintained stable and low False Triggered Rate (FTR) values (1.51%-2.92%) across all noise levels, compared with the BGAN-augmented Decision Tree, which reached 49.09% under benign perturbations. These findings demonstrate that BGAN consistently enhances both class balance and adversarial robustness, while the proposed BGAN-TabTransformer framework provides an effective and adaptive intrusion detection solution for adversarial network environments.

# Summary. An optional shortened abstract.
summary: 
tags:
- Intrusion Detection
- Adversarial
- Network Security

featured: true

# - name: Custom Link
#   url: http://example.org
url_pdf: https://arxiv.org/abs/2607.16348
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
