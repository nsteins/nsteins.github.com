---
layout: post
title: 
date: 2020-07-31 15:05
category: 
author: 
tags: []
summary: 
---

The Green New Deal tries to connect social and environmental issues by identifying problems with connected causes and solutions. One of those connections is between equitable access to housing and energy costs. Having access to heat and lights is a fundamental part of having access to housing, so it is important to think about affordable utility bills as a part of affordable housing. This is one of the core principles of the [Democratize Com Ed](democratizecomed.com) campaign: a publicly owned utility could do more to make sure that energy is affordable for everyone. 

Utility affordability is often studied under the name "Utility Burden", which simply refers to the portion of household income spent on utility bills (often including electric, gas/fuel heating, and water). For middle and upper income households, this burden is often below 4%, but for lower income families, this can be much higher. Elevate Energy's research shows that amongst low income families in Illinois, [the average utility burden is 13%](https://www.elevateenergy.org/wp/wp-content/uploads/Energy-Burden-in-IL.pdf) Lower income households need utilities as much as their higher income counterparts, and their energy bills are roughly comparable (TKTK CITE), but with flat rate pricing, they end up paying a much larger share of their income.

Another compounding factor in utility burden is the role of energy efficiency. Energy efficiency in both building materials and appliances has drastically improved over time, but lower income families are more likely to live in older housing stock with older appliances, leading to even higher energy bills. Energy efficiency is also an important part of a transition to a zero carbon energy future, as reduced demands will reduce the amount of renewable power generation sources that we need to build. While there are many programs that provide subsidies for improvements in energy efficiency, they are often inaccessible to lower income households, because they are only available to property owners, or because they lack the resources to make an upfront cash investment in appliances that will save money over the long term, even with a subsidy.

As part of my work with Democratize ComEd, I wanted to understand where in Chicago utility burden is the highest, in order to understand which members of the city council could best help their constituents by providing affordable, progressive rates on electricity. Fortunately, the Department of Energy has provided data on energy burden as part of its [Low Income Energy Affordability Data (LEAD) Tool](https://openei.org/doe-opendata/dataset/celica-data). This data is based off of the 2016 5-year American Community Survey (ACS), which provides sample responses on household income, utility costs and building characteristics. 

The first challenge with using this dataset is that the data is aggregated at a census tract level, but I am interested in viewing the data by aldermanic ward, which don't line up neatly with each other. Fortunately, I have encountered this problem before, and re-sample the energy burden data by intersecting geometries and assign data proportional to the intersection. (see [this gist](https://gist.github.com/nsteins/cdb6e947e7e9ff9bf717798050f2a143) for an example). This is obviously not a perfect method, since it assumes that households are evenly distributed through the area of a census tract, but this is not true due to parks, airports, industrial buildings, etc. However, it is hopefully accurate enough, since we are splitting data from a few thousand [TKTK] census tracts into 50 city wards. When all the re-sampling is done, we have a map of energy burden in Chicago by aldermanic ward.

**TKTK add burden % map**

For anyone familiar with the racial and economic segregation in Chicago, this map will not be surprising. Wards on the South and West sides of Chicago have an average energy burden of 10%-12%, while wealthier wards on the North side have an average energy burden of 2%-4%. The primary driver of energy burden is income, so this roughly maps income in the city. 

However, after creating this map, I wasn't satisfied. Averages often obscure information, and this was especially true when calculating energy burden as a fraction of household income. Households with high incomes were lowering the average in the entire ward and obscuring the acuity of energy burden in low income households. If you filter the data to only map energy burden for lower income households, you see that energy burden is much higher than the average and more evenly spread through out the city. Even in wealthier wards, there are still people struggling with energy burden.

**TKTK add FPL 150? % map**

So this lead me to refine the question from "What is the average energy burden per ward?" to "How many households are struggling with energy burden per ward?" Using estimates of the number of households in each income bracket, along with the estimated energy bill per census block, I was able to map out the number (and percentage) of households in a ward experiencing an energy burden greater than 6%. (6% is often defined as the threshold of affordable energy burden TKTK).

**TKTK add burden number map**

I think this map gives a much clearer and tangible representation of the problems with energy affordability. In high-burden wards, there are >10,000 households experiencing energy burden, which is over 60% of households in the ward! But even in low-burden wards, where the average energy burden is <4%, there are still thousands of households experiencing energy burden. I hope this information can help us 
