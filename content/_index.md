---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: My CV's
        url: cv/
    design:
      color: white
      background:
        image:
          # Name of image in `assets/media/`.
          # filename: background.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.5
            #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
            size: cover
            # Image focal point. Options include `left`, `center` (default), or `right`.
            position: center
            # Use a fun parallax-like fixed background effect on desktop? true/false
            parallax: true
            # Text color (true=light, false=dark, or remove for the dynamic theme color).
            text_color_light: true
  - block: markdown
    content:
      title: 'My Research'
      subtitle: ''
      text: |-
        My research interests are to discover and understand critical security issues, and then to design and develop innovative solutions to address these issues.
        
        To be precise, my research areas and interests:
        - Secure ML Systems
        - NLP/ML-assisted Anomaly Detection
        - Vulnerability Discovery
        - Firmware Security & Reverse Engineering
        - Side-channel Attacks on Wireless Networks
        - Cyber Threat Intelligence
        - IPS/IDS
        - Privacy Compliance and Enforcement (Formal Methods)
        - Programmable Network Security

        I’m always excited to collaborate with like-minded individuals and organizations to solve complex challenges and drive innovation. Please reach me at raihansultanpb@gmail.com for a research collaboration!
    design:
      columns: '1'
      color: white
      design:
      view: article-grid
      columns: 2
      background:
        image:
          # Name of image in `assets/media/`.
          # filename: cyber.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.2
          #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
          size: cover
          # Image focal point. Options include `left`, `center` (default), or `right`.
          position: center
          # Use a fun parallax-like fixed background effect on desktop? true/false
          parallax: true
          # Text color (true=light, false=dark, or remove for the dynamic theme color).
          text_color_light: false
  - block: collection
    content:
      title: Recent Publications
      text: ""
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation
  - block: markdown
    id: news
    content:
      title: 'Recent News'
      subtitle: ''
      text: |-
        - <ins>News</ins> **Oct 5, 2025**: Started a Teaching Assistant position for KKAI300 – Artificial Intelligence for the Fall 2025 semester.
        - <ins>News</ins> **May 21, 2025**: Started conduct research for [VT Security Intelligence Laboratory.](https://people.cs.vt.edu/penggao/lab.html)
        - <ins>News</ins> **May 13, 2025**: Started conduct research for ESQ Group Corporation, as their ML Researcher, working on LLM.
        - <ins>News</ins> **Apr 17, 2025**: [Full-time Research Assistant at AIRDU Research Group.](https://raihansultan.tech/post/airdu-ra/)
        - <ins>News</ins> **Mar 13, 2025**: [Brainstorming and Project Initation with AIRDU Research Group.](https://raihansultan.tech/post/airdu-initiate/)
        - <ins>Research</ins> **Jan 3, 2025**: We proposed [DepPredict](https://raihansultan.tech/publication/pmpdp/), a model to predict and identifies the likelihood of depression for students.
        - <ins>Award</ins> **Dec 2, 2024**: Raihan received Garuda ACE 2.0 Research Fellowship Award by MoECRT of Indonesia.
    design:
      columns: '1'
      color: white
      design:
      view: article-grid
      columns: 2
      background:
        image:
          # Name of image in `assets/media/`.
          # filename: cyber.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.2
          #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
          size: cover
          # Image focal point. Options include `left`, `center` (default), or `right`.
          position: center
          # Use a fun parallax-like fixed background effect on desktop? true/false
          parallax: true
          # Text color (true=light, false=dark, or remove for the dynamic theme color).
          text_color_light: false
  #   content:
  #     title: Recent News
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: post
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: date-title-summary
  #     # Reduce spacing
  #     spacing:
  #       padding: [10, 10, 0, 0]
  - block: collection
    id: contents
    content:
      title: Contents
      filters:
        folders:
          - teaching
        featured_only: false
    design:
      view: article-grid
      columns: 2
      background:
        image:
          # Name of image in `assets/media/`.
          # filename: background1.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.4
            #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
            size: cover
            # Image focal point. Options include `left`, `center` (default), or `right`.
            position: center
            # Use a fun parallax-like fixed background effect on desktop? true/false
            parallax: true
            # Text color (true=light, false=dark, or remove for the dynamic theme color).
            text_color_light: false
  - block: collection
    id: project
    content:
      title: Projects
      filters:
        folders:
          - project
    design:
      view: article-grid
      columns: 2
      color: white
      background:
        image:
          # Name of image in `assets/media/`.
          # filename: background3.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.4
          #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
          size: cover
          # Image focal point. Options include `left`, `center` (default), or `right`.
          position: center
          # Use a fun parallax-like fixed background effect on desktop? true/false
          parallax: true
          # Text color (true=light, false=dark, or remove for the dynamic theme color).
          text_color_light: false
  
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      view: article-grid
      columns: 1
      color: white
      background:
        image:
          # Name of image in `assets/media/`.
          # filename: background2.jpg
          # Apply image filters?
          filters:
            # Darken the image? Range 0-1 where 1 is transparent and 0 is opaque.
            brightness: 0.4
          #  Image fit. Options are `cover` (default), `contain`, or `actual` size.
          size: cover
          # Image focal point. Options include `left`, `center` (default), or `right`.
          position: center
          # Use a fun parallax-like fixed background effect on desktop? true/false
          parallax: true
          # Text color (true=light, false=dark, or remove for the dynamic theme color).
          text_color_light: false
  - block: cta-card
    demo: true # Only display this section in the Hugo Blox Builder demo site
    content:
      title: Raihan Sultan Pasha Basuki
      text: |-
        Hi there, I'm Raihan! An undergraduate Computer Science student at Universitas Ary Ginanjar, diving deep into Cybersecurity especially Network Security (My career path), I'm also a Security Researcher, where you can find me on Bugcrowd and HackerOne. 
      button:
        text: See More
        url: https://raihansltn.github.io/
    design:
      card:
        # Card background color (CSS class)
        css_class: "bg-primary-700"
        css_style: ""
---
