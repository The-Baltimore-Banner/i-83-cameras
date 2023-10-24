# I-83 Speed Cameras Crash Analysis

This repository includes all of the code and methodology needed to reproduce The Baltimore Banner's findings on the impact of new speeding cameras on I-83 crashes.

- [Overview](#overview)
- [Methodology](#methodology)
- [Limitations](#limitations)
- [Correction](#correction)
- [License](#license)

---
## Overview

More than a year after Baltimore City Department of Transportation officials flipped the switch on two new speed cameras on Interstate 83, car crashes have significantly decreased, a Baltimore Banner data analysis found.

The city-controlled “Grand Prix,” as some call it, due to the way some people drive it, connects Baltimore to Harrisburg, Pennsylvania. It has long bedeviled area drivers with its winding curves, lack of lighting and unruly motorists. The city’s I-83 speed camera initiative, which kicked off last year in an effort to slow drivers on their way in and out of the city, already had shown early anecdotal success at reducing speeds. Fewer tickets have been issued than city officials expected.

But it’s been unclear whether the two cameras — one positioned northbound, the other southbound — have influenced drivers. Some experts who study driving psychology and traffic-calming measures were skeptical they would.

However, The Banner’s analysis of state vehicle-crash data and the city’s citations shows the number of crashes has dropped significantly since March 2022, when transportation officials installed the two cameras. They began issuing citations from those cameras in July 2022 following a 90-day trial period.

Read the story: [A year into speed cameras program, I-83 crashes are down](https://www.thebaltimorebanner.com/community/transportation/interstate-83-speed-cameras-analysis-AZIOHN64TRHPJD6TEB2HL2JFTU/)

Download the [data](https://banner-public.s3.amazonaws.com/i-83-camera-data.zip) needed to reproduce this analysis. 
---

<a id="methodology"></a>

## Methodology

The Baltimore Banner used data obtained by a public information request and **Parking & Moving Citations** data from [OpenBaltimore](https://data.baltimorecity.gov/datasets/parking-and-moving-citations/explore) for this analysis. The Banner is able to identify where drivers receive their tickets, the reason behind the citation and the speed they were going at the time a driver was cited. Speed was not available on Open Baltimore.

Crashes on I-83 were analyzed using data from the [Maryland Crash Database](https://mdsp.maryland.gov/Pages/Dashboards/CrashDataDownload.aspx).

The Banner defined I-83 using the [MDOT SHA Roadway National Highway System](https://data-maryland.opendata.arcgis.com/datasets/maryland::mdot-sha-roadway-national-highway-system-nhs/explore?location=39.150272%2C-76.802565%2C10.66) shape file. The Banner did not count crashes that occurred on ramps on and off the highway.

Distances calculated by The Banner are calculated "as the crow flies." That means parts of I-83 we say are two miles away are so when measured in a straight line. Actually driving the winding road that is I-83 may be slightly longer or shorter than the stated distance to any given point.

The road was binned based on the distance from the overpass closest to the two cameras. The furthest bin, mile 4, is not a complete mile. Crash rates were calculated by dividing the number of accidents by the length of the bin to the hundredth decimal point.

<a id="limitations"></a>

## Limitations

There are known errors in the way the Maryland State Police collect and report crash data that impact this analysis. 

There is a lag in the reporting of the most serious crashes. Crashes that were complex or resulted in a fatality often take much longer to investigate. Only crashes that have a complete investigation are included in the data. Counts of the most recent crashes are, therefore, likely incomplete. The Banner has noted this in the story and intends to revisit this analysis after more time has passed.

Sometimes, the listed road does not match the point listed in the Maryland crash database. The Banner only counted crashes that both identified I-83 or the Jones Falls Expressway as the road where the crash occurred and when the listed latitude and longitude show a position on the expressway. Points that were excluded appear to be far away from the road or to have happened on ramps on and off the highway.

<a id="correction"></a>

## Correction

An earlier version of this analysis inadvertantly included 543 crashes that did not occurr on I-83. This error was introduced during fact checking. The error did not diminished the strength of the analysis. When only including crashes that list I-83 as the road and have latitude and longitude locations that intersect with the road, the decrease in crashes near the speed cameras is actually larger than we originally reported.

---

## License

Copyright 2023, The Venetoulis Institute for Local Journalism

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
