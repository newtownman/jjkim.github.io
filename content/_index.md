---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-02-09
type: landing

design:
  spacing: '6rem'

sections:
  # 1. 프로필 섹션
  - block: resume-biography-3
    content:
      username: admin          # <--- ★여기를 admin으로 해야 아까 넣은 사진이 뜹니다!
      text: ''
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

  # 2. 연구 소개 섹션
  - block: markdown
    content:
      title: '📚 Research Interests'
      subtitle: ''
      text: |-
        Welcome to my research page. I am a Professor of English Linguistics at Pusan National University.
        
        My primary research interests lie in Sociolinguistics, Semantics, and Phonetics. I am passionate about exploring the intricate relationship between language and society.
    design:
      columns: '1'

  # 3. 주요 논문 (Featured)
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2

  # 4. 최근 논문 (Recent)
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation

  # 5. 강의/발표 (Talks) - 없으면 이 덩어리 삭제 가능
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - events
    design:
      view: card
---
