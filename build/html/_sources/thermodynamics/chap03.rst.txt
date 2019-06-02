CHAPTER 3. - IDEAL GAS AND SPECIFIC HEATS
=========================================

.. meta::
  :description: This chapter introduces the ideal gas equation of state and specific heats. The concept of specific heat at constant volume and specific heat at constant pressure are defined. The relationship between the two specific heats is developed for ideal gas. The chapter also defines the concept of perfect gas which is used to further simplify the thermodynamic analysis.
  :keywords: thermodynamics, ideal gas, equation of state, specific heat, specific heat at constant volume, specific heat at constant pressure, perfect gas
  :author: Sandeep Raheja



.. |br| raw:: html

  <br>

.. index:: ideal gas

Ideal Gas
---------

Three properties of substances are measurable in nature which are :math:`P` , :math:`v` and :math:`T`. A relation (which is in the form of an equation) amongst these three state variables or properties is called an **equation of state**.

The simplest of these equations is the **ideal gas equation of state** which is experimentally found to closely approximate the behaviour of several gases at low pressures and high temperatures.   The ideal gas equation is given by


.. important:: Ideal Gas Equation of State

  .. math::

    Pv = RT

The constant in the above equation is called as the gas constant. Gas constant is given by the following relationship

.. math::

  R = \frac{R_0}{MW}

where

|br| :math:`R_0` is the universal gas constant (8314 J/kmol.K units)
|br| :math:`MW` is the molecular weight (kg/kmol) units)


.. index:: specific heat

Specific Heats (:math:`c_p` and :math:`c_v`)
--------------------------------------------

Specific heat is defined as the energy required to raise the temperature of a unit mass of substance by one degree.

The specific heat of a substance depends on the manner in which the substance is heated. In thermodynamic analysis, two types of specific heats are of interest namely, the specific heat at constant volume (:math:`c_v`)  and the specific heat at constant pressure (:math:`c_p`).

.. index:: specific heat at constant volume

Specific Heat at constant volume (:math:`c_v`)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Physically specific heat at constant volume (:math:`c_v`) is the heat required to raise the temperature when the volume is kept constant (an isochoric process)

In chapter02, the first law equation for an isochoric process was derived :eq:`first_law_closed_specific` and is reproduced here, as

.. math::

  q - w =  \varDelta u + \varDelta pe + \varDelta ke \\


Ignoring the potential and kinetic energy terms for a stationary closed system, and using the equation in differential form we have

.. math::

  \delta q - \delta w =  du

In chapter 02, the boundary work for an isochoric process was demonstrated as zero (:math:`w=0`, no displacement means no work). All the heat supplied goes to raise the internal energy of the fluid. Substituting work as zero we get

.. math::

  \delta q =  du

By definition of :math:`c_v` we have

.. math::

  \delta q =  c_v dT

By substitution we have

.. math::

  c_v dT =  du

or

.. math::

  c_v  =  \left(\frac{ \partial u}{\partial T}\right)_v


.. index:: specific heat at constant pressure

Specific Heat at constant pressure (:math:`c_p`)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In chapter 02, the equation for boundary work was derived as :eq:`first_law_isobaric`

.. math::

  W_{boundary} = P_0(\mathbb{V}_2-\mathbb{V}_1)

or on per unit mass basis as

.. math::

  w_{boundary} = P_0v_2-P_0v_1 = P_2v_2 - P_1v_1

in the above we have utilised the fact that for an isobaric process, :math:`p_0=p_1=p_2`.

Stepping back, the first law equation is restated below

.. math::

  q - w =  \varDelta u = u_2 - u_1

substituting the value of :math:`w` as boundary work for isobaric system and after rearrangment we get

.. math::

  q  &=  u_2 - u_1 + P_2v_2 - P_1v_1 \\
  q  &=  (u_2 + P_2v_2) - (u_1  + P_1v_1)

or making use of the definition of enthalpy :math:`h = u + Pv` we have

.. math::

  q  =  h_2 - h_1

In differential form the above equation can also be written as

.. math::

  dq  =  dh

By using the definition of :math:`c_p`, we can substitute :math:`dq` in the above equation and write

.. math::

  c_p dT  &=  dh \\

or,

.. math::

  c_p  =  \left(\frac{ \partial h}{\partial T}\right)_p



Specific Heat for Ideal Gas
~~~~~~~~~~~~~~~~~~~~~~~~~~~

It has been demonstrated experimentally by Joule, that the internal energy is only a function of temperature (:math:`T`) i.e.

.. math::

  u = u(T)

From enthalpy definition and ideal gas equation we have

.. math::

  h &= u + Pv \\
  Pv &= RT

therefore,

.. math::

  h = u + RT  = u(T) + RT

as the entire expression on the right hand side is a function of temperature (:math:`T`) only we can say that enthalpy is a function of temperature only.

.. math::

  h = h(T)


Since :math:`u` and :math:`h` are a function of temperature only, specific heats which are their temperature derivatives, are also a function of temperature only.


.. important:: Specific Heat behaviour for Ideal Gas

  .. math::

    u &= u(T) \\
    h &= h(T) \\

  and

  .. math::

    du &= c_v(T)dT \\
    dh &= c_p(T)dT


.. index:: perfect gas

Perfect Gas
-----------

In thermodynamic analysis many property and heat, work evaluations require that the function :math:`C_p(T)` and :math:`C_v(T)` be known. The analysis becomes very simple, if we assume that during the process the specific heats remain constant.  When such an assumption is made about the gas, the gas is called as a *calorically perfect gas* or simply *perfect gas*.

While there might be some variation in the values of specific heats, but assuming that they are constant at an average value during the process, the loss of accuracy incurred due to this assumtion is found to be fairly acceptable in most circumstances.


.. important:: For a Perfect Gas

  .. math::

    c_p &= constant \\
    c_v &= constant
