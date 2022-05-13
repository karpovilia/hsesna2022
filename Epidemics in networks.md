##
## SIR model
The SIR model is one of the simplest compartmental models, and many models are derivatives of this basic form. The model consists of three compartments:

* ***S**: The number of **s**usceptible individuals. When a susceptible and an infectious individual come into "infectious contact", the susceptible individual contracts the disease and transitions to the infectious compartment.
* ***I**: The number of **i**nfectious individuals. These are individuals who have been infected and are capable of infecting susceptible individuals.
* ***R** for the number of **r**emoved (and immune) or deceased individuals. These are individuals who have been infected and have either recovered from the disease and entered the removed compartment, or died. It is assumed that the number of deaths is negligible with respect to the total population. This compartment may also be called "**r**ecovered" or "**r**esistant".

SIR model takes population, infected cases, recovered cases as input. The model is able to give predictions for an arbitrary time period. As an output, it gives the number of infected and recovery cases.

**Model description** The SIR model is one of the simplest compartmental models, and many models are derivatives of this basic form. The model consists of three compartments: S for the number of susceptible, I for the number of infectious, and R for the number of recovered or deceased (or immune) individuals. SIR system can be described by the following set of ODE:
$$\frac{ds}{dt}= -\frac{βIS}{N}$$
$$\frac{dI}{dt}= \frac{βIS}{N} - \gamma I$$
$$\frac{dR}{dt}= \gamma I$$
where $\beta$ is the number of people infected at each timestep and $\gamma$ is the recovery rate.  $S$ is the stock of susceptible population, $I$ is the stock of infected, $R$ is the stock of removed population (either by death or recovery), and $N$ is the sum of these three.

The model takes information about the healthy and infected people and simply forecasts the next values based on the ODE system.

**Training process** Scipy library can be used to calculate ODE’s and fit the SIR parameters (e.g curvefit method in the scipy.optimize module).

**Limitations** The SIR model does not count many factors and its parameters are considered to be constant. Death predictions The SIR model is not able to predict death cases.


## SIR with polynomial contact rate (SIR-poly)

SIR-poly model takes population, infected cases, recovered cases as input. The model is able to give predictions for an arbitrary time period. As an output, it gives the number of infected and recovery cases.

**Model description** In the basic SIR model we assume a static contact and transition rates through the entire course of the disease, which is not the case for the epidemics. The spread of the disease has led to large changes in societal behavior and so on, which affect the rate of the spread. It is suggested (Conley, 2020) to define the contact
rate as a function of active cases. For example, let $X_i$ be active cases per thousand $\beta_i$ be the contact rate at a point in time $i$.
$$X_i = \frac{l_i}{N} * 1000$$
$$\beta_i = \beta_aX_i + \beta_b$$
$\beta_i$ is then used as a beta in the basic SIR system.

**Training process** Scipy library can be used to calculate ODE’s and fit the SIR parameters (e.g curvefit method in the scipy.optimize module).

**Limitations** This model does not count many factors. Death predictions The SIR-poly model is not able to predict death cases.


## SIS model
