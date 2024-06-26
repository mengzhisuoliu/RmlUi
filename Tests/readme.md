## RmlUi Test Suite

This directory contains tests and benchmarks for RmlUi. They have been separated into three projects located under the `Source` directory. These projects can be enabled using the CMake options `BUILD_TESTING`.


#### Visual tests

For visually testing the layout engine in particular, with small test documents that can be easily added. Includes features for capturing and comparing tests for easily spotting differences during development. A conversion script for the CSS 2.1 tests is available as described below.

#### Unit tests

To ensure smaller units of the library are working properly.

#### Benchmarks

Benchmarking various components of the library to keep track of performance improvements or regressions for future development, and to find any performance hotspots that could need extra attention.



### Directory Overview

#### `Data`

This directory contains the shared style sheets and documents, as well as the source documents for the included visual tests. All documents located under `Data/VisualTests/` will automatically be loaded by the visual tests project. Additional source folders can be specified with the CMake option `RMLUI_VISUAL_TESTS_RML_DIRECTORIES`. 

#### `Dependencies`

This directory contains additional libraries used by the test suite.

#### `Output`

By default, the visual tests will store screenshots and other outputs into this directory, and read previous screenshots from this directory. To specify other directories, use the CMake options `RMLUI_VISUAL_TESTS_CAPTURE_DIRECTORY` and `RMLUI_VISUAL_TESTS_COMPARE_DIRECTORY`.

#### `Source`

Source code for the test suite.
               
#### `Tools`

Includes a best-effort conversion script for the [CSS 2.1 tests](https://www.w3.org/Style/CSS/Test/CSS2.1/), which includes thousands of tests, to RML/RCSS for testing conformance with the CSS specifications.
