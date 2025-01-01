---
layout: page
permalink: /repositories/
title: codes
description: 
nav: true
nav_order: 4
---

## Taylor-Couette flow code

MPI-parallellized code solving coupled Navier-Stokes and induction equations for a flow between two rotating cylinders. The code has spectral discretization in the axial and azimuthal directions, and the radial coordinate is discretized using finite differences. The nonlinear terms are evaluated in the physical space and are de-aliased using the 3/2 rule; more details of the numerical method can be found in {% cite guseva2015transition %}. The code showed excellent scalability in high-performance computing centers (Jülich Supercomputing Centre), and allowed to model low-resistivity fluids, unachievable numerically before; see {% cite guseva2016azimuthal} {% cite gellert2016nonaxisymmetric} {% cite guseva2017dynamo} {% cite guseva2017transport} {% cite mamatsashvili2018quasi} {% cite guseva2023transition} for works using this code.


## Channel flow code with control

MPI-parallellized code solving coupled Navier-Stokes and induction equations for a flow between two rotating cylinders. The code has spectral discretization in the axial and azimuthal directions, and the radial coordinate is discretized using finite differences. The nonlinear terms are evaluated in the physical space and are de-aliased using the 3/2 rule; more details of the numerical method can be found in {% cite guseva2015transition %}. 


{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
