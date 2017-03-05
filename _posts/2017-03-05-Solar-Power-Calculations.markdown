---
layout: post
title:  "Solar Power Calculations"
date:   2017-03-05 22:09:16 -0800
categories: Electrical Solar
author: Ben
imagePath: "Monocrystalline_solar_panel.png"
---
Calculating solar power requirements can seem simple, but there are quite a few components to be aware of when attempting to size solar arrays and battery banks.  The below discussion addresses some of the items to take into account.  For the discussion we have assumed that the solar power system is photovoltaic (PV) based (not solar thermal) and that the system is stand-alone (not grid tied).


## Electrical Load


The electrical load for a given system is composed of AC loads, DC loads and conversion inefficiencies.  Because electrical loads will vary over time, be sure to track both peak load and average load.  Average power is usually calculated over 1 day or 1 week.  A given piece of equipment can be divided into different power consumption states such as ‘receive and transmit’ or ‘compressor on and compressor off’ in order to capture the actual amount of power consumed on average.


For AC power loads, be sure to include the actual or estimated power factor as that will affect the ‘real’ power required.  For DC power loads, but sure to factor in any DC-DC power conversion losses or AC-DC conversion loss if that is how the system is architected.  If cooling or heating is required, be sure to have worked through the required power to support the thermal load.


![AC Power Calculations Headings][ac]


![DC Power Calculations Headings][dc]


Once you have an accurate estimate or measurement of the electrical load, you are ready to estimate the number of solar panels that will be required.


## PV Panels


In order to accurately understand the photovoltaic production capability of a given site, you will need to know a few details:


* Clear view of the sky - Any shading or shadows crossing the PV array such as trees or even chain-link fences will degrade the production capability of the array.
* Ambient temperature - Very high ambient temperatures will degrade the performance of a PV array.  Determine the temperature coefficient of the proposed PV panels and compare with the average, high and low temperatures of the site.
* Solar intensity (insolation) - The solar power available will vary by time of year and latitude.  Consult a good source of solar information for a given location such as NASA’s Surface Meteorology and Solar Energy [site][sse].  Keep in mind that the power ratings for PV panels are usually stated under ‘standard’ test conditions. The ‘standard’ test conditions may not apply to the site for the majority of the time.
* Solar tracking - The amount of solar energy that will be captured will depend on the incident angle of the sun to the PV array.  Tracking is usually either full (horizontal and vertical) or vertical only.  Fixed angles will have to be determined based on if the system is engineered for peak (summer), average or worst case (winter) solar energy capture.
* Dark or Cloudy days - Weather impacts the solar production capability of a system.  While this factor generally determines the size of the battery reserve, it also plays into the ‘recovery’ time of the system which can determine the size of the PV array.  The recovery time is how long it takes the battery system to come back to a full charge following a deep discharge event.


## Battery Storage


The required battery capacity for the system is dependent on the load (of course), required battery runtime and the required lifetime of the battery system.  The required runtime will depend on the safety factor that is required of the system and the estimated number of ‘dark days’ for a given site.  ‘Dark days’ are not solar eclipses(!), but rather are days where cloud cover reduces the solar insolation far below the average and solar power production is minimal.  Ensure that the entire system can absorb at least the historical number of dark days for a given time period - keeping in mind that the PV array must be sized to provide enough extra energy to allow the battery system to recover from dark days in a reasonable amount of time.


The capacity of the battery system to hold energy will be reduced over time.  You can see this happening in your cell phone.  The effect is accentuated for systems where the battery container ambient temperature is high ( greater than 25 deg. C) for extended periods of time.  Additional battery system capacity can compensate for the reduction in performance to hit a system lifetime performance goal.


## Solar MPPT and Battery Charge Controller


Almost all modern solar systems use a maximum power point tracker (MPPT) facing the PV array.  Because PV arrays are essentially current sources, the voltage can be set by the system to maintain the maximum power production from the array.  The details behind MPPT would be a discussion for another day.


The battery charge controller should be configured to match the type of battery (VRLA, Lithium, Gel, etc.).  Be sure to consult the manual for the battery that is used to set the charge voltage points and double-check the voltage with a meter at installation time and during preventative maintenance inspections.


## Finale


When designing a solar powered system, ensure that all of the loads and inefficiencies are accounted for.  Ensure that the PV array is sized appropriately for the location and to provide sufficient excess power to recharge a discharged battery system in a reasonable amount of time.  Size the battery bank system to account for historical dark days and system aging effects.  Finally, ensure that the solar power tracking and battery charging electronics are appropriate for the system.




[sse]: https://eosweb.larc.nasa.gov/sse/
[ac]: {{ site.baseurl }}/assets/ACpowercalcs.png “AC Power Calculation Headings”
[dc]: {{ site.baseurl }}/assets/DCpowercalcs.png “DC Power Calculation Headings”