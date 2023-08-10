# Inspiration
Hurricane Harvey made landfall in August 2017, causing catastrophic flooding in the city of Houston, Texas, and surrounding areas. 107 lives were lost, over 1,000 homes were completely destroyed, and more than 17,000 sustained major damage.

Houston is known for its lack of zoning regulations, which allowed developers to build in flood-prone areas. As a result, many homes and businesses were destroyed by flooding during Hurricane Harvey. Zoning regulations that restrict development in flood-prone areas can help mitigate the damage caused by future flooding events.

Hurricane Harvey also highlighted the disproportionate impact of natural disasters on low-income and marginalized communities. Cities can work to address social vulnerability by investing in affordable housing, improving access to healthcare and other essential services, and engaging with community members to ensure that their needs are taken into account during emergency planning and response efforts.

# What it does
SurveySense utilizes two separate deep learning models: one for determining whether or not a structure has been affected by a natural disaster and another for automated land use and land coverage (LULC) maps.

The first model aids first responders by allowing the user to plug in real-time satellite imagery and detect affected regions.

In combination with the LULC maps, the two models allow for a user-friendly view of land usage in order to assess risk and potential improvements for future urban development.

# How we built it
The natural disaster survey model was trained on satellite imagery of Hurricane Harvey sourced from Kaggle, using binary classification. The result was a model which allows the user to upload an image and returns an accurate analysis of the region within seconds.

The LULC identification model was trained on satellite imagery sourced from EuroSAT and Google Earth Engine, using RGB image classification. The result was a model which allows the user to request satellite images from certain regions, segment the image into 64x64 chunks, and use the LULC model to accurately label them. A GeoJSON file is returned with the predicted labels, which is then visualized using kepler.gl.

# Challenges we ran into
Hardware and network limitations were definitely unforeseen challenges that we ran into. Our original plan included connecting to a virtual machine, which would allow us to not only train our models to be more accurate, but also process far more data. However, due to network limitations, we were unable to establish a solid connection and had to pivot to a more hardware and network-friendly project.

# Accomplishments that we're proud of
We are extremely proud of our natural disaster survey model, which was created from scratch! Additionally, we are proud of finding a way to visualize LULC data in an easily interactable way.

# What we learned
We both learned a lot about applying our ML knowledge to satellite imagery, targeted toward a specific societal cause.

# What's next for 98 - SurveySense
Implementing more advanced object detection models and being able to process larger data sets with the LULC model, and analyzing changes over time.
