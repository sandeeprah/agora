CHAPTER 2. - FIRST LAW OF THERMODYNAMICS
========================================

.. meta::
  :description: This chapter applies the principle of energy conservation to closed and open systems. The first law of thermodynamics is introduced as a relation between heat transfered, work done and change in the  energy content of the system. For a closed system the concept of work is expanded to include boundary work Pdv. For an open system, the concept of flow energy Pv and enthalpy is introduced. The principle of first law is applied to isochoric, isobaric, isothermal, isentropic and polytropic processes for a closed system. First law equation is also applied to open system devices like nozzles, diffusers, compressors, turbines, mixing chambers and throttling devices.

  :keywords: thermodynamics, closed system, open system, boundary work, flow energy, enthalpy, isochoric, isobaric, isothermal, isentropic, polytropic, nozzle, diffuser, compressor, turbine, mixing, throttling

  :author: Sandeep Raheja

While analysing any thermodynamic system, the universal principles of conservation of mass and energy must stand demonstrated in the mathematical model. The method to mathematically invoke these principles in analysis is presented in the sections below under *mass balance principle* and *energy balance principle*.



Mass Balance Principle
----------------------

.. index:: mass balance principle

The principle of mass balance (which follows from the law of conservation of energy) can be stated as:

.. math::
  :label: mass_balance

  m_{in}- m_{out}=\varDelta m_{system}

where,
|br|:math:`m_{in}` is mass going in to the system
|br|:math:`m_{out}` is mass going out of the system
|br|:math:`\varDelta m_{system}` is the change in mass of the system.


In time rate form this can be written as:

.. math::
  :label: mass_balance_timerate

  \dot{m}_{in} - \dot{m}_{out}=\dot{m}_{system}

Under steady state conditions :math:`\dot{m}_{system}=0`, hence

.. math::
  :label: mass_balance_steady

  \dot{m}_{in} = \dot{m}_{out}

For a single stream moving in and a single stream moving out, we have:

.. math::
  :label: mass_balance_steady_single_stream

  \dot{m}_1 &= \dot{m}_2 \\

where subscript :math:`1` denotes the inlet stream and subscript :math:`2` denotes outlet stream.

Making use of the relationship :math:`\dot{m}=\rho\dot{\mathbb{V}}=\rho VA` , where :math:`\dot{\mathbb{V}}` is the volumetric flow rate, :math:`\rho` is density, :math:`V` is fluid velocity and :math:`A` is the fluid flow area we can write the mass balance equation :eq:`mass_balance_steady_single_stream` as:

.. math::
  :label: mass_balance_steady_compressible

  \rho_1V_1A_1 &= \rho_2V_2A_2 \\

For incompressible flows, the density at inlet (:math:`\rho_1`) and outlet (:math:`\rho_2`) are the same and so the mass balance equation can be simplified to:

.. math::
  :label: mass_balance_steady_incompressible

  V_1A_1 = V_2A_2


Energy Balance Principle
------------------------

.. index:: energy balance principle


The principle of energy balance (which follows from the law of conservation of energy) can be stated as:

.. math::
  :label: energy_balance

  E_{in} - E_{out}=\varDelta E_{system}

.. |br| raw:: html

  <br>

where,
|br|:math:`E_{in}` is energy going in to the system
|br|:math:`E_{out}` is energy going out of the system
|br|:math:`\varDelta E_{system}` is the change in energy of the system.

In time rate form this can be written as:

.. math::
  :label: energy_balance_timerate

  \dot{E}_{in} - \dot{E}_{out}=\dot{E}_{system}

Under steady state conditions :math:`\dot{E}_{system}=0`, hence

.. math::
  :label: energy_balance_steady

  \dot{E}_{in} = \dot{E}_{out}



.. index:: first law for closed system

First Law Analysis for  Closed Systems
--------------------------------------

Energy Balance for Closed Systems
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the case of closed system no mass enters or leaves the system. However, mass balance principle which applies can still be evoked for the sake of mathematical rigour.

.. math::
  :label: mass_balance_closed_system

  \varDelta m = m_{in} - m_{out}= 0 - 0 = 0

The energy balance principle as given in equation :eq:`energy_balance` can be invoked in thermodynamic context of a closed system with :math:`E_{in}`, :math:`E_{out}` and :math:`\varDelta E_{system}` as given below:

.. math::

  E_{in} &= Q_{in} + W_{in} \\
  E_{out} &= Q_{out} + W_{out} \\
  \varDelta E_{system} &= \varDelta U + \varDelta PE + \varDelta KE

where,

:math:`Q_{in}` is heat going in to the system
|br| :math:`Q_{out}` is heat going out of the system
|br| :math:`W_{in}` is work done on the system
|br| :math:`W_{out}` is work done by the system
|br| :math:`\varDelta U` is the change in internal energy of system
|br| :math:`\varDelta PE` is the change in potential energy of system
|br| :math:`\varDelta KE` is the change in kinetic energy of system


Upon substitution in energy balance equation :eq:`energy_balance`, we have,

.. math::
  :label: energy_balance_closed_system

  (Q_{in} + W_{in}) - (Q_{out} + W_{out}) &= \varDelta U + \varDelta PE + \varDelta KE \\
  (Q_{in} - Q_{out}) - (W_{out} - W_{in}) &= \varDelta U + \varDelta PE + \varDelta KE

To further simplify the above, let us use the expressions of net heat (:math:`Q`) moving in to the system  and net work (:math:`W`) done by the system i.e. :

.. math::

  Q &= Q_{in} - Q_{out}\\
  W &= W_{out} - W_{in}

Substituting in :eq:`energy_balance_closed_system` we get the first law equation of thermodynamics for closed system i.e.


.. math::
  :label: first_law_closed_system

  Q - W = \varDelta U + \varDelta PE + \varDelta KE \\

For the typical case of a stationary closed system, the potential and kinetic energy terms can be set to zero. So, *First Law in stationary form* can be written as:

.. important:: First Law equation for closed systems

  .. math::
    :label: first_law_closed_system_stationary

    Q - W = \varDelta U

*First Law in differential form*  can be written as:

.. math::
  :label: first_law_closed_differential

  \delta Q-\delta W  = dU + dPE + dKE

*First Law in time rate form* can be written as:

.. math::
  :label: first_law_closed_timerate

  \dot{Q}-\dot{W} = \frac{dU}{dt} + \frac{dPE}{dt} + \frac{dKE}{dt}


Dividing by mass :math:`m` we get *First Law in specific quantity form* as:

.. math::
  :label: first_law_closed_specific

  q - w =  \varDelta u + \varDelta pe + \varDelta ke \\


Concept of Boundary Work
~~~~~~~~~~~~~~~~~~~~~~~~

In the context of closed system, we need to expand our idea of work, to include a special form of work that happens when a closed system undergoes expansion or compression. This special form of work which happens because of the motion of the boundary enclosing the closed system is termed as **boundary work**. In classical mechanics the work done is described by the **mechanical work equation** as given below:

.. index:: mechanical work equation

.. math::
  :label: work_mechanical

  W_{mech} = \int_{x1}^{x2}F.dx

To exemplify a closed system let us take the example of a cylinder piston arrangement as shown in figure.

.. figure:: closed-system.png
  :scale: 50 %
  :alt: boundary work in non flow process (closed system)

The cylinder has an internal pressure (:math:`p`) and the force (:math:`F`) acting on the piston face of a given area (:math:`A`) will be :math:`F=pA`. Substituting this in the mechanical work equation :eq:`work_mechanical` we get the following:

.. math::

  W_{boundary} = \int_{x1}^{x2}PA.dx


Since :math:`dV=Adx`, on substitution in the above we get the **boundary work equation**:

.. index:: boundary work equation

.. math::
  :label: boundary_work

  W_{boundary} = \int_{\mathbb{V}_1}^{\mathbb{V}_2}Pd\mathbb{V}

First Law Equation (Boundary Work Form)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

There may be several types of work interactions acting on a closed system. Boundary work is just one of the various work interactions for the system. So in general terms,

.. math::

  W = W_{other} + W_{boundary}

Having developed the expression of boundary work as applicable to closed system :eq:`boundary_work`, the first law equation :eq:`first_law_closed_system` upon substitution of :math:`W` gives the following equation:

.. math::
  :label: first_law_closed_rigorous

  Q- W_{other} -  \int_{\mathbb{V}_1}^{\mathbb{V}_2}Pd\mathbb{V} = \varDelta U + \varDelta PE + \varDelta KE

Most closed systems are stationary in nature and hence the change in potential and kinetic energy is zero (:math:`\varDelta PE=0` and :math:`\varDelta KE=0`). In a large majority of cases, the only applicable work is the boundary work and hence, :math:`W_{other}=0`. Thus we can simplify the above equation to:

.. important:: First Law equation for closed system (Boundary Work form)

  .. math::
    :label: first_law_closed_simple

    Q -   \int_{\mathbb{V}_1}^{\mathbb{V}_2}Pd\mathbb{V} = \varDelta U

While analysing any closed system process, certain idealizations are required to be made to simplify the mathematics. A process may have to be treated as isochoric, isobaric, isothermal, adiabatic or polytropic. A brief on what these are given in the following sections. In each of these processes, the boundary work term must be evaluated and plugged in equation :eq:`first_law_closed_rigorous` or :eq:`first_law_closed_simple` . An evaluation of boundary work for each of these processes is now discussed. This is no more complicated than working out a correct mathematical integral of :math:`\int PdV`, using an appropriate relationship between :math:`P` and :math:`V`

.. index:: isochoric process

Isochoric (Constant-Volume) Process
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: isochoric.png
  :scale: 100 %
  :alt: P-v diagram of isochoric process

For a constant volume process, the volume of the system remains fixed and hence :math:`dV=0` and consequently the boundary work

.. math::
  :label: boundary_work_isochoric

  W_{boundary} = \int Pd\mathbb{V} =0.


.. index:: isobaric process

Isobaric (Constant-Pressure) Process
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: isobaric.png
  :scale: 100 %
  :alt: P-v diagram of isobaric process

For a constant pressure process, :math:`P=P_0` where :math:`P_0` is the constant pressure. Hence, boundary work is given by:

.. math::

  W_{boundary} = \int_{\mathbb{V}_1}^{\mathbb{V}_2} Pd\mathbb{V}= P_0\int_{\mathbb{V}_1}^{\mathbb{V}_2}d\mathbb{V}

therefore

.. math::
  :label: first_law_isobaric

  W_{boundary} = P_0(\mathbb{V}_2-\mathbb{V}_1)


.. index:: isothermal process

Isothermal (Constant-Temperature) Process (Ideal Gas)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: isothermal.png
  :scale: 100 %
  :alt: P-v diagram of isothermal process

For a constant temperature process, :math:`T=T_0` where :math:`T_0` is the constant temperature. For an ideal gas the following relation holds:

.. math::
  :label: ideal_gas_isothermal

  P\mathbb{V} = mR_{g}T_0 = C\\

or,

.. math::

  P  = \frac{C}{\mathbb{V}}

where,
|br|:math:`m` is the mass of the gas in the closed system
|br|:math:`R_{g}` is the specific gas constant (:math:`\frac{R}{MW}`)
|br|:math:`C` is a constant used for simplicity

Hence boundary work for isothermal expansion/compression can be written as:

.. math::

  W_{boundary} = \int_{1}^{2}Pd\mathbb{V} = \int_{1}^{2}\frac{C}{\mathbb{V}}d\mathbb{V} = C\int_{1}^{2}\frac{d\mathbb{V}}{\mathbb{V}} =  C\ln\frac{\mathbb{V}_{2}}{\mathbb{V}_{1}}

or substituting the value of :math:`C` from :eq:`ideal_gas_isothermal`,

.. math::
  :label: boundary_work_isothermal

  W_{boundary} = P_{1}\mathbb{V}_{1}\ln\frac{\mathbb{V}_{2}}{\mathbb{V}_{1}} = P_{2}\mathbb{V}_{2}\ln\frac{\mathbb{V}_{2}}{\mathbb{V}_{1}} = mR_{g}T_0\ln\frac{\mathbb{V}_{2}}{\mathbb{V}_{1}}


.. index:: polytropic process

Polytropic Process
~~~~~~~~~~~~~~~~~~

.. figure:: polytropic.png
  :scale: 100 %
  :alt: P-v diagram of polytropic process

A study of actual expansion and compression processes in most practical situations reveal that the pressure :math:`P` and volume :math:`V` are related by the following equation:

.. math::
  :label: polytropic process

  P\mathbb{V}^{n} = C

where :math:`n` and :math:`C` are constants. Under these situations we can express :math:`P` as :

.. math::

  P = \frac{C}{\mathbb{V}^n}

boundary work can then be written as:

.. math::

  W_{boundary} = \int_{1}^{2}Pd\mathbb{V} = \int_{1}^{2}C\mathbb{V}^{-n}d\mathbb{V} = C\frac{\mathbb{V}_2^{-n+1} - \mathbb{V}_1^{-n+1}}{-n+1}

we can make use of the fact that :math:`C=P_1\mathbb{V}_1^n=P_2\mathbb{V}_2^n` in the above equation and get the equation for boundary work in polytropic process as:

.. math::
  :label: boundary_work_polytropic_a

  W_{boundary} = \frac{P_2\mathbb{V}_2 - P_1\mathbb{V}_1}{1-n}

For an ideal gas gas :math:`P\mathbb{V}=mR_gT`, and therefore we may also write:

.. math::
  :label: boundary_work_polytropic_b

  W_{boundary} = \frac{mR_g(T_2-T_1)}{1-n}

Polytropic process is a very generalised process model. Specific values of polytropic exponent :math:`n` lead to specific processes for example,

For :math:`n=0` is an isobaric process
|br| For :math:`n=+\infty` is an isochoric process
|br| For :math:`n=1` is an isothermal process
|br| For :math:`n=\kappa` is an adiabatic process


.. index:: isentropic process

Isentropic Process
~~~~~~~~~~~~~~~~~~

Isentropic Process is a special case of Polytropic process where :math:`n=\kappa`. By substituting the same in :eq:`boundary_work_polytropic_a` and :eq:`boundary_work_polytropic_a` we get :

.. math::
  :label: boundary_work_isentropic_a

  W_{boundary} = \frac{P_2\mathbb{V}_2 - P_1\mathbb{V}_1}{1-\kappa}

.. math::
  :label: boundary_work_isentropic_b

  W_{boundary} = \frac{mR_g(T_2-T_1)}{1-\kappa}

where,

.. math::

  \kappa = \frac{c_p}{c_v}


.. index:: first law for controlled volume system

First Law Analysis of Controlled Volume System
----------------------------------------------

Mass & Energy Balance for Controlled Volumes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In the case of controlled volume system mass may enter and leave the system. For a system in steady state, the rate of mass *flowing in* equals that *flowing out*. Invoking mass balance principle in steady state system :eq:`mass_balance_steady` we get:

.. math::

  \dot{m}_{in} = \dot{m}_{out}

for a single stream we can write this as:

.. math::

  \dot{m}_1 = \dot{m}_2 = \dot{m}

The energy balance principle for steady state as given in :eq:`energy_balance_steady` can be invoked in the context of a controlled volume system with :math:`\dot{E}_{in}` and :math:`\dot{E}_{out}` as given below: state.

.. math::

  \dot{E}_{in} &= \dot{Q}_{in} + \dot{W}_{in} + \underset{in}{\sum}\lambda_{in}\\
  \dot{E}_{out} &= \dot{Q}_{out} + \dot{W}_{out} + \underset{out}{\sum}\lambda_{out}\\

where,

:math:`\dot{Q}_{in}` is the rate at which heat goes into the system
|br| :math:`\dot{Q}_{out}` is the rate at which heat goes out of the system
|br| :math:`\dot{W}_{in}` is the rate at which work is done on the system (power in)
|br| :math:`\dot{W}_{out}` is the rate at which work is done by the system (power out)
|br| :math:`\lambda_{in}` is the rate at which energy is transported by an incoming stream.
|br| :math:`\lambda_{out}` is the rate at which energy is transported by an  outgoing stream.

Upon substitution in energy balance equation :eq:`energy_balance_steady`, we have,

.. math::
  :label: energy_balance_controlled_volume

  \dot{Q}_{in} + \dot{W}_{in} + \lambda_{in} &= \dot{Q}_{out} + \dot{W}_{out} + \lambda_{out} \\
  (\dot{Q}_{in} - \dot{Q}_{out}) -  (\dot{W}_{out} - \dot{W}_{in})  &=  \underset{out}{\sum}\lambda_{out} - \underset{in}{\sum}\lambda_{in}

To further simplify the above, let us use the expressions of net heat transfer rate(:math:`\dot{Q}`) moving in to the system  and net work rate (:math:`\dot{W}`) done by the system i.e. :

.. math::

  \dot{Q} &= \dot{Q}_{in} - \dot{Q}_{out}\\
  \dot{W} &= \dot{W}_{in} - \dot{W}_{out}\\

Substituting in :eq:`energy_balance_controlled_volume` we get :


.. math::
  :label: energy_balance_controlled_volume_simplified

  \dot{Q} -  \dot{W}  =  \underset{out}{\sum}\lambda_{out} - \underset{in}{\sum}\lambda_{in}

The rate of energy transfer by incoming and outgoing mass ( :math:`\lambda`) needs to be elaborated further to evolve this equation in to a more useable form.  To understand this energy term, the concept of *flow work*, needs to defined which applies to flow processes or controlled volumes.


.. index:: flow work, flow energy

Concept of Flow Work
~~~~~~~~~~~~~~~~~~~~

Just as in the case of closed systems, we need to enhance our idea of work for controlled volume systems as well. A special form of work applies in this case which is termed as **flow work**.

In a flow process, Work is spent to push the fluid into the system. To help our imagination, let us assume that there is a tiny packet of length :math:`L` which is about to enter the system through an area :math:`A`.  The system has a pressure of :math:`P`. This packet is being pushed by the fluid behind, which can be imagined to act like a piston, The work that this piston has to do to push this packet completely in is:

.. math::
  :label: work_flow

  W_{flow} = FL = PAL = P\mathbb{V}

The flow work performed per unit mass can be written as:

.. math::
  :label: specific_flow_work

  w_{flow} = Pv

A similar work is retrieved (sign shall be negative) as fluid moves out of the control volume, pushing the gas downstream.

Though this is work, while working with flow process in controlled volumes it becomes convenient to treat it like an energy associated with the stream. So this is also sometimes referred to as **flow energy**.


.. figure:: controlled-volume.png
  :scale: 50 %
  :alt: flow work in flow process

First Law Equation (Enthalpy Form)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The energy transported by stream of fluid  moving in to a controlled volume constitutes of the internal energy, potential energy, kinetic energy as well as the flow energy.  Thus, on per unit mass terms this can be expressed as:

.. math::
  :label: methalpy

  \theta = w_{flow} + u + pe + ke

The individual terms on the right hand side can be substituted as follows:

|br| specific Work Flow energy :math:`w_{flow} = Pv` from :eq:`specific_flow_work`
|br| specific Potential energy :math:`pe = gz`, where :math:`z` is the elevation from datum
|br| specific Kinetic energy :math:`ke = \frac{1}{2}V^2`, where :math:`V` is the fluid velocity


After substitution in :eq:`methalpy`  we get:

.. math::
  :label: energy_stream

  \theta = Pv + u + gz + \frac{1}{2}V^2

.. index:: enthalpy

The quantity :math:`Pv + u` occurs invariably in all flow problems and hence a new property **enthalpy** is defined just to help simplify matters. Thus enthalpy is defined as:

.. math::
  :label: enthalpy

  h = u + Pv

where,
|br| :math:`u` is the internal energy per unit mass
|br| :math:`P` is pressure of the flow stream
|br| :math:`v` is specific volume

Substituting :math:`h` in the equation :eq:`energy_stream` above we get,

.. math::

  \theta = h + gz + \frac{1}{2}V^2

The rate at which energy is transported by a mass stream can now be expressed as:

.. math::

  \lambda = \dot{m}\theta = \dot{m}(h + gz + \frac{1}{2}V^2)

Using this expression of stream energy rate (:math:`\lambda`) we can write :eq:`energy_balance_controlled_volume_simplified` as follows:

.. important:: First Law equation for controlled volumes (steady state and multiple streams)

  .. math::
    :label: first_law_controlled_volume_rigorous

    \dot{Q} - \dot{W}  =  \underset{out}{\sum}\dot{m}_{out}(h_{out}+\frac{V_{out}^2}{2}+gz_{out}) -  \underset{in}{\sum}\dot{m}_{in}(h_{in}+\frac{V_{in}^2}{2}+gz_{in})


For the most popular case of single stream in and out of controlled volume and acknowledging that under steady state :math:`\dot{m}_1 = \dot{m}_2 = \dot{m}` we get the first law equation as applicable to controlled volumes:

.. important:: First Law equation for controlled volumes (steady state and single stream)

  .. math::
    :label: first_law_controlled_volume

    \dot{Q} - \dot{W}  =  \dot{m}(h_2 - h_1 +\frac{V_2^2 - V_1^2 }{2}+g(z_2-z_1))


Dividing both sides of the equation by mass flow rate (:math:`\dot{m}`), we get the equation on **per unit mass basis**:

.. important:: First Law equation for controlled volumes (steady state and single stream) on per unit mass basis

  .. math::
    :label: first_law_controlled_volume_specific

    q - w  =  h_2 - h_1 +\frac{V_2^2 - V_1^2 }{2}+g(z_2-z_1)


if the changes in kinetic and potential energies can be neglected, then the above further simplifies to:

.. important:: First Law equation for controlled volumes (steady state and single stream) on per unit mass basis with neglible potential and kinetic energy changes

  .. math::
    :label: first_law_controlled_volume_simple

    q - w  =  h_2 - h_1


In the subsequent part of this chapter we shall look into the application of these equation to various devices like nozzles, diffusers, compressors, expanders, throttle valves and mixers etc.

.. index:: nozzle, diffuser

Nozzles and Diffusers
~~~~~~~~~~~~~~~~~~~~~

Nozzles and Diffusers are used in propulsion jet engines, rockets and stationary aerodynamic components of compressors and turbines etc.

A **nozzle** is a device that increases the velocity of the fluid at the expense of pressure.

A **diffuser** is a device that increases the pressure of the fluid at the expense of velocity.

.. figure:: nozzle_diffuser.png
  :scale: 50 %
  :alt: flow work in flow process

In both these devices the heat transfer  can be neglected (:math:`q=0`)as the time period of interaction is very short. Since there is no work done on or by the device we also have (:math:`w=0`). The change in elevation is also negligible and therefore we can consider (:math:`z_2 = z_1`).

Thus the first law equation for controlled volume :eq:`first_law_controlled_volume`, after using the above substitutions becomes:

.. math::
  :label: first_law_nozzle_diffuser

  h_2 = h_1 - \frac{V_2^2 - V_1^2 }{2}

.. tip::

  For nozzles, :math:`V_2 > V_1` and hence :math:`h_2 < h_1`, so a cooling effect is observed.
  |br| For diffusers, :math:`V_2 < V_1` and hence :math:`h_2 > h_1`, so a heating effect is observed.


.. index:: compressor, turbine

Compressors and Turbines
~~~~~~~~~~~~~~~~~~~~~~~~

In a compressor mechanical work is spent to raise the pressure of a fluid (compressible fluid), while in a turbine work is obtained by letting down the pressure of the fluid stream. For approximate calculations these devices can be treated as adiabatic i.e. :math:`\dot{Q}=0`. Further the changes in kinetic and potential energy can also be neglected :math:`\varDelta{pe}=0` and :math:`\varDelta{ke}=0`.



For turbines, a net work is obtained from the device and we can call this work as :math:`W_{output}`. The first law equation :eq:`first_law_controlled_volume` can be written for an approximate analysis case as:

.. figure:: turbine.png
  :scale: 70 %
  :alt: first law for turbines

.. math::

  - \dot{W}_{output} = \dot{m}(h_{2} - h_{1})

rearranging we get the first law equation as applicable to turbines.

.. important:: First Law applied to turbines

  .. math::

    \dot{W}_{output} =  \dot{m}(h_1 - h_2)



For compressors net positive work is done on the machine and we can call this work as :math:`W_{input}`. In a more rigorous performance evaluation such as those adopted by the ASME PTC 10 code for compressor a more accurate approach is adopted. Heat losses from the equipment (:math:`Q_{loss}` is not ignored. The affect of change in potential energy is always neglected by codes as well because it is really very small compared to the other energy terms. Kinetic energy term does not directly enter the heat balance equation, but it is still accounted for by making  use of the concept of total enthalpy (or stagnation enthalpy). Total enthalpy is defined as:

.. figure:: compressor.png
  :scale: 70 %
  :alt: first law for compressor

.. math::

  h_{total} = h + \frac{V^2}{2}


The first law equation :eq:`first_law_controlled_volume` can be written as:

.. math::

  -\dot{Q}_{loss} + \dot{W}_{input} = \dot{m}(h_{2_{total}} - h_{1_{total}})

rearranging we get the first law equation as applicable to compressors.

.. important:: First Law applied to compressors

  .. math::
    :label: first_law_compressor

    \dot{W}_{input} = \dot{Q}_{loss} + \dot{m}(h_{2_{total}} - h_{1_{total}})

  The heat loss is primarily the bearing loss (mechanical loss) and can be determined by measurement of oil flow rates to bearings and the oil temperature rise, using a known value for the oil specific heat. Surface losses can be measuring the compressor body area, surface temperatures and air temperatures and use convective heat loss rules.

.. index:: throttle

Throttling Valves
~~~~~~~~~~~~~~~~~

Throttling valves are flow restricting devices that cause a  significant drop in pressure in the fluid. These devices could be adjustable valves, porous plugs or capillary tubes.

.. figure:: throttle.png
  :scale: 50 %
  :alt: first law for throttling

No work interaction happens in the device and the heat loss is also considered negligible due to the short interaction time.  Thus both heat rate (:math:`\dot{Q}`) and work rate (:math:`\dot{W}`) are zero and therefore after substituting in :eq:`first_law_controlled_volume` we have:

.. math::

  0 - 0 = \dot{m}(h_2 - h_1)

which upon rearrangement leads to the following equation of first law as applicable to throttle valves:

.. important:: First Law applied to Throttle valves

  .. math::

    h_1 &= h_2\\
    u_1 + P_1v_1 &= u_2 + P_2v_2

  while, :math:`h` remains constant its constituents :math:`u` and :math:`Pv` could change such that their sum is a constant.

.. note::
  For ideal gases enthalpy :math:`h` is a function of temperature :math:`T` only. Thus when an ideal gas undergoes throttling the temperature remains same.

  However for most real gases, a temperature drop is observed therby implying that there is a fall in internal energy :math:`u`. This is most notable for refrigerants. For hydrogen, a temperature rise is observed during throttling.

.. index:: mixing

Mixing Chambers
~~~~~~~~~~~~~~~

.. figure:: mixer.png
  :scale: 50 %
  :alt: first law for mixing chamber

Mixing of two streams is a very common engineering problem. For an adiabatic mixing case (which is usually the case), both Heat rate (:math:`\dot{Q}`) and work rate (:math:`\dot{W}`) are zero. Kinetic and potential energy changes can also be neglected. Therefore after substituting in :eq:`first_law_controlled_volume_rigorous` and some rearrangement we have:

.. math::

  (\dot{m_1} + \dot{m_2})h_3 = (\dot{m_1}h_1 + \dot{m_2}h_2 )

if :math:`y = \dot{m}_1/\dot{m}_2`, we get upon dividing the above equation by :math:`\dot{m_2}` :

.. math::

  (1+y)h_3 = yh_1 + h_2

upon rearrangment, leads to the first law as applicable to mixing:

.. important:: First Law applied to Mixing

  .. math::

    h_3 = \frac{yh_1 + h_2}{1 + y}

  with rearrangement, if the enthalpy of the stream after mixing is known, then mixing ratio can be expressed as:

  .. math::

    y  = \frac{h_3 - h_2}{h_1 - h_3}


  where :math:`y = \dot{m}_1/\dot{m}_2`, is the mixing ratio


.. index:: heat exchanger

Heat Exchanger
~~~~~~~~~~~~~~

Heat exchanger is a device where two moving streams exchange heat without mixing with each other. There is no work interaction in a heat exchanger and assuming adiabatic process (which is a good approximation of heat exchanger), the heat interaction can also be neglected.

.. figure:: heat-exchanger.png
  :scale: 70 %
  :alt: first law for heat exchanger

Let the two streams be ':math:`a` and ':math:`b` and their mass flow rates :math:`m_a` and :math:`m_b` respectively. Let subscript :math:`1` denote inlet and  subscript :math:`2` outlet as usual. Substituting in :eq:`first_law_controlled_volume_rigorous` we get the first law equation for heat exchanger:

.. important:: First Law applied to Heat Exchanger

  .. math::

    \dot{m}_a(h_{a_1} - h_{a_2}) = \dot{m}_b(h_{b_2} - h_{b_1})
