CHAPTER 1. - INTRODUCTION AND KEY DEFINITIONS
=============================================

.. meta::
  :description: This chapter covers the relevant areas of thermodynamics applications and the approaches for system definition. It brings out definitions that are central to the understanding of the subject like property, state, process, equillibrium, pressure, specific volume and temperature.
  :keywords: thermodynamics, closed system, open system, equillibrium, pressure, specific volume, temperature
  :author: Sandeep Raheja


The word *thermodynamics* originates from the greek words *therme* (heat) and *dynamis* (force). The name of this branch of study suggests that it sprang out of the human endeavour to convert heat energy into useful mechanical work.

Modern thermodynamics, today deals with all aspects of energy conversion including chemical energy, heating and cooling aspects etc.


Relevant areas
--------------

Study of thermodynamics is especially fruitful for engineers who are dealing with equipment like pumps, compressors, engines, gas turbines and steam turbines, fired heaters, boilers, combustion processes, refrigeration and air conditioning etc.

All the above applications deal with heat, work and chemical energy interconversions. Certain processes as encountered in mechanical equipment deserve special attentions and have therefore become the focus of thermodynamic analysis. These include:

* compression of fluids using work energy in compressors
* expansion of fluids deriving work energy in turbines and expanders
* acceleration of fluids in nozzles
* deacceleration of fluids in diffusers
* heat addition through combustion or nuclear reactions
* power or refrigeration cycles which involve a sequence of compression, heat addition, expansion and heat removal in some variant or other.
* propulsion
* throttling of fluids
* mixing of fluids
* heat transfer
* phase changes (evaporation, condensation, gas separation, liquefaction etc)

Reader may recall from their own experience, as to how often these are encountered in our day to day engineering activities.

.. index:: system, boundary, surroundings

System Definition
-----------------
An important step in any problem solving is to have a proper definition of problem. In order to avoid distractions, the subject of our study is separated from the rest of the world and all interactions of our subject with the external world carefully analysed.

In mechanics for example a free body diagram is drawn for the subject, identifying all the forces which act on the subject. The principles of second law of motion can then be applied.

In thermodynamics also we need to separate the subject (which we shall henceforth refer to as **system**) from the external world (which shall henceforth be referred to as **surroundings**) by a **boundary**. This boundary is totally fictitious and may change in shape and size even. This boundary is created to identify all interactions of concern that may happen between the system and the surroundings. In thermodynamics important interactions are mass and energy (in any form heat/work/kinetic/potential etc.), moving into and out of the system.


System Study approaches
-----------------------

Two basic kinds of systems are used in analysis.

.. index:: closed system, non flow process

closed system
~~~~~~~~~~~~~

The system is defined as a fixed quantity of matter under study. No mass transfer applies at the boundary. As an example, a gas expanding in a cylinder piston arrangement can be analysed as a *closed* system.

.. index:: isolated system

If there is no heat or work transfer also at the boundary, the closed system can be called as an *isolated* system.

As no mass flows cross the system boundary, thermodynamic process related to closed systems is also referred to as *non flow  process*.

.. index:: controlled volume, flow process

controlled volume
~~~~~~~~~~~~~~~~~

In this approach a region within a prescribed area of space is studied. Mass may flow into and out of this system. A steam turbine where steam enters the inlet nozzle and leaves the exhaust nozzle, can be modelled using a controlled volume approach.

As mass flows may cross the system boundary, thermodynamic process related to controlled volume is also referred to as *flow process*.

.. attention:: Just because gas expansion in cylinder piston has been used as an example for closed system does not imply that closed system approach is the most convenient approach in equipment with cylinder pistons. In most practical cases this is not the case. Performance of engines and reciprocating compressors can be more easily analysed using a control volume approach where air/gas enters the system, exhausts/discharge leave the system and also other fluid streams like cooling water, lube oil and sealing fluids could enter and leave.

  ASME PTC codes aptly use controlled volume approach in analysing performance tests of various.

.. index:: property, state, process

Property, State and Process
---------------------------
To sufficiently describe a system we need to take recourse to some quantified measureables that serve to characterize a system.

A **property** is thus a macroscopic characteristic of a system such as mass, volume, energy, pressure, and temperature to which a numerical value can be assigned.

The **state** refers to the condition of a system as described by its properties. Since *properties* may be interrelated, knowing just a few may help us in determining all the rest. A system is said to be in **steady state** if none of its properties changes with time.

A **process** is a transformation from one *state* to another. So when *property(or properties)* change the *state* of the system is understood to have changed.

A **thermodynamic cycle** is a sequence of *processes* that begins and ends at the same *state*.

.. tip:: A quantity is a property if its change in value between two states is independent of the process. It follows that if the value of a particular quantity depends on the details of the process, and not solely on the end states, that quantity cannot be a property. So while *pressure*, *temperature* , *density*, *enthalpy*, *entropy* qualify as properties, *work* and *heat* do not. The amount of work or heat transferred during a process does not depend on the initial and final states alone, but also on the path taken.

.. index:: extensive properties, intensive properties

Extensive and Intensive Properties
----------------------------------

A property is called **extensive** if its value for an overall system is the sum of its values for the parts into which the system is divided e.g.  mass, volume, energy etc. Extensive properties are dependent on the size or extent of the system.

A property is called **intensive** if its value is independent of the size or extent of a system and may vary from place to place within the
system at any moment e.g. pressure, temperature, specific volume etc.

.. index:: phase, pure substance


Phase and Pure Substance
------------------------

The term **phase** refers to a quantity of matter that is homogeneous throughout in both chemical composition and physical structure (i.e. all solid, all liquid, or all vapor). A system can contain one or more phases.

A **pure substance** is one that is uniform and invariable in chemical composition. A pure substance can exist in more than one phase, but its chemical composition must be the same in each phase e.g. a substance containing liquid water and ice can be called as pure.

A uniform mixture of gases can be regarded as a pure substance provided it remains a gas and does not react chemically and no liquids are formed in the temperature/pressure range of interest.

.. index:: equillibrium

Equilibrium
-----------

A thermodynamic system can be said to be in a state of equillibrium if, when isolated from the surroundings, does not show any tendency of change of state spontaneously. Thus pressure (ignoring gravity effects), temperature and other property values should tend towards uniform values and there should be no tendency to change in terms of phase and chemical composition.


Three Measurable Properties :math:`P`, :math:`v` and :math:`T`
--------------------------------------------------------------

Three particularly important intensive properties in the study of thermodynamics are:

* Pressure (:math:`P`)
* Specific Volume (:math:`v`)
* Temperature (:math:`T`)

Thermodynamics takes a macroscopic perspective of the system. It makes use of an assumption (the *continuum hypothesis*) that the matter is distributed continuously throughout the region. It is therefore possible to speak of thermodynamic properties at a point.

.. index:: pressure

Pressure (:math:`P`)
~~~~~~~~~~~~~~~~~~~~
Let us take a point in the fluid at rest and consider a small area :math:`A` passing through it. The fluid on one side of this area :math:`A` exerts a compressive force normal to the area. The fluid on the other side exerts an equal and opposite force. The *pressure* :math:`P` at the specified point is defined as the limit

.. math::
  :label: pressure_defn

  \begin{equation}
    p=\lim_{A\rightarrow A^{'}}\frac{F_{normal}}{A}
  \end{equation}

where :math:`A^{'}` is the smallest area for which a definite value of this ratio exists. The area is large enough for sufficient molecules to exist so that the *continuum hypothesis* can hold through statistical averages.

.. index:: density, specific volume

Specific Volume (:math:`v`)
~~~~~~~~~~~~~~~~~~~~~~~~~~~
Density (:math:`\rho`) is defined as the mass (:math:`m`) per unit volume (:math:`V`). Density at a point in fluid can be defined as a limit:

.. math::
  :label: density_defn

  \begin{equation}
    \rho=\lim_{V\rightarrow V^{'}}\frac{m}{V}
  \end{equation}

where :math:`V^{'}` is the smallest volume for which a definite value of this ratio exists. The volume is large enough for sufficient molecules to exist so that the *continuum hypothesis* can hold through statistical averages.

The *specific volume* (:math:`v`) is defined as the reciprocal of density.

.. math::
  :label: specific_volume_defn

  \begin{equation}
    v=\frac{1}{\rho}
  \end{equation}

.. index:: thermal equillibrium

Temperature (:math:`T`)
~~~~~~~~~~~~~~~~~~~~~~~

In layman's terms Temperature is the degree of *hotness* or *coldness* of a body. However, this description can not be accepted as a scientific one as it is based on perceptions which may also be erroneous. To understand temperature we have to understand the concept of  *thermal equillibrium*. The concept of equillibrium has already been defined in earlier sections. In short, a system at equillibrium does not show any spontaneous change in properties when isolated from its surroundings

.. index:: thermal interaction

Temperature is in some sense the key to all properties i.e. all other properties depend on it. If we take Two different bodies and bring them in contact with each other a specific interaction which we can call us *thermal interaction* occurs. The warmer body tends to cool off while the colder body tends to warm. A change in properties like density, thermal conductivity, electrical conductivity, mechanical strength also occur during this interaction. Over a period of time, both bodies reach equilibrium and the state (i.e. properties) of the two bodies no longer changes. It would be beneficial to ascribe a property to the two bodies, which helps determine whether the two are at equillibrium or not. Developing this idea further, it is can be postulated that two bodies will be in thermal equillibrium, if their *temperature* property is equal.

.. index:: zeroeth law of thermodynamics, thermometer

It is also a universal experience that when two bodies are in thermal equillibrium with a third body, they are also in thermal equillibrium with each other. This is also known as the *zeroeth law of thermodynamics*. This law, forms the basis of temperature measurement and the third body which is used as a reference body is the *thermometer*.
