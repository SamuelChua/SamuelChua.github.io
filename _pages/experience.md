---
layout: default
permalink: /experience/
title: Experience
nav: true
nav_order: 1

# Content lives in front matter so it's easy to maintain
experiences:
  - company: Amazon
    location: Boston, MA
    role: Software Development Intern
    dates: Jun 2025 -- Sep 2025
    bullets:
      - Engineered a centralized AWS DynamoDB data transformation mechanism, reducing write operation costs by 50%
      - Designed virtual middleware to generate simplified real-time data representations for 20+ downstream teams
      - Implemented fill-forwarding algorithm to standardize temporal data management across 35+ business domains

  - company: VECTR Lab @ UCLA
    location: Los Angeles, CA
    role: Robotics Researcher
    dates: Dec 2023 -- Jun 2025
    bullets:
      - Implemented a LiDAR-based change detection pipeline using pose-aligned geometric differences of 3D submaps
      - Built spatial octrees to query point clouds 75% faster to perform change detection in dynamic environments
      - Integrated with Direct LIDAR-Inertial Odometry & Mapping algorithm, achieving long duration robot autonomy

  - company: DSO National Laboratories
    location: Singapore
    role: Robotics Algorithm Developer
    dates: Aug 2023 -- Sep 2023
    bullets:
      - Developed Viewpoint Generation algorithm for 3D urban search, optimizing inspection for swarm robotics drones
      - Built a C++ quad-tree for dynamic surface subdivision, significantly boosting inspection efficiency by 70%
      - Ensured complete surface coverage by validating drone camera footprints and checking for occlusion

  - company: Tandem Space (YC S24)
    location: San Francisco Bay Area, CA
    role: Full-Stack Developer
    dates: Apr 2023 -- Jun 2023
    bullets:
      - Utilized React JS to streamline manual data input by 50% through intuitive entry components and listing pages
      - Employed Django REST for efficient data modeling and JWT token authentication, facilitating data collection
      - Developed MVP by integrating front and back-end to enhance hybrid office space matching for 120+ companies

  - company: LEMUR Lab @ UCLA
    location: Los Angeles, CA
    role: Student Researcher
    dates: Nov 2022 -- Dec 2023
    bullets:
      - Formulated a robust Deep Reinforcement Learning algorithm to optimize distribution of large-scale robot systems
      - Employed decentralized controllers in Python to achieve Nash Equilibrium, enhancing Uber dispatching operations
      - Publication: 3rd Author on “Population-aware Online Mirror Descent for Mean-Field Games by Deep Reinforcement Learning,” International Conference on Autonomous Agents and Multiagent Systems (AAMAS)

activities_projects:
  - title: Association for Computing Machinery @ UCLA
    location: Los Angeles, CA
    role: Dev Team Officer
    dates: Apr 2024 -- Jun 2025
    bullets:
      - Developed ACM's membership portal with Next.js & ExpressJS, streamlining check-ins for 1,700+ members
      - Managed ACM's award-winning website on Netlify and enhancing UX, supporting UCLA's largest CS club
      - Automated data integration on the Dev Team page with Javascript parser scripts, improving maintenance efficiency

  - title: Pill.ai (LA Hacks 2024 Winner)
    link: https://github.com/SamuelChua/pill.ai
    dates: Apr 2024 -- Apr 2024
    bullets:
      - Engineered an LLM-driven web-app with React JS & Material UI, reducing medication-related errors by 90%
      - Leveraged Google's Gemini API, utilizing 1M tokens for precise speech-to-text and image-to-text translation
      - Successfully deployed a user-friendly and real-time dashboard for medication verification, benefiting 500+ patients
---

<div class="post">

  <div class="header-bar">
    <h1>{{ page.title }}</h1>
    {% if site.blog_description %}
      <h2>{{ site.blog_description }}</h2>
    {% endif %}
  </div>

  <!-- EXPERIENCE -->
  <h2 class="mt-4 mb-3">
    <i class="fa-solid fa-briefcase fa-sm"></i> Experience
  </h2>

  <ul class="post-list">
    {% for exp in page.experiences %}
      <li>
        <div class="card hoverable mb-3">
          <div class="card-body">
            <div class="d-flex justify-content-between align-items-start flex-wrap">
              <h3 class="card-title m-0">
                {{ exp.company }}
                <span class="text-muted"> | {{ exp.role }}</span>
              </h3>
              <p class="post-meta m-0">
                <i class="fa-solid fa-location-dot fa-sm"></i> {{ exp.location }}
                &nbsp; &middot; &nbsp;
                <i class="fa-solid fa-calendar fa-sm"></i> {{ exp.dates }}
              </p>
            </div>
            <ul class="mt-3">
              {% for b in exp.bullets %}
                <li>{{ b }}</li>
              {% endfor %}
            </ul>
          </div>
        </div>
      </li>
    {% endfor %}
  </ul>

  <hr>

  <!-- ACTIVITIES & PROJECTS -->
  <h2 class="mt-4 mb-3">
    <i class="fa-solid fa-diagram-project fa-sm"></i> Activities &amp; Projects
  </h2>

  <ul class="post-list">
    {% for ap in page.activities_projects %}
      <li>
        <div class="card hoverable mb-3">
          <div class="card-body">
            <div class="d-flex justify-content-between align-items-start flex-wrap">
              <h3 class="card-title m-0">
                {% if ap.link %}
                  <a class="post-title" href="{{ ap.link }}" target="_blank" rel="noopener">
                    {{ ap.title }}
                  </a>
                  <svg width="2rem" height="2rem" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg" aria-hidden="true" focusable="false">
                    <path d="M17 13.5v6H5v-12h6m3-3h6v6m0-6-9 9" class="icon_svg-stroke" stroke="#999" stroke-width="1.5" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path>
                  </svg>
                {% else %}
                  {{ ap.title }}
                {% endif %}
                {% if ap.role %}
                  <span class="text-muted"> | {{ ap.role }}</span>
                {% endif %}
              </h3>
              <p class="post-meta m-0">
                {% if ap.location %}
                  <i class="fa-solid fa-location-dot fa-sm"></i> {{ ap.location }}
                  &nbsp; &middot; &nbsp;
                {% endif %}
                <i class="fa-solid fa-calendar fa-sm"></i> {{ ap.dates }}
              </p>
            </div>
            <ul class="mt-3">
              {% for b in ap.bullets %}
                <li>{{ b }}</li>
              {% endfor %}
            </ul>
          </div>
        </div>
      </li>
    {% endfor %}
  </ul>

</div>
