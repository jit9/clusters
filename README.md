# ptsrc-cat
Point source catalog code

Initial readme from Heather skyping with Kevin on 4 October 2016. A more complete readme coming soon!

To make the map used by the source finding code:
1. add together the CMB I and beam_test maps using eg add_input_beam_test_and_100.py

2. Run weightedCoadd which uses flipperDict dictionary-> need to give it the names and weights of the 
4-way split sets **how do you give these inputs?

3. Run get_maps - not sure if this does anything important or just renames files

4. Run convertToJyPerSr to change from micro Kelvin to Janskys per steradian
or alternatively just have an input map that is in Jy per sr to use as input to makeCatalogMaster

To get the source catalogue
1. Run makeCatalogMaster (it uses makeCatalogMaster.dict so make sure the information in there is correct. 
It might also use makeCatalog, so makeCatalog.dict should be up to date, including with a reference to a 1D beam 
pattern in signalTransformParameters). This produces the source catalog.

If you get an error about not finding catalog.pickle, then look in main in the folders created by makeCatalogMaster 
and read catalog.err to see what went wrong.
