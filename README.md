# UrbanRVM-Hack4Resilient

**UrbanRVM – Reducing Local Flood Risk in Jakarta**

**Overview**
UrbanRVM (Urban Runoff Volumetric Model) is a runoff simulation tool tailored for flat urban topography such as Jakarta. Unlike conventional flood models that primarily simulate river overflow, UrbanRVM focuses on local runoff processes using a 2D surface-based approach.

**Key features:**
	•	2D Runoff Modeling with NF 3×3 neighborhood analysis to estimate flow accumulation, stop points, and runoff hotspots.
	•	Deep Learning Integration using a CNN (Convolutional Neural Network) to develop a Flood Susceptibility Model (FSM).
	•	Runoff Management Scenarios that evaluate potential interventions such as:
	•	Green Base Coefficient (KDH) regulation.
	•	Infiltration wells.
	•	Optimization of green open space (RTH).
	•	Outputs include surface runoff flow direction, accumulation maps, and scenario-based vulnerability analysis

**Instructions**
	1.	Data Preparation
  	•	Input datasets:
  	•	Digital Elevation Model (DEM).
  	•	Land use / impervious surface.
  	•	Rainfall records.
  	•	Hydrological indicators (NDBI, NDVI, TWI, slope, distance to rivers/drainage/pumps).
  	•	Preprocess into GeoTIFF raster layers.
	2.	Runoff Simulation
  	•	Apply Neighborhood Filter (NF 3×3, minimum function) to calculate flow accumulation and runoff stop points.
  	•	Derive Runoff Volumetric Maps per catchment.
	3.	CNN Model Training
  	•	Prepare training & testing datasets using historical flood records.
  	•	Train LSM_CNN model with selected features.
  	•	Validate against strategic flood-prone areas.
	4.	Scenario Analysis
  	•	Define alternative land management scenarios:
  	•	Implementation of Green Base Coefficient (KDH/GBC).
  	•	Infiltration well (sumur resapan) deployment.
  	•	Enhancement of green open space (RTH).
  	•	Compare existing vs scenario outputs to assess flood risk reduction.
	5.	Visualization & Reporting
  	•	Generate:
  	•	Accumulated runoff maps (m³/year).
  	•	Flood vulnerability maps (FSM).
  	•	Comparative scenario plots.

**Credits**
This work was developed as part of Hack4Resilient Jakarta 2025: Reimagining Urban Futures, led by the Sepuluh Nopember Institute of Technology (ITS).
	•	Research Team: UrbanRVM Development Group
	•	Core Contributions:
	•	2D runoff modeling workflow.
	•	CNN-based Flood Susceptibility Model.
	•	Local runoff management scenario design.
