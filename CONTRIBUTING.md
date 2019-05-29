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
