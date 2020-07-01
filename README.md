# Investigation potential impacts of future dam development on protected areas around the globe
This repository contains the codes and files for a collaborative project with the World Wildlife Fund to understand the potential impacts of dam development on protected areas globally.

## Project Description
Dam construction over the past century has dramatically altered our landscapes, threatening ecosystems and endangered species around the world. Thousands of new dams are proposed globally that would affect protected areas such as National Parks, UNESCO World Heritage Sites, and United Nations Ramsar Sites. While data is publicly available, there is scant understanding of how these proposed dams will affect these critical protected areas. 

This project aims to understand how proposed dams could affect protected areas globally by (1) analyzing proposed dams by continent, (2) providing functions that combine protected areas datasets to create full datasets of protected areas by region, (3) calculating the difference between current and future degree of regulation for global rivers that overlap protected areas, (4) calculating the total length of rivers on protected lands and total area of protected lands that are affected by proposed dams by country, and (5) creating data visualizations of rivers by degree of regulation paired with protected areas.


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
The files in this repository comprise a global analysis of rivers combined with protected areas. We compare the current status with the planned future status of rivers, as measured by Degree of Regulation. For context on the primary dataset used (Free Flowing Rivers of the World), including background on Degree of Regulation as a measure of river health,  <a href="https://www.nature.com/articles/s41586-019-1111-9s" target="_blank">see this publication</a>.

### Notebooks
* exploration-notebooks/dam-impacts-on-protected-areas-calc-sam.ipynb: A JupyterNotebook that, for South America, (1) contains functions that combine World Database of Protected Areas and Ramsar Data for a country or continent to create a full protected areas dataset for the desired region (2) calculates the total length of rivers on protected lands and total area of protected lands that are affected by proposed dams by country for a desired continent (3) and provides a map of all current rivers and protected areas in all South America by Degree of Regulation. 
* exploration-notebooks/dam-impacts-on-protected-areas-calc-africa.ipynb: Same as JupterNotebook above but for Africa 
* exploration-notebooks/dam-impacts-on-protected-areas-calc-asia.ipynb: Same as JupyterNotebook above but for Asia.
* exploration-notebooks/dam-impacts-on-protected-areas-visualization.ipynb: A JupyterNotebook that creates three example maps for one country, with all rivers stratified by Degree of Regulation, (1) all current rivers and protected areas, (2) all current rivers that overlap protected areas, and (3) all projected future rivers that overlap protected areas.
* exploration-notebooks/explore-proposed-dams-and-ramsar-areas.ipynb A JupyterNotebook exploring the data for a preliminary analysis of FHReD and Ramsar Site data. Use this notebook to better understand proposed dams globally and how they overlap Ramsar protected areas.

### Presentations
* presentations/blog_final.ipynb: A JupyterNotebook with a short blog post of the findings of the final analysis.
* presentations/project_summary.pptx: A PowerPoint presentation with results of the final analysis.
* presentations/ea-python-dam-blog.ipynb: A JupyterNotebook with a short blog post of the findings of the preliminary analysis.
* presentations/ea-python-final-presentation.pptx: A PowerPoint presentation with results from the preliminary analysis.

## Run Workflow
This workflow will run each of the analyses notebooks. You can run the notebooks on their own and in any order.
1. Clone the repository https://github.com/stephlshep/global-dam-impacts.git, or download and decompress the zip file (see the green button for Clone or download).
2. Open a terminal and change directories to this directory: cd global-dam-impacts
3. Create the directories for the Figshare data to download to: "earthanalytics/data"
4. Open and run the preliminary analysis notebook to gain context on proposed dams that overlap Ramsar Areas globally: exploration-notebooks/explore-proposed-dams-and-ramsar-areas.ipynb
5. Open and run the dam impacts on protected areas calculation notebook to find the total length of rivers and total area of protected lands that are affected by proposed dams by country: 
exploration-notebooks/dam-impacts-on-protected-areas-calc.ipynb
4. Open and run the dam impacts visualization notebook to see summary figures on rivers on protected lands that are affected by proposed dams by continent and country: 
exploration-notebooks/dam-impacts-on-protected-areas-visualization.ipynb


## Example Usage
* Run dam-impacts-on-protected-areass-calc.ipynb: This will produce a pandas dataframe the total length of rivers on protected lands and total area of protected lands that are affected by proposed dams by country for whichever continent you choose. The notebook provdies code for Asia, Africa, and South America, you simply need to uncomment your selected continent and comment out deselected continents (running all three continents at once will likely crash your notebook!).
* Run dam-impacts-on-protected-areas-visualization.ipynb: This will present an example visualization of proposed dams affecting rivers in one specific country.
* Run ea-python-2020-final-project-shepherd-herwehe.ipynb: This will present graphs and analysis of proposed dams globally and an analysis of the area of Ramsar Sites affected by proposed dams for all countries in Africa.

## References
Lehner, B., C. Reidy Liermann, C. Revenga, C. Vörösmarty, B. Fekete, P. Crouzet, P. Döll, M. Endejan, K. Frenken, J. Magome, C. Nilsson, J.C. Robertson, R. Rodel, N. Sindorf, and D. Wisser. 2011. High-resolution mapping of the world’s reservoirs and dams for sustainable river-flow management. Frontiers in Ecology and the Environment 9 (9): 494-502.

Mulligan, M., van Soesbergen, A., Saenz, L. 2020. GOODD, a global dataset of more than 38,000 georeferenced dams. Scientific Data, 7(31). https://doi.org/10.1038/s41597-020-0362-5

Zarfl, C., Lumsdom, A. E., Berlekamp, J., Tydecks, L., Tockner, K. 2014. A global boom in hydropower dam construction. Aquatic Sciences 77.
https://doi.org/10.1007/s00027-014-0377-0

Kolbert, E. 2014. The Sixth Extinction. New York: Henry Holt and Company. 320 p.

Graf, W.L. 2001. Damage Control: Restoring the Physical Integrity of America’s Rivers in The Annals of the Association of American Geographers, 91(1), p. 1-27.

Nilsson, C., Reidy, C.A., Dynesius, M., Revenga, C.. 2014. Fragmentation and Flow Regulation of the World’s Large River Systems in Science, 308(5720), p. 405-408. DOI: 10.1126/science.1107887

McAllister, D.E., Craig, J.F., Davidson, N., Delany, S., Seddon, M. 2001. Biodiversity Impacts of Large Dams. International Union for Conservation of Nature and Natural Resource and the United Nations Environmental Programme Report. http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.392.9398&rep=rep1&type=pdf
