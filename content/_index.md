---
# Homepage. Each item under `sections` is one block on the page.
title: ''
summary: ''
type: landing

sections:
  - block: resume-biography-3
    content:
      username: me
      # About text shown on the homepage (Markdown).
      text: |-
        I develop microscopic tools to quantify how viruses interact with their hosts, currently using bacteriophages (viruses of bacteria) as a model system. This research supports the development of **phage therapy** strategies to combat **antimicrobial resistance**—a major public-health challenge. Some of my work has been published and is linked below.

        ![phage-bacteria, microscopy, tracking](phage_bac.jpg)

        At Yale, I am affiliated with the following entities:

        * [Paul Turner Lab](https://turnerlab.yale.edu/), Department of Ecology & Evolutionary Biology
        * [Center for Phage Biology and Therapy at Yale](https://phage.yale.edu/)
        * [Yale Quantitative Biology Institute](https://qbio.yale.edu/)
        * Closely collaborated with [Thierry Emonet Lab](http://emonet.biology.yale.edu/), Molecular, Cellular, and Developmental Biology
        * Recently joined [Joerg Bewersdorf Lab](https://bewersdorflab.yale.edu/) to perform image analysis on super-resolution microscopy datasets and to learn building new optical microscopy modalities

        My PhD research was in [Pushkar Lele Lab](http://pushkarlelelab.org/) at Texas A&M University. It focused on the physics of how bacteria move and sense their surroundings. My thesis dissertation (2021) was titled [Sensory Functions of the Bacterial Flagellar Motor](https://hdl.handle.net/1969.1/195225). 

        I took an advanced summer course on microscopy in 2022: [Optical Microscopy & Imaging in the Biomedical Sciences](https://www.mbl.edu/education/advanced-research-training-courses/course-offerings/optical-microscopy-imaging-biomedical-sciences) at Marine Biological Laboratories, Woods Hole, MA (USA). Having fallen in love with the course, I have been going back as a Research Facilitator.

        I contribute to scientific service and open science through editorial/society roles, method-sharing, and community outreach. To this end, I... 

        * serve on the editorial board of [mSystems](https://journals.asm.org/journal/msystems), a non-profit journal by the American Society for Microbiology ([ASM](https://asm.org/))
        * serve as a councilor at [ASM's Connecticut Valley Branch](https://sites.google.com/view/ctvalleybranchasm/home)
        * use [Foldscopes](https://foldscope.com/) to teach local middle school students about microscopy
        * have written [1 article](https://doi.org/pqns) (and counting) to explain my science to a high-school educated audience
        * made [a video](https://www.youtube.com/watch?v=8Ixnc2So3GE) explaining the protocol to make agarose pads for microscopic visualization of bacteria
      button:
        text: Download CV
        url: /media/CV_JAntani.pdf
      headings:
        about: 'About'
        education: 'Education'
        interests: 'Interests'
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

  - block: collection
    id: projects
    content:
      title: Key Publications
      text: 'Full list on [Google Scholar](https://scholar.google.com/citations?user=3S_V-uoAAAAJ).'
      filters:
        folders:
          - project
      count: 0
      sort_by: Date
      sort_ascending: false
    design:
      view: article-grid
      columns: 2

  - block: collection
    id: posts
    content:
      title: Science Outreach
      filters:
        folders:
          - post
      count: 0
    design:
      view: date-title-summary
---
