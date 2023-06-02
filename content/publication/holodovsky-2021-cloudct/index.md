---
# Documentation: https://wowchemy.com/docs/managing-content/

title: CloudCT 3D volumetric tomography-mission advances
subtitle: ''
summary: ''
authors:
- Masada Tzabari
- Vadim Holodovsky
- admin
- Eshkol Eitan
- Orit Altaratz
- Ilan Koren
- Anna Aumann
- Klaus Schilling
- Yoav Schechner
tags: 
  - CloudCT
categories: [CloudCT]
date: '2021-01-01'
lastmod: 2023-06-02T20:08:13+03:00
featured: true
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: 
  - CloudCT
publishDate: '2023-06-02T17:07:57.487681Z'
publication_types:
- '1'
abstract: 'Significant climate uncertainties are associated with insufficient understanding of small warm clouds, due to the nature of their 3D structure and radiative transfer. It is desirable to improve understanding of such clouds and their sensitivity to environmental changes. This requires sensing platforms that are suitable for 3D sensing, and signal analysis tuned to 3D radiative transfer. We approach these challenges in the CloudCT project, funded by the ERC. It is a mission that develops and aims to demonstrate 3D volumetric scattering tomography of clouds. This will be facilitated by an unprecedented large formation of ten cooperating nanosatellites. The formation will simultaneously image cloud fields from multiple directions, at approximately 20m nadir ground resolution. Based on this data, scattering tomography will seek the 3D volumetric distribution of droplet effective radius, liquid water content and optical extinction. In addition to advancement of the technology, CloudCT will yield a global database of 3D macro and microphysical properties of warm cloud fields.

In this talk, we present advances made on several fronts of the project: modeling, payload, algorithm, and operation. Regarding cloud modeling, we performed LES simulations (using the SAM model with bin microphysics) of warm convective cloud fields (at different environments), at high spatial resolution. Using the simulated clouds properties, several imager and waveband possibilities have been quantitatively considered for the mission. Major consideration criteria are tomographic quality in the face of sensor and photon noise, calibration errors and stray light. Additional criteria are technological availability, platform constraints, calibration requirements and cost.

We investigated specifically possibilities of visible light (VIS, 463nm, 545nm, 645nm, and 705nm) short wave infra-red (SWIR, 1641 nm), and polarized imagers (POL, 463nm, 545nm, 645nm, and 705nm).  These examinations relied on physical modeling of 3D radiative transfer and the sensing processes. Due to platform constraints in CloudCT, each platform will carry a single camera exclusively (either VIS/NIR or SWIR). Hence, we describe the tradeoff of introducing SWIR cameras and various POL architectures.  

While CloudCT is mainly designed for simultaneous imaging of each cloud field, it is possible to tolerate a lag of several seconds, as small warm clouds hardly evolve in this time scale (at the 20 meter spatial scale). We exploit this, to add more view-points, using the same number of platforms (10). The added viewpoints correspond to single-scattering angles, where polarization yields enhanced sensitivity to the droplet microphysics. These angles require sampling of <1° in the fogbow region. This dictates requirements for the platform attitude control.  

On the algorithmic front, we advanced the retrieval to yield results that (compared to the simulated ground truth) have smaller errors than the prior art. Elements of our advancement include initialization by a parametric horizontally-uniform microphysical model. The parameters of this initialization are determined by a fast optimization process.  The optimized initialization is particularly strong, when relying on the detected degree of linear polarization, instead of radiance.'
DOI: '10.5194/egusphere-egu21-9585'
publication: '*EGU General Assembly Conference Abstracts*'
---
