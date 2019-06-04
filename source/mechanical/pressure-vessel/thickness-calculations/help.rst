.. meta::
  :title: Pressure Vessel Thickness/MAWP Calculation - Reference
  :description: Help/Reference for the thickness/MAWP, volume and weight estimation of pressure vessels. The thickness and MAWP are calculated based on the internal design pressures as per ASME Section VIII Div-1 requirements.
  :keywords: pressure vessel thickness MAWP volume weight calculation ASME
  :author: Sandeep Raheja


=====================================
Pressure Vessel Thickness Calculation
=====================================

.. figure:: vessel.jpg
  :scale: 70 %
  :alt: pressure vessel


.. |br| raw:: html

  <br>

Design Formulas
---------------

Minimum thickness requirement (UG-16)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The minimum thickness requirement of any pressure retaining component (excluding corrosion allowance) is 1.5 mm in accordance with the provisions of UG-16 i.e.

.. math::
  :label: minimum-thickness

  t_u = 1.5 mm

Thickness, MAWP and Volume of Cylindrical Shells
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: cylinder.png
  :scale: 70 %
  :alt: Cylindrical Shell

**Thickness**

The thickness required (:math:`t_c`) to handle circumferential stress arising due to internal pressure (:math:`P_i`) is given as:


If :math:`P_i \leq 0.385SE`, using **UG-27(1)**

.. math::
  :label: UG-27(1)

  t_c = \frac{P_iR}{SE-0.6P_i}

else if :math:`P_i > 0.385SE`, using **Appendix 1-2(1)**

.. math::
  :label: app-1-2(1)

  t_c = R\left(e^{\frac{P_i}{SE}}-1\right)


The thickness required (:math:`t_l`) to handle longitudinal stress arising due to internal pressure (:math:`P_i`) is given as:

If :math:`P_i \leq 1.25SE`, using **UG-27(2)**

.. math::
  :label: UG-27(2)

  t_l =  \frac{P_iR}{2SE+0.4P_i}

else if :math:`P_i > 1.25SE`, using **Appendix 1-2(3)**

.. math::
  :label: app-1-2(3)

  t_l = R\left(\sqrt{Z} - 1\right)

where,

.. math::

  Z = \left( \frac{P_i}{SE} + 1\right)


The shell thickness excluding corrosion allowance (:math:`t`) is the highest of the thickness amongst :math:`t_c`, :math:`t_l`, :math:`t_u`:

.. math::

  t = max(t_c, t_l, t_u)


**MAWP**


The MAWP for the available thickness is determined for circumferential stress (:math:`MAWP_c`) as:

If :math:`t \leq \frac{R}{2}`, using **UG-27(1)**

.. math::
  :label: P-UG-27(1)

  MAWP_c = \frac{SEt}{R + 0.6t}

else if :math:`t > \frac{R}{2}`, using **Appendix 1-2(2)**

.. math::
  :label: app-1-2(2)

  MAWP_c = SElog_e\left(\frac{R + t}{R}\right)


The MAWP for the available thickness is determined for longitudinal stress (:math:`MAWP_l`) as:

If :math:`t \leq \frac{R}{2}`, using **UG-27(2)**

.. math::
  :label: P-UG-27(2)

  MAWP_l =  \frac{2SEt}{R-0.4t}

else if :math:`t > \frac{R}{2}`, using **Appendix 1-2(4)**

.. math::
  :label: app-1-2(4)

  MAWP_l = SE\left(Z-1\right)

where,

.. math::

  Z = \left( \frac{R+t}{R}\right)^2

The shell MAWP (:math:`MAWP`) is the lowest of the MAWP amongst :math:`MAWP_c` and :math:`MAWP_l`:

.. math::

  MAWP = min(MAWP_c, MAWP_l)


**Volume**

The inner volume (:math:`V`) of a cylindrical shell is obtained from the following:

.. math::

  V = \pi R^2 S

The volume of steel (:math:`V_m`) for weight computation is obtained from the following:

.. math::

  V_m = \pi S (R_o^2 -R^2)


Thickness, MAWP and Volume of Spherical Shells
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: sphere.png
  :scale: 70 %
  :alt: Spherical Shell

**Thickness**

If :math:`P_i \leq 0.665SE`, using **UG-27(3)**

.. math::
  :label: UG-27(3)

  t =  \frac{P_iR}{2SE-0.2P_i}

else if :math:`P_i > 0.665SE`, using **Appendix 1-3(1)**

.. math::
  :label: app-1-3(1)

  t = R\left(e^{\left[\frac{0.5P_i}{SE}\right]} - 1\right)


**MAWP**

If :math:`t \leq 0.356R`, using **UG-27(3)**

.. math::
  :label: P-UG-27(3)

  MAWP =  \frac{2SEt}{R-0.4t}

else if :math:`t > 0.356R`, using **Appendix 1-3(2)**

.. math::
  :label: app-1-3(2)

  MAWP = 2SElog_e\left( \frac{R+t}{R} \right)

**Volume**

The inner volume (:math:`V`) of a spherical shell is obtained from the following:

.. math::

  V = \frac{4}{3}\pi R^3

The volume of steel (:math:`V_m`) for weight computation is obtained from the following:

.. math::

  V_m = \frac{4}{3}\pi \left(R_o^3 - R^3\right)

Thickness, MAWP and Volume of Ellipsoidal Head
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: ellipsoidal.png
  :scale: 50 %
  :alt: Ellipsoidal Head

For an ellipsoidal head the aspect ratio (:math:`\beta`) is defined as:

.. math::
  :label: beta_from_h

  \beta = \frac{D}{2h}

where:

:math:`h` is the inner height of the head
|br| :math:`D` is the inner diameter of the head skirt

this can be used to determine the inner height (:math:`h`) of the ellipsoid when the aspect ratio (:math:`\beta`) is known:

.. math::
  :label: h_from_beta

  h = \frac{D}{2\beta} \\

Factor (K) for ellipsoid is obtained as:

.. math::
  :label: ellipsoid_K

  K = \frac{1}{6}\left[2 + \beta^2 \right]

**Thickness**

Using the equation **Appendix 1-4(1)**, the thickness for ellipsoidal head is given as:

.. math::
  :label: ellipsoidal_head_thickness

  t = \frac{P_iDK}{2SE - 0.2P_i}

**MAWP**

Using the equation **Appendix 1-4(1)**, the MAWP for ellipsoidal head is given as:

.. math::

  MAWP = \frac{2SEt}{KD + 0.2t}

**Volume**

The inner volume (:math:`V`) of an ellipsoidal head is obtained from the following:

.. math::

  V = \frac{2}{3}\pi R^2h

The volume of steel (:math:`V_m`) for weight computation is obtained from the following:

.. math::

  V_m = \frac{2}{3}\pi \left(R_o^2h_o - R^2h\right)

where :

:math:`R=\frac{D}{2}`
|br| :math:`R_o=R+t`
|br| :math:`h_o=h+t`

Thickness, MAWP and Volume of Torispherical Head
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: torispherical.png
  :scale: 50 %
  :alt: Torispherical Head

The following relationships are applicable:

Outer Diameter :math:`D_o=D+2t`
|br| Outer Crown Radius :math:`L_o=L+t`
|br| Outer knuckle radius :math:`r_o=r+t`

Factor M for the torispherical head is obtained as:

.. math::

  M = \frac{1}{4}\left( 3 + \sqrt{\frac{L}{r}}\right)

where :

:math:`L` is the inner crown radius as shown in figure above
|br| :math:`r` is the knuckle radius as shown in figure above

**Thickness**


Using the equation **Appendix 1-4(3)**, the thickness for torispherical head is given as:

.. math::
  :label: app-1-4(3)

  t = \frac{P_iLM}{2SE - 0.2P_i}



**MAWP**

Using the equation **Appendix 1-4(3)**, the MAWP for torispherical head is given as:

.. math::
  :label: P-app-1-4(3)

  MAWP = \frac{2SEt}{LM + 0.2t}


**Volume**

The inner volume of the torispherical head is given by:

.. math::

  V = V(D,L,R) = \frac{\pi}{3} \left[ 2hL^2 - (2r^2 + c^2 + 2rL)(L-h) + 3r^2c sin^{-1} \left(\frac{L -h}{L - r} \right) \right]

where :

:math:`c = \frac{D}{2} - r`
|br| :math:`h = L - \sqrt{(r + c - L)(r - c - L)}`

The volume of steel (:math:`V_m`) for weight computation is obtained by the subtracting the inner volume of the toridome from the outer volume of the toridome:

.. math::

  V_m = V(D_o, L_o, r_o) - V(D, L, r)



Thickness, MAWP and Volume of Hemispherical Head
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: hemispherical.png
  :scale: 50 %
  :alt: Hemispherical Head

The following relationships are applicable:

Inner Radius :math:`R=\frac{D}{2}`
|br| Outer Radius :math:`R_o=R+t`

**Thickness**

If :math:`P_i \leq 0.665SE`, using **UG-27(3)**

.. math::

  t =  \frac{P_iR}{2SE-0.2P_i}

else if :math:`P_i > 0.665SE`, using **Appendix 1-3(1)**

.. math::

  t = R\left(e^{\left[\frac{0.5P_i}{SE}\right]} - 1\right)


**MAWP**

If :math:`t \leq 0.356R`, using **UG-27(3)**

.. math::

  MAWP =  \frac{2SEt}{R-0.4t}

else if :math:`t > 0.356R`, using **Appendix 1-3(2)**

.. math::

  MAWP = 2SElog_e\left( \frac{R+t}{R} \right)

**Volume**

The inner volume (:math:`V`) of a hemispherical shell is obtained from the following:

.. math::

  V = \frac{2}{3}\pi R^3

The volume of steel (:math:`V_m`) for weight computation is obtained from the following:

.. math::

  V_m = \frac{2}{3}\pi \left(R_o^3 - R^3\right)


Thickness, MAWP and Volume of Conical Head
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: conical.png
  :scale: 50 %
  :alt: Conical Head


The following relationships are applicable:

Inner radius :math:`R=\frac{D}{2}`
|br| Outer radius :math:`R_o=\frac{D + 2t}{2}`
|br| Inner height :math:`h = \frac{D}{2 tan\alpha}`
|br| Outer height :math:`h_o = h + t`


**Thickness**

For semi apex angle, :math:`\alpha` not exceeding 30 degrees, the thickness and MAWP are obtained using the following formulas.

The thickness for conical head is obtained as :

.. math::
  :label: app-1-4(5)

  t = \frac{P_iD}{2cos \alpha \left(SE - 0.6P_i\right)}


**MAWP**

The MAWP for conical head is obtained as :

.. math::
  :label: P-app-1-4(5)

  MAWP = \frac{2SEtcos \alpha}{D + 1.2tcos \alpha}


**Volume**

The inner volume (:math:`V`) of a conical head is obtained from the following:

.. math::

  V = \frac{2}{3}\pi R^2h

The volume of steel (:math:`V_m`) for weight computation is obtained from the following:

.. math::

  V_m = \frac{4}{3}\pi \left(R_o^2h_o - R^2h\right)



Thickness, MAWP and Volume of Toriconical Head
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: toriconical.png
  :scale: 50 %
  :alt: Toriconical Head

The following relationships are applicable:

the inside diameter of the conical portion :math:`D_i = D - 2r(1- cos \alpha)`
|br| the inner crown radius :math:`L = \frac{D_i}{2cos \alpha}`

**Thickness**

The thickness  of the knuckle portion (:math:`t_{knuckle}`) can be obtained using Appendix 1-4(3) as given in :eq:`app-1-4(3)` above.

The thickness of the conical portion (:math:`t_{cone}`)can be obtained using Appendix 1-4(5) as given in :eq:`app-1-4(5)`.

The thickness of the toricone is obtained as:

.. math::

  t = max(t_{knuckle}, t_{cone} )


**MAWP**

The MAWP of the knuckle portion (:math:`MAWP_{knuckle}`) can be obtained using Appendix 1-4(3) as given in :eq:`P-app-1-4(3)` above.

The MAWP of the conical portion (:math:`MAWP_{cone}`) can be obtained using Appendix 1-4(5) as given in :eq:`P-app-1-4(5)` above.

The MAWP of the toricone is obtained as the minimum of the two.

.. math::

  MAWP = min(MAWP_{knuckle}, MAWP_{cone} )


**Volume**

Presently the program estimates the volume of the toricone, with a cone so the equations given in conical head sections apply. In future this may change by making use of more accurate relationships.



Calculation Procedure
---------------------

**Shell Evaluation**

*Step -1 :* : Determine the unknown dimensions of the vessel shell from the dimensions as provided.

If the user has provided outer diameter (:math:`D_o`) of the vessel then the inner diameter (:math:`D`) can be obtained as :

.. math::

  D = D_o - 2t_n

If the user has provided inner diameter (:math:`D`) of the vessel then the outer diameter (:math:`D_o`) can be obtained as :

.. math::

  D_o = D + 2t_n

The inner (:math:`R`) and outer (:math:`R_o`) radius of the shell  can be determined as:

.. math::

  R &= \frac{D}{2} \\
  R_o &= \frac{D_o}{2} \\

*Step -2 :* Establish the dimensions under corroded conditions. The dimensions as used in the formulas shall be considered after considering the removal of material on account of corrosion. This implies adding the specified corrosion allowance on the inner dimensions which are exposed to the fluid and deducting the corrosion allowance from the nominal thickness provided. Thus,

.. math::

  D_{cor} &= D + 2ca \\
  R_{cor} &= R + ca \\
  t_{cor} &= t_n - ca

*Step -3 :* Based on the value of internal design temperature lookup and interpolate the allowable stress of the specified material as furnished in ASME-II Part D.

*Step -4 :* Establish the minimum thickness of any component required to meet the requirement of UG-16 as below.

.. math::

  t_u = 1.5mm

*Step -5 :* Calculate the thickness of the shell based on the internal design pressure i.e. :math:`t_c` and :math:`t_l` for cylinder and :math:`t_{sph}` for sphere.

For cylindrical shell the thickness (:math:`t`) shall be the maximum amongst :math:`t_c`, :math:`t_l` and :math:`t_u` i.e.

.. math::

  t = max(t_c, t_l, t_u)

For spherical shell the thickness (:math:`t`) shall be the maximum amongst :math:`t_{sph}` and :math:`t_u` i.e.

.. math::

  t = max(t_{sph}, t_u)


*Step -5 :* Calculate the required thickness of the shell (:math:`t_r`) of the vessel shell after adding the corrosion allowance i.e. :

.. math::

  t_r = t + ca

The provided shell thickness (:math:`t_n`) is adequate if the provided nominal thickness exceeds the required thickness (:math:`t_r`):

.. math::

  t_n \geq t_r

*Step -6 :* Calculate the MAWP of the shell using the design formulas as applicabe for the shell Shape (cylindrical or spherical) with the inner shell dimensions under corroded conditions. The thickness available (:math:`t_{cor}`) under corroded conditions shall be used for the purpose of MAWP calculation.


**Head Evaluation**

*Step -7 :* : Determine the dimensions of the head.

It is assumed that the inner dimension of the head skirt is the same as the inner dimension of the cylindrical shell. Thus, :math:`D_1 = D_2 = D` and  :math:`R_1 = R_2 = \frac{D}{2}`.

The outer diameters of the head are obtained as:

.. math::

  D_{o1} &= D_1 + 2t_{n1} \\
  D_{o2} &= D_2 + 2t_{n2} \\

The outer radiuses of the head are obtained as:

.. math::

  R_{o1} &= \frac{D_{o1}}{2}  \\
  R_{o2} &= \frac{D_{o2}}{2}  \\


*Step -8 :* Determine the dimensions of the head in corroded conditions.

.. math::

  D_{cor1} &= D_1 + 2ca \\
  R_{cor1} &= R_1 + ca \\
  h_{cor1} &= h_1 + ca \\
  L_{cor1} &= L_1 + ca \\
  r_{cor1} &= r_1 + ca \\
  t_{cor1} &= t_{n1} - ca \\

The relationship for head 2 are identical to the above.

*Step -9 :* Calculate the thickness of Head 1 (:math:`t_{h1}`) and Head 2 ( :math:`t_{h2}`) for the internal design pressure based on the relevant formula as applicable to the head shape. The calculated thickness of the head shall be obtained by application of the provisions of UG-16 for minimum thickness i.e.

.. math::

  t_1 &= max(t_{h1}, t_u) \\
  t_2 &= max(t_{h2}, t_u) \\

*Step -10 :* The required thickness of the heads (:math:`t_{r1}` and :math:`t_{r2}`) is obtained by adding the corrosion allowance to the calculated thickness.

.. math::

  t_{r1} &= t_1 + ca \\
  t_{r2} &= t_2 + ca \\

The provided head thickness (:math:`t_{n1}` / :math:`t_{n2}`  ) is adequate if it exceeds the required thickness (:math:`t_{r1}`/:math:`t_{r2}`):

.. math::

  t_{n1} &\geq t_{r1} \\
  t_{n2} &\geq t_{r2} \\

*Step -11 :* Calculate the MAWP of Head-1 (:math:`MAWP_1`) and Head-2 (:math:`MAWP_2`) using the design formulas as applicabe for the head shape (ellipsoidal, torispherical, hemispherical, conical or toriconical) with head inner dimensions under corroded conditions. The thickness available (:math:`t_{cor1}`/:math:`t_{cor2}`) under corroded conditions shall be used for the purpose of MAWP calculation.

**Overall MAWP and Hydrotest Pressure**

*Step -12 :* Determine the overall MAWP of the vessel which is the least amongst the MAWP as determined for the shell and the heads.

.. math::

  MAWP = min(MAWP_{sh}, MAWP_1, MAWP_2)

*Step -13 :* Determine the hydrotest pressure requirements as per the provisions of UG-99 (b).

.. math::

  P_t = 1.3MAWP(\frac{S_t}{S})

where :

:math:`S_t` is the allowable stress of the material at hydrotest temperatures.

**Volumes and Weights**

*Step -14 :* : Determine the inner volume of the shell (:math:`V_{sh}`), Head-1 (:math:`V_{1}`) and Head-2 (:math:`V_{2}`) using the formulas as applicable to the geometry.

The volume of the vessel (:math:`V`) is obtained as:

.. math::

  V = V_{sh} + V_{1} + V_{2}

*Step -15 :* : Determine the material volume (steel volume) of the shell (:math:`V_{msh}`), Head-1 (:math:`V_{m1}`) and Head-2 (:math:`V_{m2}`) using the formulas as applicable to the geometry. Knowing the density of steel (:math:`\rho_{steel}`) the fabricated weight of the shell(:math:`W_{sh}`), Head-1 (:math:`W_{1}`) and Head-2 (:math:`W_{w2}`) can be obtained as:

.. math::

  W_{sh} &= \rho_{steel}*V_{msh} \\
  W_{1} &= \rho_{steel}*V_{m1} \\
  W_{2} &= \rho_{steel}*V_{m2} \\

The fabrication weight of the vessel is obtained as:

.. math::

  W = W_{sh} +  W_{1} + W_{2}

Knowing the markup weight as a percent (:math:`\zeta`) for additional items like vessel supports, nozzles etc. the gross fabrication weight of the vessel is obtained as:

.. math::

  W_{gross} = W(1 + \frac{\zeta}{100})

Knowing the density of water (:math:`\rho_{water}`) the hydrotest weight of the vessel (:math:`W_t`) is obtained as:

.. math::

  W_t = W_{gross} + \rho_{water}V
