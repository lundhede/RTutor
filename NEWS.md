# News for RTutor package

### 2015-11-13: hints at beginning of chunk possible

- You can now add a hint block at the beginning of a chunk,
  before any other command.
  While other hints are linked to the previous expression that will
  be tested, the initial hint works for the whole chunk.
  It will be shown in addition to any expression specific hint.
  It will also  be shown if the code cannot be evaluated
  or in a chunk that has no expression to be tested.


### 2015-11-08: htmlwidget support

- Allow chunks that output htmlwidgets. You need to set the chunk option `output="htmlwidget"`, and specify the widget type in the chunk option `widget`, e.g. `widget="leaflet"`. An example is given in `LeafletExample_sol.Rmd` in the `./inst/examples` folder.

### 2015-11-02: quiz blocks

- Added quiz blocks. You need to provide the argument `addons="quiz"` in create.ps, and add `#< quiz quiz_name ... #>` blocks. For an example, see `QuizExample_sol.Rmd` in the `./inst/examples` folder.


### 2015-11-01: option for memoisation when reading data

- Added the argument `use.memoise` in create.ps. If set to `TRUE`, the functions listed in the argument `memoise.funs` will be memoised when running and showing a problem set. By default memoisation is done for a set of functions that read data from files. This saves time and memory if the same data set is repeatedly loaded in different 
exercises.

### 2015-06-01: awards also in web-based problem sets

- awards can now be used and will be correctly displayed also in web-based problem sets

### 2015-04-01: optional code chunks and notes with chunks

- Add chunk option `optional=TRUE`. Optional chunks don't need to be solved in an exercise and their computations will not be available in subsequent chunks.

- We can now put RTutor chunks and texts in notes using the lines
```  
  #! start_note "Note Title"
   ...
  #! end_note
```
  Unlike info blocks the chunks inside a note can be solved.    Chunks inside a note should have the chunk option `optional=TRUE`.