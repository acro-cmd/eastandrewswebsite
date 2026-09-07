---
# This is "front matter" — settings just for this one page.
layout: default
title: "About"
---

<!--
  HERO SECTION
  Big heading + subheading on the left, photo on the right.
  Edit the text directly below. To change the photo, replace
  the file at assets/images/hero-photo.jpg with your own image
  (keep the same filename, or update the "src" path below).
-->
<section class="hero">
  <div class="hero-text">
    <h1 class="hero-title">Doing Good, Better</h1>
    <p class="hero-subtitle">Welcome to Effective Altruism St. Andrews</p>
  </div>

  <div class="hero-image">
    <img src="{{ '/assets/images/hero-photo.jpg' | relative_url }}"
         alt="Two people talking">
  </div>
</section>

<!--
  ACCORDION SECTIONS ("About EA", "About us", "What we do on campus")
  Each <details> block is one collapsible section. Click the
  <summary> line to expand/collapse it — no JavaScript needed.

  TO EDIT: change the text inside <summary> (the title) or
  inside the <p> tags (the description).
  TO ADD a new section: copy one whole <details>...</details>
  block and edit it.
-->
<section class="accordion">

  <details class="accordion-item">
    <summary>About EA</summary>
    <p>
      Effective altruism is a project that combines both the heart and
      the head: using evidence and careful reasoning to figure out how
      to do as much good as possible, and taking action on that basis.
      Replace this paragraph with your own description.
    </p>
  </details>

  <details class="accordion-item">
    <summary>About us</summary>
    <p>
      Effective Altruism St. Andrews is a student-run group that
      explores how to have the greatest positive impact with our time,
      careers, and resources. Replace this paragraph with your own
      description of the group.
    </p>
  </details>

  <details class="accordion-item">
    <summary>What we do on campus</summary>
    <p>
      We run weekly discussions, reading groups, guest talks, and
      fellowships (like Arete and STAIR) open to all students,
      regardless of background or experience with EA. Replace this
      paragraph with your own description.
    </p>
  </details>

</section>
