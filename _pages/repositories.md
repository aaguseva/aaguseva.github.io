---
layout: page
permalink: /repositories/
title: codes
description: 
nav: true
nav_order: 4
---

**If you would like to use these codes, please contact me via anna.guseva at obspm.fr**

### Magnetohydrodynamic Taylor-Couette flow code

MPI-parallelized code solving coupled Navier-Stokes and induction equations for a flow between two rotating cylinders, developed in collaboration with A.P. Willis (U. Sheffield, UK). The code has spectral discretization in the axial and azimuthal directions, and the radial coordinate is discretized using finite differences. The nonlinear terms are evaluated in the physical space and are de-aliased using the 3/2 rule; more details of the numerical method can be found in {% cite guseva2015transition %}. The code showed excellent scalability in high-performance computing centers (Jülich Supercomputing Centre), and allowed to model low-resistivity fluids, unachievable numerically before; see {% cite guseva2016azimuthal %} {% cite gellert2016nonaxisymmetric %} {% cite guseva2017dynamo %} {% cite guseva2017transport %} {% cite mamatsashvili2018quasi %} {% cite guseva2023transition %} for works using this code.


### Channel flow code with control

MPI-parallelized high-performance code for channel flow in Fortran 90, building upon an older formulation by Flores and Jimenez (2006), with the opposition control strategy. The code solves coupled equations for vorticity and wall-normal velocity using pseudo-spectral direct numerical simulations. The opposition control strategy is implemented as a proportionality between the boundary conditions on velocity at the wall and velocity at a given location above it. See {% cite guseva2022linear %} for more details.

{% if site.data.repositories.github_repos %}

### GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}

