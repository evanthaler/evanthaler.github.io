---
layout: page
title: Permafrost machine learning
permalink: /pfml/
---
<html>
<head>
<style>
</style>
</head>
<body>

	<figure alt="Grid" style="width:450px;height:200px;margin-right:15px;float:left;padding-right:20px;padding-bottom:300px">
		<img src="/assets/research/permafroststudyarea.jpg">
		<figcaption style="text-align:justify">
			<b>Fig. 1</b> Here are the areas on the Seward Peninsula in Alaska where we used field and remote sensing data to map the extent of near-surface permafrost. The photos show the type of vegetation we see at the sites. Those shrubs can be seen in the Lidar point cloud data by making models of the canopy. (You can open the image in a new tab to view a larger version)
		</figcaption>			
	</figure>
	<p>
	
<h1><b>Using machine learning models to make high-resolution maps of permafrost extent</b></h1>
	<p style="text-align:justify">
First of all what is permafrost? Strictly, permafrost is any ground that is frozen for two at least two consecutive years. In our work, we only consider the permfrost within the upper 120 cm of the ground surface, which we call "near-surface permafrost." We're interested in making high-resolution maps ( <5 m spatial resolution) because 1) when permafrost thaws, the ground can sink rapidly and cause damage to nearby or overlying infrastructure, and 2) permfrost soils hold a ton of carbon which can be released during thaw, and we want to know how much of the landscape has already thawed. 
    </p>
    <p>
We wanted to test how well machine learning models can be trained to make maps of near-surface permafrost extent. For ground truth data, we used some geohysical measurements and other observations like soil pits and frost probes. 
    </p>
    <p>
It turns out that snow is has high reflectance (is really bright) in the blue wavelengths. We developed an algorithm called the Blue Snow Threshold algorithm, which dynamically sets a threshold blue reflectance value to separate snow and non-snow pixels (Figure 1). Now, because we are only using blue wavelengths, we can use high-resolution satellites to actually map the distribution of snow on the landscape throughout the year. 
	</p>


<h1><b>Validating our snow cover estimates</b></h1>
	<p style="text-align:justify">
We compared the extent of snow covered area predicted by just using the blue wavelength to snow cover estimates from Landat 8, which uses many different wavelengths and to snow covered area measured with repeat lidar scans (Figure 2). <a href="https://oceanservice.noaa.gov/facts/lidar.html#:~:text=Lidar%2C%20which%20stands%20for%20Light,variable%20distances)%20to%20the%20Earth."><b>Lidar</b></a> is a fancy laser range finder attached to an airplane or helicopter. We found that just using the blue wavelengths works really well and is really easy to do! You can read more about our method in the paper published in Earth and Space Science(<a href="https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2023EA003015"><b>Thaler et al., 2023</b></a>). 
	</p>
	
	
	<figure alt="Grid" style="width:450px;height:300px;margin-right:15px;float:left;padding-right:20px;padding-bottom:300px">
		<img src="/assets/research/ASO_v1.jpeg">
		<figcaption style="text-align:justify">
			<b>Fig. 2</b> Comparison of snow cover predicted by our method (BSI) to snow cover measured using airbone laser measurments from the <a href="https://www.airbornesnowobservatories.com/"><b>Airbone Snow Observatory (ASO)</b></a>. Our method is correctly predicting snow covered area with a precision of around 85%. (You can open the image in a new tab to view a larger version)
		</figcaption>			
	</figure>
	<p>
	

	

