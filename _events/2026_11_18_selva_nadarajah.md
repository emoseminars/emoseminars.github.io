---
# Replace the TBA values as speaker details become available.
# Keep text values quoted so punctuation remains valid YAML.
title: "Learning-Augmented Power System Expansion Planning Beyond Capacity Credits (rescheduled from October 21)"
speaker: "Selva Nadarajah"
affiliation: "University of Illinois at Chicago"

# Optional personal or institutional profile.
speaker_url: https://www.selva-nadarajah.com

# Change these fields if this talk is rescheduled or shortened.
# America/New_York supplies EST/EDT automatically; do not add a UTC offset.
talk_date: "2026-11-18"
start_time: "3:00 PM"
duration_minutes: 60

# Use term-year; the homepage creates and orders semester tables automatically.
semester: fall-2026

# Placeholder speaker image shown on the website.
# Replace this path when a real headshot arrives.
speaker_image: /assets/images/selva_nadarajah.jpg

# Public Zoom access: fill in ONE field, or leave both blank.
# Registration is the recommended default for a public, high-attendance event.
registration_url:
join_url: https://yale.zoom.us/j/91931480042

# Add the YouTube recording after the talk; leave blank beforehand.
recording_url:

# Usually keep scheduled. Use cancelled/postponed only for a public notice.
# Delete or reschedule the file instead when no public label is wanted.
status: scheduled

# Keep every line of the abstract indented by two spaces.
abstract: >-
  Utilities and grid operators plan generation and transmission investments years ahead with optimization models that represent reliability through a reserve margin and fixed capacity credits. These credits act as a linear approximation of reliability, computed once for each technology, so they cannot distinguish where capacity is built or how it is connected. Plans with the same accredited margin can therefore differ substantially in simulated reliability, and planners may pay more than necessary to meet a standard. We address this gap by learning a reliability surrogate from adequacy simulations of reserve margin plans. The surrogate is a convex piecewise linear function of nodal generation, storage, and transmission capacities, built from random ReLU features. It embeds exactly in the mixed integer planning model and comes with approximation guarantees. Because the space of plans is combinatorial and each simulation is expensive, we optimize within trust regions around evaluated plans, with ensemble predictions guarding against extrapolation. On benchmark systems, the resulting plans meet reliability standards at lower annual cost than plans based on capacity credits, through different choices of investment mix, siting, and transmission. We discuss implications for capacity accreditation and planning practice. 

# Keep every line of the biography indented by two spaces.
bio: >-
  Selvaprabu (“Selva”) Nadarajah is Professor and Head of Information and Decision Sciences at the University of Illinois Chicago College of Business Administration, where he is the Bielinski Family Faculty Scholar and UIC Global Scholar. His research sits at the intersection of operations research and finance, developing methods for energy investment and operating decisions under uncertainty, including generation and transmission planning, merchant energy trading, and renewable procurement. His current work centers on the computing and energy nexus, including grid reliability under AI driven load growth, data center siting, and the resource constraints these create. He is an affiliate of the Institute of Government and Public Affairs and previously served as Decision Intelligence R&D lead at the Discovery Partners Institute, the innovation hub of the University of Illinois System. His work has appeared in leading journals including Operations Research and Management Science, and he serves as an Associate Editor at Operations Research, Production and Operations Management, and Decision Sciences. His research has been recognized with the 2024 INFORMS Harvey J. Greenberg Award for Computing and Operations Research, the 2021 Best Paper Award from the Commodity and Energy Markets Association, the Best Overall Paper Award at the 2020 NeurIPS Workshop on Tackling Climate Change with Machine Learning, and the 2020 INFORMS ENRE Young Researcher Prize.
---
