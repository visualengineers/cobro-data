# Contributing a data visualization project to the database

0. Classify all elements of the visualization project according to the construction kit elements (see constructionkit.md and [visual-search.org](http://visual-search.org) -- more tutorials coming soon!
1. Find a suitable short name (ID) for the project, e.g. "utopia"
2. Create a project folder inside the repository in the "project" folder
3. Create JSON file with meta data of project "project.json" (see schema file and other projects for structure)
4. Create or find a construction plan inside the "_constructionplan" folder that corresponds to the project's construction plan
  * If no existing construction plan and patterns match the project, create the required patterns inside the "_patterns" folder and the construction plan insinde the "_constructionplan" folder
  * If a construction plan exists with exactly the same patterns as in your project, find its ID.
5. Reference the construction plan you created or an existing one inside the project.json
6. Upload and add thumbnails of the project (at least one, pay attention to high resolution screenshots) inside the project folder
7. Inform the author of the visualization project about the upload to this repository and ask for permission if necessary
8. Commit and push your additions to a new branch and create a merge request
9. DONE! Thank you very much

```
cobro-data
├── _assets/
│   ├── blocks/
│        └── <png / svg files of blocks>
│   └── blocks.json
├── _constructionplans/ 
│   ├── ...
│   └── *cp0001.json*
├── _patterns/
│   ├── ...
│   └── *cp0001.json*   --> one or more patterns of the construction plan
├── _schema/    
│   ├── blocks.schema.json
│   ├── pattern.schema.json
│   ├── project.schema.json
│   └── constructionplan.schema.json
└── projects/
    ├── ...
    └── *yourproject/*
        ├── *project.json*
        └── *thumbnail.png*
```

# Create a vector graphic in Adobe Illustrator

0. If necessary: create a new Adobe Illustrator project (AI file). There you already have the opportunity to increase the number of artboards and arrange them. In the project pattern.ai (see  */cobro-data/_assets/pattern/pattern.ai*) you already find such a structure (40 artboads á 320×180px, 5 columns).
1. Within a project, you can use the Artboards tool to create and edit new artboards.
2. Rename the artboards in a desired title, like the pattern name (Later at point 6, it's useful to be able to export individual artboards)
3. Import a PDF file: you open a PDF file and select a page (only one page can be choosen at a time) - Illustrator opens it in a separate project
4. With the Selection tool you can select the desired area and copy it to a artboards in your own project
5. Use the Color Mixer or Color Picker to change the colors of the selected element faces or contour and take the Contour tool to change the shape of the contour
   * Standard colors and their hex codes: 
      * light green = # A1D5D2 (e.g. the pattern face)
      * dark green = # 236666 (e.g. the pattern grid or visual elements) 
      * dirty green = # 52702A (e.g. interaction elements)
      * purple        = # 3D2877 (e.g. layout structure elements)
      * dark red     = # B32D2B (e.g. dimension elements)
      
   * Standard shapes/objects and their properties:
      * Text   - font = Roboto/ RobotoCondensed
      * Icons - contour thickness = 1 pt

6. Finally, you can export each artboard in SVG and PNG files:
   * for SVG: Click on Save As and choose the SVG format. For separate files, click the Artboard button at the bottom of the Save As window and give the files a prefix as file name (e.g.: Prefix = *pattern.svg*, Ardboard Title = abc → Result = *pattern_abc.svg*). You can also select a desired area of artboards. Save!
   * for PNG: Export the project as PNG. For separate files follow the appropriate steps in the export window like saving SVG. In addition, another window opens after the click on Save. There choose the resolution 300ppi and color Transparency. Confirm with OK!
7. DONE
      
