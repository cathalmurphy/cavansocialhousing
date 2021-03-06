# **Site selection for social housing in Cavan**


## **Table of contents**
* [Chapter 1: Background and context](#chapter-1--background-and-context)
    + [1.1: Project Outline](#11--project-outline)
    + [1.2: Why ghost estates?](#12--why-ghost-estates-)
    + [1.3: Typically-associated datasets](#13--typically-associated-datasets)
* [Chapter 2: Spatial data and criteria specification](#chapter-2--spatial-data-and-criteria-specification)
    + [2.1: Data sources](#21--data-sources)
    + [2.2: Projection problems](#22--projection-problems)
    + [2.3: Creating spatial datasets for Cavan](#23--creating-spatial-datasets-for-cavan)
* [Chapter 3: Modelling criteria](#chapter-3--modelling-criteria)
    + [3.1: Modelling factors and constraints](#31--modelling-factors-and-constraints)
    + [3.2: Factor: Distance to towns](#32--factor--distance-to-towns)
    + [3.3: Factor - Distance to lakes](#33--factor---distance-to-lakes)
    + [3.4: Factor - Distance to sports and leisure facilities](#34--factor---distance-to-sports-and-leisure-facilities)
    + [3.5: Factor - Distance to major roads](#35--factor---distance-to-major-roads)
    + [3.6: Factor - distance from mineral extraction sites](#36--factor---distance-from-mineral-extraction-sites)
    + [3.7: Constraint - Protected heritage areas](#37--constraint---protected-heritage-areas)
    + [3.8: Constraint - Bogs and marshes](#38--constraint---bogs-and-marshes)
    + [3.9: Constraints - Slopes](#39--constraints---slopes)
* [Chapter 4: Final suitability raster](#chapter-4--final-suitability-raster)
    + [4.1: Weighing criteria](#41--weighing-criteria)
    + [4.2: Final suitability raster](#42--final-suitability-raster)
    + [4.3: Summary of results](#43--summary-of-results)
    + [4.4: Potential impacts](#44--potential-impacts)
* [Chapter 5: Conclusion](#chapter-5--conclusion)
    + [5.1: Possible improvements and technical difficulties](#51--possible-improvements-and-technical-difficulties)
    + [5.2: Concluding remarks](#52--concluding-remarks)
* [Bibliography](#bibliography)

## **List of tables and figures**
* [Table 1: List of criteria by type and weight](#table1)
* [Table 2: Degree of slope and development potential](#table2)
* [Table 3: Distribution of unfinished estates by suitability band](#table3)
* [Figure 1: Map for distance to towns and villages](#figure1)
* [Figure 2: Map for distance to lakes](#figure2)
* [Figure 3: Map for distance to sports and leisure facilities](#figure3)
* [Figure 4: Map for distance to major roads](#figure4)
* [Figure 5: Map for distance to mineral extraction sites](#figure5)
* [Figure 6: Final MCE Suitability Index with unfinished estates point file overlain](#figure6)


## <a name="chapter-1--background-and-context"></a>**Chapter 1: Background and context**
### <a name="11--project-outline"></a>1.1: Project Outline
The first step involved in this project was the most important one – to choose what kind of sites would have their suitability mapped using MCE methods. A number of possible options held interest for the study area, Cavan, but were ultimately dismissed because of a difficulty locating comprehensive information, in particular, an MCE study that would have mapped suitable sites for fracking in the county. Ultimately I decided to model something which has generated a large amount of discussion, both nationally and globally, in the recent period – housing. In particular, I wanted to explore the possibilities Cavan held for social housing, and explore the possibility utility of GIS and multi-criteria evaluation in the process of planning social housing. I planned to use a combination of factors and constraints to produce a map which would grade different areas on the county on their suitability for any possible social housing projects. In addition, I wished to see how MCE could be brought to bear on recent proposals (and small-scale philanthropic actions) to use existing “ghost estates” – unfinished estates abandoned in the wake of the Irish financial crisis – as both social housing and as a source of possible economic stimulus.

Cavan may seem like a strange choice as a location for the construction of new housing stock – 6.0% of its stock is currently on the market, the highest of any county nationally (Griffin, 2014) – and the area is relatively remote and not a major population centre in a period where population (both in Ireland and globally) is focused more and more around the major cities (nationally, Dublin and Cork, globally, New York, London, Paris, and Hong Kong) (Kuper, 2013), yet even though the practical use of an MCE project on housing in Cavan may be limited, there is a generalizability which I think offers this project a very real use-value. Although it is unlikely (and not really practical) to use state funds to redevelop housing (Kerr & Melia, 2009) in a place like Cavan, this project can be seen as a kind of pilot program – showing, firstly, how a real public good can be achieved by finishing the construction of selected ghost estates (and the project would satisfy a variety of political constituencies, socialist, Keynesian, etc.), and that GIS and MCE methods could offer an invaluable aid in the early stages of any such project.


### <a name="12--why-ghost-estates-"></a>1.2: Why ghost estates?
After the initial site-type for this project – housing – had been chosen, the next step was to think through how the site-type would be mapped. The types of spatial data typically associated with a project are discussed below, in section 1.3, but also offered here is a brief explanation of what ghost estates are, and why they were chosen for this project.


Put briefly (but less briefly than in section 1.1), ghost estates are a phenomenon associated with the 2008 Global Financial Crisis which is especially prominent in Ireland. The term was first coined in 2006 by economist David McWilliams (McWilliams, 2006), but really came to the public’s attention from 2008 on (Henley, 2010). Ghost estates are residential developments which secured planning permission and had construction work initiated, but were abandoned by the developers, or the bank, when either the developer could no longer afford payments on the loan securing the site, or walked away from the site as house values had been depressed to the point where selling the residences on the development would no longer cover the amount remaining on the loan. These estates are typified by incomplete or non-existent infrastructure, a lack of promised services and facilities, an abundance of environmental and health hazards, and extreme isolation for the families who had bought early on these developments.


A large number of these sites were repossessed by NAMA in the wake of its establishment after the GFC, and what was to be done with these sites generated a range of responses, but the ones of interest here were the Keynesian and socialist responses, which, with the former, emphasized the possibility of using the estates as a form of economic stimulus, with construction work on the sites generating a large amount of employment (both skilled and unskilled) and revitalizing a failing economy, and, with the latter emphasizing the large number of unfinished estates (with the deeds now owned by the public) compared to the number of homeless, etc., in the country (Gleeson & Kitchin, 2010). A combination of these approaches seemed to hold some potential, and thus the project should be seen as generally following that line of argument in terms of policy.


Cavan is actually quite a good site for an exploration of this policy and the application of a (theoretical) pilot project, as it has one of the highest numbers of ghost estates in the county, per county, proportional to the total of the county’s housing stock. This means there are a large number of potential sites in the county, allowing for more precision in demonstrating the utility of MCE and GIS to this project in locating the estates in Cavan most suitable for any possible redevelopment.


### <a name="13--typically-associated-datasets"></a>1.3: Typically-associated datasets
The datasets typically associated with MCE studies of housing generally focus around pre-existing built space, and a select number of important physical geographical features like rivers and lakes. Most of this spatial data was contained within one particular dataset which was used extensively throughout the project – the CORINE2006 dataset, which maps land use according to a set of categories which are standardized across the EU. The other datasets typically associated with GIS applied to planning are road layers, and again these were included in the initial archive of spatial datasets that came with the project brief. A more detailed breakdown of the datasets used in this project, and the process involved in creating additional datasets, are discussed in chapter 2.

## <a name="chapter-2--spatial-data-and-criteria-specification"></a>**Chapter 2: Spatial data and criteria specification**
### <a name="21--data-sources"></a>2.1: Data sources
Most of the spatial data used in this project was acquired from Ronan Foley, who uploaded a zip archive containing national data sets (along with county-level spatial data for rivers and protected areas) specifically for use in this MCE project. The only other data I required was a shapefile displaying the locations of unfinished estates in Ireland as points, so that individual estates could be overlain on the final suitability raster, allowing for the identification of the most suitable estates for completion.


Searching for pre-existing spatial data on this subject (it was not viable to compile a spatial dataset on this subject myself) I found a project compiled by AIRO, which was offered freely in shapefile format, presenting the results of the 2010 DEHLG survey of unfinished estates nationally (All-Ireland Research Observatory, 2010). The shapefile included 2,846 unfinished estates, and importantly, also contained a detailed attribute table, breaking down the status of each estate by a number of criteria, including the percentage of houses and roads/infrastructure completed on an estate-by-estate basis, which was highly useful for a project such as this.


### <a name="22--projection-problems"></a>2.2: Projection problems
The first significant problem I encountered in this project pertained to mismatched geographical projections between individual spatial datasets. The shapefiles used covered 3 separate projections, and some transformation and re-projection work was required before the final Cavan files could be created. Without these transformations, the Unfinished Estates shapefile in particular became problematic – it would appear far off on the northeast of the map viewer from the rest of the files, which all (bar one) were set to no projection.  I made several attempts to solve the problem using ArcToolbox’s available tools in its Projections and Transformations toolset, cycling through the possible projections the files could have been set to, before learning that the files had no actual projection set. At this point, the problem was solved by adding the spatial layers in a particular order. Although most of the national datasets had no projection set, they did match up exactly with the CORINE2006 shapefile, which did have a projection set. By adding the CORINE2006 shapefile first, I was given the option to reproject and transform all subsequent spatial layers added to match its projection, including with the Unfinished Estates shapefile, using an automated transformation stored in its database.


Even though adding spatial layers in a particular order solved the main problem with mismatching projections, ArcMap’s solution to the problem was imperfect, and placed strict limits on what would later be possible with the project. In particular, attempting to use ArcMap’s built-in base maps option meant simply that some of the shapefiles would project correctly onto the added base map layer while others, their zero point being pegged literally in X,Y co-ordinates as (0, 0) would be projected at OpenStreetMap’s own zero point off the west coast of Africa.


However, for the purposes of this project, the use of basemap layers was not strictly necessary, although they would have enhanced some of the detail and resultant commentary around the section of the project dealing with towns and villages. All that was necessary for the scope of this project was to ensure that the AIRO Unfinished Estates shapefile was correctly projected onto the same extent as the initial shapefiles – although it took a lot of trial and error to get this to work correctly, once I had worked out the process it was achieved very quickly and in a very straightforward manner.


### <a name="23--creating-spatial-datasets-for-cavan"></a>2.3: Creating spatial datasets for Cavan
This project was given a very open brief, having only 2 requirements – firstly, that it involve the use of Multi-Criteria Evaluation in the evaluation of a particular problem (of my own choosing – in this instance, social housing and unfinished estates), and that the area under evaluation be County Cavan. However, the files I was given to work with for this project contained data at the national level, covering the Republic of Ireland, and, with one file, all of the island of Ireland itself. Thus, before I could begin designing and implementing an MCE for Cavan, I had to process the national data sets to extract only the spatial data pertaining to Cavan itself.


The first step in extracting only the Cavan data from each national spatial layer was to create a single Cavan shapefile against which these other layers could be clipped using ArcMap’s geoprocessing tools. This was done using the IrelandLA shapefile – the Selection by Attributes function was used to select only Cavan from the layer, and then a layer was created from this selection, and the layer in turn was exported as a shapefile which now contained only 1 polygon which represented only Cavan.


From here, this new file, Cavan_County.shp, could be used as the source layer for all subsequent clipping, intersection, and selection by location tasks to extract Cavan data from the other spatial layers. Select by Location was used for some of the layers whose polygons at least partially exceeded the boundaries of County Cavan, for example, the layers containing the 3 types of protected areas, as this allowed for the extraction of any features from a layer where there was even the slightest intersection with the source layer representing Cavan. Elsewhere, clip was used where possible, as it ensured that only spatial objects in the target layer which was overlain by the source layer’s extent (Cavan) was extracted and output as a new layer, which was given a name indicating its location and the features contained within (e.g., Cavan Lakes).


In total, using the Cavan_County.shp created using selection by attribute, 9 other Cavan-only files were extracted from national-level spatial layers, while some other layers (e.g. rivers, natural heritage areas, special areas of conservation, and special protection areas) came pre-prepared, containing only spatial data for features that were overlain by the county of Cavan. Only after these files had been prepared from the Ireland-wide files was it possible to proceed unto the bulk of the project itself – the Multi-Criteria Evaluation.


## <a name="chapter-3--modelling-criteria"></a>**Chapter 3: Modelling criteria**
### <a name="31--modelling-factors-and-constraints"></a>3.1: Modelling factors and constraints
The brief for this project specified that the final MCE calculation had to include a minimum of 3 criteria, of which 2 had to be factors. However, examining the various factors at play in real-life examples of site-selection for social housing, it was determined that several more factors and constraints would be required than the minimum the project brief stipulated. After an examination of the spatial datasets available, previous MCE studies on housing, and the nature of the environment being studied, a total of 8 criteria were selected, 5 factors and 3 constraints, listed in the table below. Discussions of the different criteria, and technical descriptions of the processes involved in their creation (and the creation of the final normalized layers which would be used in the final MCE calculation), are discussed in the rest of chapter 3, while the weightings visible in the table below are discussed in the first section of chapter 4.


<a name="table1"></a><p align="center">

**Criterion**|**Type**|**Weight**
:-----:|:-----:|:-----:
Distance to towns and villages|Factor|0.3
Distance to bodies of water|Factor|0.1
Distance from mineral extraction sites|Factor|0.2
Distance to major roads|Factor|0.2
Distance to sports/leisure facilities|Factor|0.2
Not located in protected area|Constraint|N/A
Not located on bog or marshland|Constraint|N/A
Slope not greater than 15%|Constraint|N/A

***Table 1: List of criteria by type and weight***

</p>


### <a name="32--factor--distance-to-towns"></a>3.2: Factor: Distance to towns
The first normalized factor raster that was created was for distance to towns and villages, and there were a number of technical steps involved. Firstly, it was necessary to create a spatial layer which consisted only of polygons representing major towns and villages within Cavan. This was done by using Selection by Attributes on the CORINE 2006 shapefile. First, the CORINE category for “discontinuous urban fabric” – signifying towns and villages – was identified, and then isolated from the map using the selection tool (CODE_06 = 112), with the selection then being created as a new layer, Cavan Towns.shp.


With a layer for towns and villages now created, it became possible to create a distance raster which would calculate the distance in meters to the nearest town or village for every point in Cavan County, using the Spatial Analyst – Distance – Euclidian Distance tool in ArcToolbox. However, Cavan’s shape and the nature of raster calculation meant that a distance value would be calculated for every pixel within an X, Y range where the range for X was the northern- and southern-most points of Cavan and Y’s range was, correspondingly, the western- and eastern-most points. This was not a problem, firstly because it was possible to raise the initial Cavan county shapefile (with its colour set to hollow) to the top of the table of contents, allowing us to see where the raster exceeded Cavan’s borders, and the actual range of distances for each point in Cavan to be estimated. The distance raster discussed here was output using the Euclidian Distance tool as TownDist.


A look at the file details in the table of contents indicated that the distances from towns for the raster ranged from 0 to 35274.9 meters. However, this raster was not usable in the final MCE calculation – it was still necessary to normalize this raster, returning a file which would recalculate the distances along a scale whose range would match up with those of the other normalized rasters being used – i.e., it would stretch from 0 on the low end to 1 on the high end. Using the fxcalculation spreadsheet I had obtained for use in an earlier MCE exercise, I designed a formula that would return a value of 1 for pixels that were located in discontinuous urban fabric (i.e., they had a distance score of 0 meters) and a value of 0 for pixels located roughly 35 kilometres away from any Cavan town or village. This formula took the form of $\frac{-TownDist}{35300} + 1$, with 35300 being chosen as the upper limit as a rounding up of 35274.9, to avoid assigning any one pixel a value of 0 and thus excluding it from any final suitability calculation.


The nature of the raster, however (i.e. that a decent proportion of it was outside of the boundaries of Cavan), meant that, practically speaking, this wouldn’t actually have been a problem, as the pixels located on the extreme high-end of the spectrum of initial distance values were outside the boundaries of Cavan and would have ultimately been excluded anyway by the constraint rasters. Secondly, again speaking practically, it would not have been useful to ascertain the range of values within Cavan itself, as realistically even locations in Cavan which were quite remote from towns were not, strictly speaking, totally undesirable because of this. On this basis, ascertaining a more limited range which pertained only to Cavan and not the processing extent was judged irrelevant to the normalization of the raster. The normalized output raster was named “C3”, as at this point two of the three constraint rasters had been created, C1, and C2 (with C standing for criterion).


<a name="figure1"></a>


![Map for distance to towns and villages](https://raw.githubusercontent.com/cathalmurphy/cavansocialhousing/master/Fig1Towns.png)
***Figure 1: Map for distance to towns and villages***


### <a name="33--factor---distance-to-lakes"></a>3.3: Factor - Distance to lakes
The creation of a normalized raster for distance to water presented, almost immediately, a choice to be made – there were 2 shapefiles I had created for water bodies in Cavan, and both stored different types of spatial objects, meaning combining both was not possible, either through using ArcMap’s edit tools, or Merge and Union geoprocessing tools. Other options were theoretically available (e.g. Shape2SQL and SQL Server) but were judged ultimately as far too unwieldy and time-consuming relative to the importance of this factor to the overall project.


Ultimately, it was decided that the Cavan Lakes shapefile (created using Select by Location on the national Lakes dataset with the Cavan polygon as the source layer), would serve as the basis for this distance raster, as it was judged to represent the most meaningful control on desirability with proximity from the types of water bodies available. An outputted distance raster called LakesDist was created using ArcToolbox’s Euclidian Distance tool, as with the Distance to Towns and Villages raster. A brief analysis of the raster layer as it appeared in the Table of Contents showed the range of distances went from 0 to 32482.7 meters.


The fxcalculation spreadsheet was then used again to work out a formula that would normalize this distance raster so that it could be used with other distance rasters in the final MCE weighed calculation. The maximum value, as with towns and villages, was rounded up, to ensure that no pixel would get a 0 value which would falsely and unfairly exclude it from the final MCE calculation and thus distort the results, with 32482.7 being rounded up to 32500. The equation used took the form of $\frac{-LakeDist}{32500} + 1$, with the output raster produced being labelled C4, ready for use in the final MCE calculation.


<a name="figure2"></a><p align="center">

![Map for distance to lakes](https://raw.githubusercontent.com/cathalmurphy/cavansocialhousing/master/Fig2Lakes.png)
***Figure 2: Maps for distance to lakes***

</p>


### <a name="34--factor---distance-to-sports-and-leisure-facilities"></a>3.4: Factor - Distance to sports and leisure facilities
The creation of a normalized raster measuring distance from sports and leisure facilities involved many of the same steps as the creation of the raster for distance to towns and villages. As with before, it was first necessary to use Selection by Attributes and Export Data to create a separate shapefile for sports and leisure facilities from the CORINE 2006 dataset. First, the CORINE legend that came with the project files was consulted to identify the attribute for sports and leisure facilities – CODE_06 = 142. Then, when the separate shapefile had been created containing only areas of the CORINE dataset that had this attribute, the Euclidian Distance calculator in ArcToolbox was used to create a new raster called SportsDist, showing the distance for every point in the processing extent to the nearest sports and leisure facility. The same problems with processing extent as outlined in 3.2 also apply here, but as with 3.2, this was not thought to be a large detriment to the final calculation and so no action was taken to get a more specific range of distance values.


A quick look at the file’s display on ArcMap’s table of contents showed that the distance values for this raster ranged from 0 to 49097.3 meters. Using the fxcalculation spreadsheet obtained earlier, a formula was obtained for creating a normalized raster for these distance values, taking the form of $\frac{-SportsDist}{49100} + 1$. Again, no pixel in Cavan would not actually return a value of 1, but this was not judged to be a problem as it would distort the final result to exclude remote areas of Cavan on this basis, with it being preferable to instead give them a low non-zero suitability score in this factor. The formula was input into the Raster Calculator tool in ArcToolbox and the normalized output raster was named C5.


<a name="figure3"></a><p align="center">

![Map for distance to sports and leisure facilities](https://raw.githubusercontent.com/cathalmurphy/cavansocialhousing/master/Fig3Leisure.png)
***Figure 3: Maps for distance to sports and leisure facilities***

</p>


### <a name="35--factor---distance-to-major-roads"></a>3.5: Factor - Distance to major roads
The process of creating the rasters for the distance to major roads in Cavan varied significantly from the process of creating the other factor rasters in a number of ways. Firstly, not only was the CORINE dataset not being used in any way, but there were several road shapefiles which needed to be considered. There were a total of 4 road shapefiles which had spatial objects located within Cavan – with the Dual Carriageways file being discarded in the process of clipping, earlier on in the project, leaving only National, Secondary, Regional, and Unclassified. After analysing the parts of the remaining road files pertaining to Cavan, it was decided to use only the National and Secondary layers for use in the distance to roads calculation. Firstly, because the Regional roads were judged to not be of major significance in determining the suitability of a site (a site’s desirability, especially in rural areas such as Cavan, is determined far more by its proximity to a “main road”, rather than to a regional one (MacCabe, 2000)), and the Unclassified category was excluded because the lack of any significant data about the nature of the roads in question made it hard to determine how major they were and how much they would contribute to the suitability of a site.


After the relevant road layers to be used in the distance calculation had been selected, it was then necessary to amalgamate them into a single shapefile using the Merge tool, creating a single shapefile containing all of the objects contained within both the National and Secondary datasets – CavanRoadsMerge.shp. Then, the Euclidian Distance calculator was used to calculate the distance from these roads for every pixel within the processing extent, stored as a raster called RoadsDist. A brief analysis of the file indicated the range of distance values went from 0 to 43790.5 meters.


With the range of values for distance known, it was now possible to use the fxcalculation spreadsheet to design a formula which would create a 2nd raster, which would normalize these distance values. This formula was determined to be $\frac{-RoadsDist}{43800} + 1$, with 43800 being rounded up from the actual maximum to again ensure that no pixel within Cavan would distort the final MCE calculation by being excluded from it on the basis of a factor. This formula was inputted into the Raster Calculator tool and the output file was named C6, and this normalized raster was added to the map document.


<a name="figure4"></a><p align="center">

![Map for distance to major roads](https://raw.githubusercontent.com/cathalmurphy/cavansocialhousing/master/Fig4MajorRoads.png)
***Figure 4: Maps for distance to major roads***

</p>


### <a name="36--factor---distance-from-mineral-extraction-sites"></a>3.6: Factor - distance from mineral extraction sites
The creation of the distance raster for mineral extraction sites was slightly different than the creation of the other rasters, as here suitability increased with distance, rather than decreasing as with the other 4 factors, which would necessitate a different general form of equation than the one used to normalize them ((-Raster/MaxDistance) + 1). The technical steps, however, were the same as before. First, the CORINE code for mineral extraction sites was obtained from the accompanying legend (131) and all mineral extraction sites were selected from the Cavan_CORINE shapefile using Select by Attributes, with the selection resulting from this query being exported as a new shapefile.


Then, the Euclidian Distance tool was used to calculate the distance from these sites for each pixel within the Cavan processing extent, with the distance raster being outputted as MinExtDist. A brief examination of the new raster showed that the distance values ranged from 0 to 50676.9 meters.


After this, it was necessary to determine the equation that would be input into the Raster Calculator to obtain a normalized distance raster. Whereas the previous fxcalculation formulas gave a score that increased with proximity, here the opposite was desired, so the formula did not require the inversion of distance used in the others, and thus (because no value below zero would be given as in the standard formula), the +1 was also not required. The formula took the form of $\frac{-MinExtDist}{51000} + 1$, and when input into the Raster Calculator produced the normalized output raster C7, the final normalized factor raster to be created for this project.


<a name="figure5"></a><p align="center">

![Map for distance to mineral extraction sites](https://raw.githubusercontent.com/cathalmurphy/cavansocialhousing/master/Fig5MinExtr.png)
***Figure 5: Maps for distance to mineral extraction sites***

</p>


### <a name="37--constraint---protected-heritage-areas"></a>3.7: Constraint - Protected heritage areas
A number of factors were considered in determining what constraints would be included in the final MCE calculation. Firstly, it was decided that, due to the nature of the project, none of the constraints would strictly reflect existing planning and zoning laws and regulations – since we were dealing with existing unfinished housing estates, this necessarily meant they had already obtained planning permission, so instead the constraints were designed to determine which areas of Cavan would be especially unsuitable for continued construction or redevelopment. 3 constraints were chosen, all of which pertained to physical geography and/or legal status. The first constraint, of which the technical details are discussed in this section, was that a site could not fall within any of the 3 categories of protected area – Natural Heritage Area, Special Area of Conservation, and Special Protection Area.


After these shapefiles were all added to the Cavan map, they were turned into a single “Protected Areas” shapefile using the merge tool. Then, the Symmetrical Difference tool was used with this amalgamated file and the Corine2006 file, with the output raster, SPADiff, returning as its area only the parts of the 2 files that didn’t overlap (i.e., the area of Cavan that was not any of the 3 areas and the parts of the protected areas that lay outside of Cavan). I had also included a new attribute field for both files, assigning a value of 1 to the Corine layer and 0 to the Protected Area layer, thus ensuring that in any subsequent raster conversion, only locations within Cavan would have a value of 1 and thus be included in the final calculation.


The next step was to convert this new feature class into a raster file, using the Feature to Raster conversion tool and selecting the aforementioned Boolean attribute field (Not_SPA) as the field, and outputting the raster as C1 – with all pixels within Cavan county not lying within one of the 3 protected areas having an attribute value of 1, meaning the file was now ready to be used as a constraint in the final MCE calculation.


### <a name="#38--constraint---bogs-and-marshes"></a>3.8: Constraint - Bogs and marshes
The 2nd constraint chosen pertained to the physical geography of the region, being selected on the basis that a site having the characteristics defined in the constraint would make it unviable for any further development (if, in fact, any site had been begun on any area meeting the constraint). This constraint was that the land could be neither a bog or a marsh, as identified by the CORINE shapefile, which contained land use codes for both peat bogs (412) and inland marshes (411). The SQL query tool built into ArcMap did not allow for the selection of two attributes at once. Thus, it was necessary to select by attribute twice: first, selecting peat bogs using CODE_06, and then returning to the Select by Attribute screen a second time, this time setting the selection (CODE_06 = 411) to add to the existing selection. This dual selection was then exported as a new shapefile, BogsMarshes.


The next step was to again use the symmetrical difference tool with the new BogsMarshes against the Corine2006 shapefile, producing a new output vector file, NotBogsMarshes, which contained only the parts of Cavan which were not designated as a peat bog or inland marsh by the CORINE land use codes.


The final step was to first add a new attribute field to the NotBogsMarshes file, and calculate the field values so that every row was assigned a value of 1. Then, with this done, the Feature to Raster conversion tool was used, with the new attribute field, NotBM, used as the relevant value. The output raster was named C2, and added to the table of contents.


### <a name="39--constraints---slopes"></a>3.9: Constraints - Slopes
The final constraint selected was slope, and again the process involved in the creation of the constraint raster in this case varied significantly from the other two, especially insofar as it did not at any point involve the use of any vector data, whereas with the other 2 constraints, the raster was calculated initially on the basis of polygon-based vector data. The initial file used in calculating the slope raster was a Digital Elevation Model for Ireland at a 90 meter resolution, which gave the elevation in meters above sea level for every point down to this resolution in Ireland.


The first step in preparing the slope constraint was to clip the DEM file so only the portion of it overlain by Cavan would be retrieved. This was done using ArcMap’s geoprocessing tool, Clip, and the new Cavan only DTM was output as a separate file. Then, the Slope tool (found in ArcToolbox under Spatial Analyst > Surface) was used to calculate the slope of every pixel from the elevations given by the DEM. This slope file was output as a separate file, CavanSlope.


Then, with the slope calculated in degrees for every pixel within the processing extent, pre-existing studies on the relation of slope to construction and housing development were studied to ascertain the ideal cut-off point for the constraint raster which was to be made, with any slope degree above the cut-off point assigning the pixel a value of 0, designating it as unsuitable for further development and giving it a value of 0 in the final suitability raster.


The report that was the main influence in the determination of the cut-off point was a November 2008 report on Guide and Model Regulations for Steep Slopes published by the Lehigh Valley Planning Commission. On page 5 of this report, there is a table, Table 1: Degree of Slope, itself based on earlier studies and soil surveys from 1963 and 1974, which gives a general guide to the development potential of a site based on its slope, except here slope is given in percentage rather than in degrees. The table is attached below.


<a name="table2"></a><p align="center">

**Degree of slope**|**Development Potential**
:-----:|:-----:
0-3%|Generally suitable for all development and uses.
3-8%|Suitable for medium density residential development, agriculture, industrial and institutional uses.
8-15%|Suitable for moderate to low-density residential development, but great care should be exercised in the location of any commercial, industrial or institutional uses.
15-25%|Only suitable for low-density residential, limited agricultural and recreational uses.
>25%|Only used for open space and certain recreational uses.
***Table 2: Degree of slope and development potential (Lehigh Valley Planning Commission, 2008)***

</p>


Ultimately, the cut-off point was chosen as 15%, as below this level land is safe for “moderate to low-density residential” development, a category into which the unfinished estates generally fit, and the other factors in the MCE calculation already account for things like infrastructure and proximity to commercial-zoned land, etc. However, as mentioned before, our slope raster was in degrees, so it was necessary to use an online percentage-to-degrees slope conversion calculator to obtain the figure in degrees that corresponded to a 15% slope – 8.53 degrees.


A formula was then input into the raster calculator that would assign a value of 1 to all pixels in the slope raster whose value was less than 8.53, with all pixels whose value was greater being assigned a value of 0. This raster was outputted as C8 and added to the map document, to be used in the final MCE calculation.


## <a name="chapter-4--final-suitability-raster"></a>
### 4.1: Weighing criteria <a name="41--weighing-criteria"></a>**Chapter 4: Final suitability raster**
Of all the components of designing and executing an MCE analysis, the most difficult and precise part is that of weight assignment. The normal routes taken in a typical MCE project concerning housing development to solving this question were not available within the confines of this specific project. Ideally, given the topic, various stakeholders would be interviewed, and asked to judge the relative importance of each of the factors which were to be used in the final model.


This methodology was unavailable here, but as an alternative, previous studies using MCE and stakeholder surveys to rate the suitability of housing sites were used. Only a small number of studies were available on the specific subject and method (Al-Shalabi, et al., 2006) (Maliene, et al., 2013) , and there were some caveats – one study dealt with affordability of existing housing, for example, but the studies nonetheless offered valuable information, utilizing the kind of primary data unavailable here, about how prospective residents weighed factors in choosing housing. Most of the same factors I had already selected for this study were included in the studies referenced, with the exception of distance to water. The weights in these studies were selected and compared against each other, and then compared with qualitative knowledge of the Irish housing context, in obtaining final weightings which would be more reflective of a specifically Irish situation. Among the qualitative sources used included journalistic and academic accounts of the various factors at play in the quality of residential space in Europe, as well as histories of successful and failed social housing projects in the 20th century (Hatherley, 2013) (Minton, 2012).


Water did not figure heavily in many of these accounts, but an analysis of trends in “urban regeneration” in the late 20th and early 21st century indicated that water-proximity did have a significant positive impact of the desirability of a development (MacLaran, 2012). However, in the final formula for this project, water was given the lowest value of the 5 factors, because although water could be, generally, seen as having a positive impact on the desirability of housing in the work consulted, it also indicated that the positive impact of water proximity was much less for the kind of water bodies found in Cavan (lakes and rivers) as opposed to the ocean found in the major cities which were the focus of the majority of the studies. Also, water proximity no longer strictly correlates to clean water access as it would have in the past (Kummu, et al., 2011). Water was, for these reasons, given a final weighting of 0.1.


The highest value given to any of the factors, 0.3, was assigned to proximity to towns and villages, for several reasons. Firstly, proximity to these spaces would be especially important for any social housing development in a relatively lightly-developed rural county like Cavan, where infrastructure and services are lightly spread outside of towns and larger villages, and public transport in the more remote areas is sparse and infrequent. Most of the estates in Cavan were already clustered around discontinuous urban fabric, and a higher weighing would give preferential treatment to estates located in these areas, as the situating of the towns and villages along main roads, and near a large existing population base, numerous services, and businesses, would not only make them more pleasant to live in for any prospective residents, but also the relative ease-of-access would make the completion of their construction simpler, and the cost lower.


Distance from mineral extraction sites was given a higher weighting than distance to water, due to both the scores afforded related indices in the consulted MCE studies and the increased public concern around the environmental and health risks accompanying sites such as these (especially in Cavan, a rumoured site for fracking, where a significant grassroots movement has formed around opposition to the proposal). On top of this, in previous studies, indexes which could be placed in the same category as “mineral extraction sites” (e.g. environmental hazards or waste management) were given scores which put them in line with those for proximity to roads or access to services, so mineral extraction site distance was given a weighting (0.2) which was in line with the weightings given to those other factors, in order to reflect both the increased public concern (The Anglo-Celt, 2011) (which would necessarily affect a project such as this, given the open nature of Ireland’s planning system) and that previous studies indicated it to be, if not an equal concern, a concern which was broadly given the same level of priority.


Road proximity was given a weighting of 0.2, based on its relatively low weighting in the Yemen study (although the factors which it was scored lower than, elevation and slope, were not included as factors but constraints in this study) being countered against the relative importance main roads have in the social structuring of rural life in Ireland. The location of this project also meant that it was probable that at least a small number of residents would commute to work, and while for social housing it would be preferable for the housing to be located in or very close to a town or village, proximity to a major road can compensate effectively for any adverse effects caused by isolation in that case, albeit less so in a county like Cavan with relatively sparse public transport provision. The weight assigned road proximity reflects its relatively lesser importance in determining the desirability of an estate than proximity to towns and villages, but also its greater importance than distance to bodies of water, and its importance being roughly on par with that of the other 2 factors (distance from mineral extraction sites and distance to sports/leisure facilities).


The final factor to be weighted, proximity to sports and leisure facilities, was accorded a weighting of 0.2, reflecting its importance relative to the other factors at play. Prior studies have demonstrated the positive impact access to sports and sports facilities can have on residents of social housing projects, and sports has furthermore been demonstrated to contribute to the forging of a sense of community and strong social bonds, especially in rural areas (Sport Ireland, 2012). Sport also plays an increasingly prominent role in the public health policy of many western governments, including Ireland, as a response to the obesity epidemic (Coulter, et al., 2011). The problematic limits inherent in CORINE’s land use categories offset the major importance of access to sport facilities in the weighing, however – although the sports facilities were judged important, it was also safe to assume that there were sports facilities in the county that were not designated as such by the CORINE dataset. Even with this in mind, the question of accessibility remained important in assigned such a relatively high weighting to a small number of sites, especially with the influx of population a social housing development like the one being explored by this project might entail. Access cannot be guaranteed by e.g. a rural GAA team with limited resources, nor is an expensive private gym likely to be immediately accessible to someone who fits the general profile of a family on the social housing weight list. Proximity to the areas designated by this factor is weighted such because of their openness and accessibility to residents, and their likely ability to cope with an increase in local population in the short-term.


As seen above, the weightings here cumulatively (as they necessarily have to, given the design of this MCE) add up to 1, with the weights, as justified above, fairly reflecting, as best they can, the importance of each factor in qualitatively judging the desirability of a particular site for new social housing. There are always problems involved in assigning quantitative weights to something as inherently qualitative as taste and desire, especially with regards to housing (doubly so when this is undertaken without being able to survey stakeholders directly on the question), but, as best as it can, the weighting here accurately reflects the interplay of factors with each other and their environment, thus achieving a more precise suitability raster for the relatively isolated and predominately rural border county of Cavan.


### <a name="42--final-suitability-raster"></a>4.2: Final suitability raster
Once the final weightings had been judged, it was possible to input an equation into Raster Calculator to create the final suitability raster. The raster, when calculated, would assign a value between 0 and 1 for each pixel calculated from this formula, accounting for all factors and their weightings, and excluding any pixels which did not meet the criteria of the 3 constraints. The final formula built using the Raster Calculator is shown below:

$${(0.3\times C3 + 0.1\times C4 + 0.2\times C5 + 0.2\times C6 + 0.2\times C7)\times C1\times C2\times C8}$$


The final suitability raster was outputted as Suitable, and its ranges of values stretched from 0 to 0.608. It would have been possible to renormalize this raster a second time, with 0.608 assigned a value of 1, using the formula (Suitable/0.608) but this was unnecessary, as the raster was portraying the desirability of different locations in Cavan in relative terms (i.e., 0.608 indicates the most suitable site, with lower scores indicating progressively less suitable/desirable areas). Areas within Cavan that are white have a value on 0 on the basis of the Protected Area or Bogs/Marshes constraints, while pixels that are dark green have a value of 0 on the basis of their slope being too steep. 7 categories were chosen for the final symbology to better differentiate suitability on the higher end of values, as the 5-category value bands ArcMap had set up initially lacked sufficient differentiation within the areas of high suitability in the centre of Cavan. The final raster, with the unfinished estates point file overlain, is pictured below.


<a name="figure6"></a><p align="center">

![Final MCE Suitability Index with unfinished estates point file overlain](https://raw.githubusercontent.com/cathalmurphy/cavansocialhousing/master/Fig7FinalIndex.png)
***Figure 6: Final MCE Suitability Index with unfinished estates point file overlain***

</p>


### <a name="43--summary-of-results"></a>4.3: Summary of results
Examining the final suitability raster, a number of spatial patterns become evident – firstly, most of the pixels falling into the 7th and highest suitability score band (roughly ~0.55 - ~0.608) are located in and around the county’s central towns and its main primary and secondary roads. The existing unfinished estates are also clustered in this “core” region, with some clusters also existing in outlying (and less desirable) areas of the county. Here we have a quantitative geospatial confirmation of something that we could have guessed at before undertaking the project – that the unfinished estates most suitable for redevelopment and completion are those located closest to Cavan’s major towns and roads. A grand total of 50 unfinished estates lie within the highest band, out of a total of 149 in the county as a whole, with 4 more lying in areas which have been excluded by the constraints. No estates fall within the lowest non-zero band, 9 more estates lie in the second non-zero band, with 35 in the third lowest non-zero band. 28 and 22 estates were located inside the 2nd- and 3rd-highest bands respectively. A table breaking down the distribution of estates by suitability range is listed below.


<a name="table3"></a><p align="center">

**Suitability score band**|**# of estates in band**
:-----:|:-----:
0|4
0 – 0.3838|0
0.3838 – 0.4339|9
0.4339 – 0.4720|35
0.4720 – 0.5101|22
0.5101 – 0.5483|28
0.5483 – 0.6079|50
***Table 3: Distribution of unfinished estates by suitability score band***


</p>

At this point, although it was beyond the purview of this project, it would be possible to perform a 2nd MCE calculation, which would consist of several factors, with the unfinished estates (converted to raster format) serving as the constraint. This would be done by weighting the final MCE raster here against several of the attributes contained within the AIRO shapefile deemed most relevant, e.g. % of units completed, or % of roads finished. As it stands, the final raster on its own offers a highly useful guide to any prospective examination of unfinished estates in Cavan looking to select a small number of those estates for redevelopment. 50 estates falling within the highest band may seem like a high number, and is evidence of the relative centralization of property development within the county, reflecting broader centralized patterns in property development and construction within Ireland as a whole (O'Leary & Tennent, 2013), but it still represents a mere third of the total unfinished estates in the county, and by limiting the range of selectable sites in this way has already vastly reduced any work a prospective re-development project would require at the stage involving site studies and selection.


### <a name="44--potential-impacts"></a>4.4: Potential impacts
If any of the housing sites identified through this MCE project as especially suitable for completion were actually worked on, it is both simple and difficult to think through the probable impacts on Cavan’s population and infrastructure. The central location of the most suitable sites in the county means that the existing infrastructure, especially the N-classed roads (the N3, N54, and N55) are well-equipped to cope with the increase in traffic a recommencement of construction would entail. Furthermore, the proximity of towns to the most preferable sites also means that the influx of population that would occur after the completion of the project will have a minimal adverse effect on the county as a whole, and the large increase in population Cavan has experienced since 1991 (about 40%, with Cavan town seeing an increase just short of 100% (City Population, 2012)) means that the service and commercial capacity of the county will be able to deal with a small further increase in population, and the increase in population would be likely to stimulate further economic growth and decrease the unemployment rate, continuing the social benefits secured by the initial construction work to be undertaken on the selected  sites. Overall, although there are significant risks in a project that would most likely entail a degree of relocation of families on the social housing waitlist (problems which possibly would play out in a manner closely according to the script for the failure of the Fianna Fáil government’s attempt at decentralization of government functions in the mid-00s (Guidera, 2010)), the economic and social benefits the project would secure would outweigh any negatives.


## <a name="chapter-5--conclusion"></a>**Chapter 5: Conclusion**
### <a name="51--possible-improvements-and-technical-difficulties"></a>5.1: Possible improvements and technical difficulties
Although this MCE has been, at the very least, useful in that it offers a quantitative demonstration of some ‘common sense’ aspects of housing policy, it also offers a sophistication of this initial ‘common sense’ analysis, allowing us to see how the interplay of various factors (which are secondary to the distribution of urban fabric but are also in an important sense contingent on it) affects the variation with space of suitability for certain uses within the region under study. While I think this project has been successful insofar as it both succeeds as a proof-of-concept of using GIS and MCE to study the suitability of re-developing unfinished publicly-held housing for social uses, and succeeds as an individual piece of high-quality GIS work, there were several limitations encountered in the course of finishing the project, and other areas I would have liked to explore further given more time or a broader project brief.


Firstly, as mentioned in the relevant section, the calculation of distance from water bodies was necessarily incomplete, because lakes and rivers were stored as incompatible spatial object types in the relevant files. While CORINE appears to offer a land use code pertaining to rivers (512 – “stream courses”), only one ‘stream’ was visible at CORINE’s spatial resolution, meaning it would have had little impact on the final raster had it been included in the distance to water calculation. On top of this, a more minor problem (which was ultimately easily resolvable by using Selection by Attribute) was that the Cavan rivers file stored both rivers and streams in a single file, and only distinguished them on the basis of a single attribute field. Ultimately, however, this did not present a problem in the final calculation because the Rivers layer was not used, but given more time I would have liked to recreate the Cavan rivers shapefile as a polygon layer so it could be included along with lakes in a single “Distance to Water” factor in the final calculation. Although it was theoretically possible to create a separate factor for “distance to rivers”, this was not done because I was already dealing with a large number of factors for the project, and having separate distance rasters for both rivers and lakes would have created significant problems in weighing the 2 layers against each other, and furthermore having these 2 rasters included in a single calculation would have been redundant and would also have introduced serious distortion into the final suitability index.


Secondly, although I think I have offered a thorough justification of the weightings for factors I ultimately chose, the circumstances of their calculation were not ideal, given they were extrapolated from secondary sources, some of which were only related to the subject matter of this project in a very tangential way. However, the nature and constraints of this project prevented any surveying of stakeholders or a more holistic calculating of weights. For this reason, the weights I have chosen should be seen as limited in a very crucial sense – although they still offer a realistic guide or baseline from which more accurate weights could be in ascertained in either a broader project or official state-backed project exploring the same sets of issues and questions.


Finally, the spatial data sets used came with broader issues which, while ultimately being resolvable, presented serious problems the kind of which can be common when working with spatial data collected in the field. In this case, most of the spatial layers used had no projection set, which meant that it was difficult to match up these layers with other layers which came with specific set projections. While technically (and as far as the naked eye could tell) the projected and unprojected layers were both really working from the same projection, ArcMap did not recognize this as being the case. However, it was easier to rectify the problem of no projection than the problem of, for example, collected data being listed as having the wrong projection, as in cases like that projection problems can be extremely difficult to diagnose and can involve extensive examination of the data and the equipment used to collect it. In this instance, I was lucky that the initial archive of spatial data included a file with a set projection that matched up with the unprojected data, as it allowed for the ‘linking’ of the unprojected data with the other datasets it was not matching up with. Ultimately, the datasets used were of a very high quality (especially the CORINE dataset) and were very easy to work with, both on the national level, when the data was being processed to produce localized layers, and then on the local level after that.


### <a name="52--concluding-remarks"></a>5.2: Concluding remarks
Through the 5 chapters thus far covered, every important detail of the project has been explored, and every important choice made has been justified – from the selection of the initial site-type for the project, to the selection of weights for the various criteria involved in the MCE segment – with additional analysis of any possible ramifications of the MCE results if the project proposed at the outset were actually realized. Although, as I have mentioned before, the proposal contained within is unlikely to be applied specifically to Cavan, it does offer a glimpse of the possibilities GIS offers to urban planners and to non-state actors interested in political questions surrounding housing. For the former, it functions as a proof-of-concept demonstrating how existing tools can be applied in novel ways to the resolution of recurring problems, while for the latter, it shows how GIS can be used to press political claims – in this case, showing how certain locations in Cavan are in fact ideal for the finishing of unfinished estates to solve problems of housing shortages, offering a proof of Denis Wood and John Krygier’s ideas about GIS as a democratic tool (Krygier & Wood, 2011), although practically the ArcGIS 10 tools used in this project would be beyond the budget of most small-scale individual non-state actors. The project also offers a generalizable model for analysing a region where questions of housing are being contested and identifying the relevant factors and constraints that would be used to produce the best possible suitability index to present to pursue a set of political claims, although in this case the housing sites involved already having seen some level of construction altered the process by which one would choose constraints (i.e. the planning code was judged irrelevant in the selection of constraints as the sites being tested for suitability already had obtained planning permission).


## <a name="bilbiography"></a>**Bibliography**
All-Ireland Research Observatory, 2010. DEHLG Unfinished Estates 2010. [Online]
Available at: http://www.airo.ie/content/dehlg-unfinished-estates-2010
[Accessed 19 December 2013].

Al-Shalabi, M., bin Ahmed, N., bin Mansor, S. & Shiriff, R., 2006. GIS Based Multicriteria Approaches to Housing Site Suitability Assessment, Munich: International Federation of Surveyors.
City Population, 2012. Cavan (County). [Online]
Available at: http://www.citypopulation.de/php/ireland.php?adm2id=CN
[Accessed 28 January 2014].

Coulter, M., Marron, S. & Murphy, F., 2011. Your Health is Your Wealth: Public Health Policy Framework 2012-2020, Drumcondra: St. Patrick's College.
Gleeson, J. & Kitchin, R., 2010. Ghost estates per county. [Online]
Available at: http://irelandafternama.wordpress.com/2010/01/27/ghost-estates-per-county/
[Accessed 4 January 2014].

Griffin, D., 2014. Dublin Prices Seen Rising 14% With Crowded Auctions: Mortgages. [Online]
Available at: http://www.bloomberg.com/news/2014-01-14/dublin-prices-seen-rising-14-with-crowded-auctions-mortgages.html
[Accessed 22 January 2014].

Guidera, A., 2010. Decentralisation 'a failed strategy'. The Irish Independent, 21 July.

Hatherley, O., 2013. The best response to gentrification is better council housing. The Guardian, 3 October.

Henley, P., 2010. Ghost estates testify to Irish boom and bust. [Online]
Available at: http://news.bbc.co.uk/2/hi/europe/8653949.stm
[Accessed 4 January 2014].

Kerr, I. & Melia, P., 2009. €20m bid to salvage the 'ghost estates' under fire. [Online]
Available at: http://www.independent.ie/irish-news/20m-bid-to-salvage-the-ghost-estates-under-fire-26509359.html
[Accessed 27 January 2014].

Krygier, J. & Wood, D., 2011. Making Maps: A Visual Guide to Map Design for GIS. 2nd ed. New York: Guilford Press.

Kummu, M., de Moel, H., Ward, P. & Varis, O., 2011. How Close Do We Live to Water? A Global Analysis of Population Distance to Freshwater Bodies. PLoS One.

Kuper, S., 2013. Priced Out of Paris. [Online]
Available at: http://www.ft.com/intl/cms/s/2/a096d1d0-d2ec-11e2-aac2-00144feab7de.html
[Accessed 28 December 2013].

Lehigh Valley Planning Commission, 2008. Steep Slopes: Guide & Model Regulations, Allentown: Lehigh Valley Planning Commission.

MacCabe, F., 2000. The Housing Market in Ireland: An Economic Evaluation of Trends & Prospects, Dublin: Peter Bacon & Associates.

MacLaran, A., 2012. Planning Participation under Neoliberalism (undergraduate lecture), Dublin: Trinity College Dublin.

Maliene, V., Mulliner, E. & Smallbone, K., 2013. An assessment of sustainable housing affordability using a multiple criteria decision making method, Manchester: University of Manchester.

McWilliams, D., 2006. A warning from deserted ghost estates. [Online]
Available at: http://www.davidmcwilliams.ie/2006/10/01/a-warning-from-deserted-ghost-estates
[Accessed 4 January 2014].

Minton, A., 2012. Ground Control: Fear and happiness in the twenty-first-century city. 2nd ed. London: Penguin.

O'Leary, D. & Tennent, J., 2013. A detailed analysis of the prospects for Irish Property, Dublin: Goodbody.

Sport Ireland, 2012. Consulation on Role and Remit of Sport Ireland, Dublin: Sport Ireland.

The Anglo-Celt, 2011. "Gas fracking" debate comes to Cavan. [Online]
Available at: http://www.anglocelt.ie/news/roundup/articles/2011/07/20/4005633-034gas-fracking034-debate-comes-to-cavan/
[Accessed 20 January 2014].
