#TopoTijdReis2Qgis

QGIS Plugin to import TopoTijdReis WMS and WMTS layers into QGIS

This plugin consists of a slider widget that allows you to easily navigate through TopoTijdReis layers and load them into QGIS. A single year can be loaded simply by entering the year in a text box in the QGIS workspace.
With the "Compare" function, a second canvas is created where a second year can be displayed. All other project layers are displayed on both the main and the second canvas.

Both topographic maps and aerial photos are available.

##Installation

You need QGIS version >3.0. In the plugin menu (Manage and Install Plugins…) search for "TopoTijdReis2Qgis" and select it.

Adding a topographic map for a single year

To load the topographic map for a single year, type the year in the text box next to the plugin icon and press Enter. The topographic map for that year from TopoTijdReis will be loaded into the project. The layer will be named "Topotijdreis 'year'".

##Switching between years with the slider

Click the TopoTijdReis icon to start the single slider.
A layer group named "Topotijdreis" will automatically be created, and the most recent topographic map from TopoTijdReis will be loaded into the project. By moving the slider to select a different year, the current layer is removed, and the map for the selected year is loaded into the project. The year can also be changed by typing it into the spinbox above the slider — don’t forget to press Enter, otherwise the map layer will not update.
Using the dropdown menu at the top of the widget, you can switch between topographic maps and aerial photos. The range of years on the slider will automatically adjust to the available years for the selected map type.

##Comparing two maps

From the menu bar, go to Web → TopoTijdReis2QGIS → Compare to open a widget with a second canvas and two sliders. A layer group "Topotijdreis" is created, containing two subgroups: "Topotijdreis_maincanvas" and "Topotijdreis_secondcanvas". The left slider controls the layer in "Topotijdreis_maincanvas" and the right slider controls the layer in "Topotijdreis_secondcanvas". Changes to map layers and switching between topo/aerial photos work the same way as with the single slider.

The extent/scale of the second canvas is not automatically linked to the main canvas. This must be set manually in the window. Check "Synchronize center with main map" and "Synchronize scale" so both maps always display the same area.

Rendering of layers in the second canvas is controlled by a map theme, which is refreshed whenever either slider is changed. This map theme is a clone of the layer symbology and render order from the main canvas, excluding the TopoTijdReis layer of the main canvas. If a layer is added to the project but does not appear on the second canvas, it may be necessary to select the spinbox of the second canvas and press Enter — this refreshes the map theme.

NOTE: When adjusting layer order in the Layers panel, move only the entire "Topotijdreis" group, not the individual layers or subgroups within it. Changing the order inside the group will break the functionality of the second canvas.
