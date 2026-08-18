---
title: "PMF code design"
draft: false
---

#  PMF (Plant Modelling Framework) 

In simple terms this is a software framework for representing the plant components in APSIM. See [PMF Paper for more details.](https://doi.org/10.1016/j.envsoft.2014.09.005)

![PMF model structure example](https://ars.els-cdn.com/content/image/1-s2.0-S1364815214002588-gr1.jpg)

# Consideration for crop models:

* Root models must allow for multi-point root systems. This is provided when [IUptake](https://github.com/APSIMInitiative/ApsimX/blob/master/Models/Interfaces/IUptake.cs) is implemented and the standard *Root* class is used. If an alternate *Root* model is used, it needs to allow for multi-point root systems.
* Plant models must provide CO2 impacts. If the user changes CO2 in the weather component the plant model should respond.
* Plant models must use the transpiration value provided by MicroClimate. Without this, intercropping will not be possible.