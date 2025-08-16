---
layout: default
permalink: /experience/
title: Experience
nav: true
nav_order: 1

experiences:
  - company: Amazon
    location: Boston, MA, USA
    role: Software Development Intern
    dates: Jun 2025 -- Sep 2025
    bullets:
      - Engineered a centralized AWS DynamoDB data transformation mechanism, reducing write operation costs by 50%
      - Designed virtual middleware to generate simplified real-time data representations for 20+ downstream teams
      - Implemented fill-forwarding algorithm to standardize temporal data management across 35+ business domains

  - company: Association for Computing Machinery @ UCLA
    location: Los Angeles, CA, USA
    role: Dev Team Officer
    dates: Apr 2024 -- Jun 2025
    bullets:
      - Developed ACM's membership portal with Next.js & ExpressJS, streamlining check-ins for 1,700+ members
      - Managed ACM's award-winning website on Netlify and enhancing UX, supporting UCLA's largest CS club
      - Automated data integration on the Dev Team page with Javascript parser scripts, improving maintenance efficiency

  - company: Verifiable & Control Theoretic Robotics Lab @ UCLA
    location: Los Angeles, CA, USA
    role: Robotics Researcher
    dates: Dec 2023 -- Jun 2025
    bullets:
      - Implemented a LiDAR-based change detection pipeline using pose-aligned geometric differences of 3D submaps
      - Built spatial octrees to query point clouds 75% faster to perform change detection in dynamic environments
      - Integrated with Direct LIDAR-Inertial Odometry & Mapping algorithm, achieving long duration robot autonomy

  - company: Defence Science Organization (DSO) National Laboratories
    location: Singapore
    role: Robotics Algorithm Intern
    dates: Jul 2024 -- Sep 2024
    bullets:
      - Developed and evaluated LIDAR-Inertial Odometry (LIO) algorithms for quadrupedal robots in SLAM tasks as part of a collaboration with KAIST
      - Implemented Direct LIO algorithms and degeneracy detection techniques to improve navigation in feature-sparse and motion-distorted conditions
      - Tested algorithms on challenging terrains to advance legged robot autonomy and reliability

  - company: Laboratory for Embedded Machines & Ubiquitous Robots @ UCLA
    location: Los Angeles, CA, USA
    role: Undergraduate Researcher
    dates: Nov 2022 -- Dec 2023
    bullets:
      - Formulated a robust Deep Reinforcement Learning algorithm to optimize distribution of large-scale robot systems
      - Employed decentralized controllers in Python to achieve Nash Equilibrium, enhancing Uber dispatching operations
      - Publication - 3rd Author on “Population-aware Online Mirror Descent for Mean-Field Games by Deep Reinforcement Learning,” International Conference on Autonomous Agents and Multiagent Systems (AAMAS)

  - company: Defence Science Organization (DSO) National Laboratories
    location: Singapore
    role: Robotics Algorithm Developer
    dates: Aug 2023 -- Sep 2023
    bullets:
      - Developed Viewpoint Generation algorithm for 3D urban search, optimizing inspection for swarm robotics drones
      - Built a C++ quad-tree for dynamic surface subdivision, significantly boosting inspection efficiency by 70%
      - Ensured complete surface coverage by validating drone camera footprints and checking for occlusion

  - company: Unmanned Aerial Systems @ UCLA
    location: Los Angeles, CA, USA
    role: UAS AUVSI Software Engineer
    dates: Sep 2022 -- Sep 2023
    bullets:
      - Researched path-finding algorithms for fixed-wing drone to perform obstacle avoidance and autonomous mission execution
      - Simulated flight behavior using ArduPilot and Gazebo to visualize navigation for Critical Design Review
      - Developed Python scripts to scan airdrop boundaries for safe package delivery at 75ft in minimal time

  - company: Tandem Space (YC S24)
    location: San Francisco, CA, USA
    role: Full-Stack Developer
    dates: Apr 2023 -- Jun 2023
    bullets:
      - Utilized React JS to streamline manual data input by 50% through intuitive entry components and listing pages
      - Employed Django REST for efficient data modeling and JWT token authentication, facilitating data collection
      - Developed MVP integrating front-end and back-end to enhance hybrid office space matching for 120+ companies

  - company: Defence Science & Technology Agency (DSTA)
    location: Singapore
    role: Robotics Engineer
    dates: May 2022 -- Jun 2022
    bullets:
      - Integrated Computer Vision and Natural Language Processing for robots in search and rescue missions
      - Achieved mAP 0.5:0.95 of 83% and 98% accuracy by fine-tuning Detectron2 and HuBERT models
      - Secured 5th place in national robotics competition using DJI RoboMaster S1 SDK out of 80+ teams and 3000+ students

  - company: Defence Science Organization (DSO) National Laboratories
    location: Singapore
    role: Artificial Intelligence Research Intern
    dates: Jan 2020 -- Mar 2020
    bullets:
      - Developed deep learning algorithms with over 90% accuracy in one-class classification of optical images using fast.ai
      - Trained PyTorch CNN to produce descriptive features while maintaining low intra-class variance
      - Optimized U-Nets for classification and devised image-cropping algorithms for preprocessing 10,000+ images

activities_projects:
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
  </div>

  <!-- EXPERIENCE -->

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
                  <svg width="2rem" height="2rem" viewBox="0 0 40 40" xmlns="http://www.w3.org/2000/svg">
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
