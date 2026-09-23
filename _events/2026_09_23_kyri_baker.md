---
# Replace the TBA values as speaker details become available.
# Keep text values quoted so punctuation remains valid YAML.
title: "Challenges with Existing Learning-for-OPF Neural Proxies, and how Constrained Learning can Help"
speaker: "Kyri Baker"
affiliation: "University of Colorado Boulder"

# Optional personal or institutional profile.
speaker_url: http://www.kyrib.com/

# Change these fields if this talk is rescheduled or shortened.
# America/New_York supplies EST/EDT automatically; do not add a UTC offset.
talk_date: "2026-09-23"
start_time: "3:00 PM"
duration_minutes: 60

# Use term-year; the homepage creates and orders semester tables automatically.
semester: fall-2026

# Placeholder speaker image shown on the website.
# Replace this path when a real headshot arrives.
speaker_image: /assets/images/kyri_2021_th.jpg

# Public Zoom access: fill in ONE field, or leave both blank.
# Registration is the recommended default for a public, high-attendance event.
registration_url:
join_url: https://yale.zoom.us/j/95869356620

# Add the YouTube recording after the talk; leave blank beforehand.
recording_url: https://www.youtube.com/watch?v=6p3MO6OGg1w&t=229s

# Usually keep scheduled. Use cancelled/postponed only for a public notice.
# Delete or reschedule the file instead when no public label is wanted.
status: scheduled

# Keep every line of the abstract indented by two spaces.
abstract: >-
    In this talk, we address the popular topic of neural surrogates for learning solutions to AC optimal power flow (OPF) problems. If the AC OPF solution mapping from loads to optimal solutions contains a discontinuity, or if a network is trained on purely locally optimal solutions (or in an unsupervised/self-supervised manner), a strictly positive lower bound on the approximation error of the neural network exists. We illustrate this issue on small networks and introduce the concept of constrained learning for AC OPF to help diagnose and understand whether or not the source of model error is arising from a lack of model capacity or from a fundamental property of the chosen network/problem. These results have implications for the ability of neural surrogates for grid optimization problems to achieve high-quality predictions at all possible grid states.

# Keep every line of the biography indented by two spaces.
bio: >-
  Dr. Kyri Baker received her B.S., M.S., and Ph.D. in Electrical and Computer Engineering from Carnegie Mellon University in 2009, 2010, and 2014, respectively. From 2015 to 2017, she worked at the National Renewable Energy Laboratory. Since Fall 2017, she has been an Assistant Professor at the University of Colorado Boulder and is now an Associate Professor and a Fellow of the Renewable and Sustainable Energy Institute (RASEI). She is also a Research Scientist at Google DeepMind.

  She combats climate change by developing computational tools that leverage optimization and machine learning to operate energy systems more efficiently and reliably. Dr. Baker has received a National Science Foundation CAREER award for her work combining power system operations with machine learning, and has led an award-winning team in the Department of Energy ARPA-E Grid Optimization competition.
---
