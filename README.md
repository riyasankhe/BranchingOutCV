# BranchingOutCV
This repository leverages the TreePedia 2.0 model to measure greenery levels in neighborhoods using the GVI metric. Our pipeline uses Google Street View (GSV) images to generate datasets and evaluate greenery, providing a scalable, data-driven approach to identify and address vegetation inequities.

# Workflow 
----

## Step 1: Sample Coordinates in Your Desired Neighborhood

Use the "Sampling Points" file to generate a set of random geographic coordinates along streets for the purpose of extracting Google Street View images. The process involves leveraging shapefiles and spatial data in QGIS to sample random points.

<p align="center">
  <img width="200" alt="Picture1" src="https://github.com/riyasankhe/BranchingOutCV/assets/75983989/13e3d52b-ae47-4cdd-8400-60ac97e998d3"><br>
  <em>Example of Roland Park street map with selected points</em>
</p>

## Step 2: Retrieve Images and Generate Predictions 

Use the file "Retrieve_Images_and_Generate_Predictions.ipynb" file to generate GSV images from your set of points and generate GVI predictions for them. We use the latitude and longitude of each point to query the Google Static API using custom parameters, and then feed the images into the Treepedia 2.0 ResNet model after appropriately resizing the images. The model outputs predictions that are saved to a CSV file by neighborhood for further analysis and visualization.

<p align="center">
  <img width="400" alt="Roland_Park" src="https://github.com/riyasankhe/BranchingOutCV/assets/75983989/6439923e-523b-41ff-8dde-f5958271b0ad"><br>
  <em>GVI Prediction: 0.404</em>
</p>
