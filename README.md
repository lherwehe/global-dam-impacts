# Investigation potential impacts of future dam development on protected areas around the globe
This repository contains the codes and files for a collaborative project with the World Wildlife Fund to understand the potential impacts of dam development to protected areas globally.

## Project Description
Dam construction over the past century has dramatically altered our landscapes, threatening ecosystems and endangered species around the world. Thousands of new dams are proposed globally that would affect protected areas such as National Parks, UNESCO World Heritage Sites, and Ramsar Sites. While data is publicly available, there is scant understanding of how these proposed dams will affect these critical protected areas. This project aims to understand how proposed dams could affect protected areas globally.

## Tools & Packages
* Numpy
* Pandas
* Matplotlib
* Geopandas
* Earthpy
* Shapely
* Contextily


## Data Sources
### Figshare Site
To maximize reproducibility, all of the data used for this project is stored on Figshare. This means that you do not need to download any data prior to running the notebook, the JupyterNotbook script will download the data.

* Free flowing rivers current Degree of Regulation
    * url="https://ndownloader.figshare.com/files/23273213"
* Free flowing rivers future Degree of Regulation
    * url="https://ndownloader.figshare.com/files/23273216"
* World Database of Protected Areas - split by continent
    * url="https://ndownloader.figshare.com/files/23354894"
* Ramsar Sites
    * url="https://ndownloader.figshare.com/files/22507082"
* Future Hydropower Reservoirs and Dams (FHReD)
    * url="https://ndownloader.figshare.com/files/22486157"
* Country Boundaries
    * url="https://ndownloader.figshare.com/files/22507058"
* Continent boundaries
    * url="https://ndownloader.figshare.com/files/23392280"
* Country ISO3 codes & Continents
    * url="https://ndownloader.figshare.com/files/23393756"


### Original Data
* Free Flowing Rivers Current & Future - https://www.nature.com/articles/s41586-019-1111-9
    * This dataset contains a shapefile with all rivers from around the world and their current and projected degree of regulation.
* World Database of Protected Areas (WDPA) - https://www.protectedplanet.net/
    * This dataset contains a shapefile with protected areas from around the world.
* GlObal geOreferenced Database of Dams (GOODD) - http://globaldamwatch.org/goodd/
    * This dataset contains the geographic locations of dams identified from Google Earth's satellite data. 
* Global Reservoir and Dam Database (GRand) - http://globaldamwatch.org/grand/
    * This database collates record for dams and river around the globe form multiple sources.  The data set is curated by McGill University, Canada.
* Future Hydropower Reservoirs and Dams (FHReD) - http://globaldamwatch.org/fhred/
    * Geographic database of dams > 1MW that are planned or underconstruction.
* Ramsar Site Database - https://rsis.ramsar.org/)
    * This database contains a shapefile of wetland areas of critical importance as identified under the Convention on Wetlands (1971).
    

## Repository Files
The files currently in the repository comprise our preliminary analysis of the FHReD and Ramsar Site data, done for the spring 2020 Earth Analytics course.
 
### Notebooks
* exploration-notebooks/dam-impacts-on-pas-by-length-area-impact-by-country-continent.ipynb: A JupyterNotebook exploring the data for the preliminary analysis.
* exploration-notebooks/dam-impacts-on-pas-example-visualization.ipynb: A JupyterNotebook exploring the data for the preliminary analysis.
* exploration-notebooks/explore-proposed-dams-and-ramsar-areas.ipynb A JupyterNotebook exploring the data for the preliminary analysis.

### Presentations
* presentations/ea-python-dam-blog.ipynb: A JupyterNotebook with a short blog post of the findings of the preliminary analysis.
* presentations/ea-python-final-presentation.pptx: A PowerPoint presentation with results from the preliminary analysis.

## Run Workflow
This workflow will run our preliminary analysis of the FHReD and Ramsar Site data.
1. Clone the repository https://github.com/stephlshep/global-dam-impacts.git, or download and decompress the zip file (see the green button for Clone or download).
2. Open a terminal and change directories to this directory: cd global-dam-impacts
3. Create the directories for the Figshare data to download to: "earthanalytics/data"
4. Open and run the preliminary analysis: presentations/ea-python-2020-final-project-shepherd-herwehe.ipynb


## Example Usage
* Run ea-python-2020-final-project-shepherd-herwehe.ipynb: This will present (1) graphs and analysis of proposed dams globally, (2) a function that overlays proposed dams on Ramsar sites and calculates the total affected area for a particular country, (3) an analysis of the area of Ramsar Sites affected by proposed dams for all countries in Africa.

## References
Lehner, B., C. Reidy Liermann, C. Revenga, C. Vörösmarty, B. Fekete, P. Crouzet, P. Döll, M. Endejan, K. Frenken, J. Magome, C. Nilsson, J.C. Robertson, R. Rodel, N. Sindorf, and D. Wisser. 2011. High-resolution mapping of the world’s reservoirs and dams for sustainable river-flow management. Frontiers in Ecology and the Environment 9 (9): 494-502.

Mulligan, M., van Soesbergen, A., Saenz, L. 2020. GOODD, a global dataset of more than 38,000 georeferenced dams. Scientific Data, 7(31). https://doi.org/10.1038/s41597-020-0362-5

Zarfl, C., Lumsdom, A. E., Berlekamp, J., Tydecks, L., Tockner, K. 2014. A global boom in hydropower dam construction. Aquatic Sciences 77. https://doi.org/10.1007/s00027-014-0377-0