---
layout: page
title: Permafrost research
permalink: /permafrostresearch/
---
<html>
<head>
<style>
</style>
</head>
<body>

	<figure alt="Grid" style="width:450px;height:300px;margin-right:15px;float:left;padding-right:20px;padding-bottom:100px">
		<img src="/assets/research/bst_example.png">
		<figcaption style="text-align:justify">
			<b>Fig. 1</b> Example of estimating snow cover using only the blue wavelength. The images on the left is the actual satellite photo showing snow as white areas. The middle image panels show the distribution of blue reflectance values, and the threshold value for each image. The images on the right show the (You can open the image in a new tab to view a larger version)
		</figcaption>			
	</figure>
	<p>
	
<h1><b>Estimating snow cover using satellites</b></h1>
	<p style="text-align:justify">
Why are we interested in detecting snow? Snow is a pretty integral component of the global climate system. First, fresh snow is really bright (a property we would call high albedo). That high albedo reflects a lot of the radiation from the sun, which can regulate the land temperature. Snow melt is also a dominant source of water in many regions across the planet.  
    </p>
    <p>
My interest in snow is its influence on permafrost soils. It might seem counterintuitive, but snow actually insulates the ground during winter and keeps the ground warmer than the cold air temperature. The insulating effect can cause soils to not refreeze during the winter, which can cause degradation or thawing of permafrost. We want to know where snow is the thickest or hangs out the longest on the landscape, especially in tundra ecosystems, so we can investigate the impact of snow on permafrost freezing/thawing. 
    </p>
    <p>
It turns out that snow is has high reflectance (is really bright) in the blue wavelengths. We developed an algorithm called the Blue Snow Threshold algorithm, which dynamically sets a threshold blue reflectance value to separate snow and non-snow pixels (Figure 1). Now, because we are only using blue wavelengths, we can use high-resolution satellites to actually map the distribution of snow on the landscape throughout the year. 
	</p>


<h1><b>Validating our snow cover estimates</b></h1>
	<p style="text-align:justify">
We compared the extent of snow covered area predicted by just using the blue wavelength to snow cover estimates from Landat 8, which uses many different wavelengths and to snow covered area measured with repeat lidar scans (Figure 2). <a href="https://oceanservice.noaa.gov/facts/lidar.html#:~:text=Lidar%2C%20which%20stands%20for%20Light,variable%20distances)%20to%20the%20Earth."><b>Lidar</b></a> is a fancy laser range finder attached to an airplane or helicopter. We found that just using the blue wavelengths works really well and is really easy to do!
	</p>
	
	
	<figure alt="Grid" style="width:450px;height:300px;margin-right:15px;float:left;padding-right:20px;padding-bottom:300px">
		<img src="/assets/research/ASO_v1.jpeg">
		<figcaption style="text-align:justify">
			<b>Fig. 2</b> Comparison of snow cover predicted by our method (BSI) to snow cover measured using airbone laser measurments from the <a href="https://www.airbornesnowobservatories.com/"><b>Airbone Snow Observatory (ASO)</b></a>. Our method is correctly predicting snow covered area with a precision of around 85%. (You can open the image in a new tab to view a larger version)
		</figcaption>			
	</figure>
	<p>
	
<h1><b>Using machine learning to identify permafrost areas</b></h1>
	Coming soon!
	
