Back to [Projects List](../../README.md#ProjectsList)

# Use Slicer from Jupyter notebook

## Key Investigators

- [Jean-Christophe Fillion-Robin](https://www.kitware.com/jean-christophe-fillion-robin/) (Kitware Inc., USA)
- [Andras Lasso](https://github.com/lassoan) (Queen's University, Canada)

# Project Description

[Jupyter notebook](https://en.wikipedia.org/wiki/IPython) is an interactive shell for executing scripts and viewing execution results.

## Objective

Notebook user interface (frontend) is separated from the code execution engine (kernel). The objective is to create a Slicer extension, which Jupyter notebooks can connect to and access all Slicer features.

## Approach and Plan

1. Implement extension that includes a simple kernel that can execute Python commands using Slicer's built-in Python interpreter.
1. Implement returning of console output to the notebook.
1. Implement returning of viewer content to the notebook.
1. Publish extension on extension manager.

## Progress and Next Steps

1. Created [SlicerJupyter](https://github.com/Slicer/SlicerJupyter) extension, which uses [xeus](https://github.com/QuantStack/xeus) as Jupyter kernel implementation
1. Contributed changes to dependent projects. See our `QuantStack/xeus` [pull requests](https://github.com/QuantStack/xeus/pulls?q=is%3Apr+is%3Aclosed+author%3Ajcfr), [our xeus issue report](https://github.com/QuantStack/xeus/issues/67) discussing best strategy to update xeus for supporting event-loop integration, and also our [branch](https://github.com/noloader/cryptopp-cmake/compare/master...jcfr:miscellaneous-tweaks) improving CMake support for `CryptoPP`.
1. Implemented command execution
1. Implemented preliminary version of ``display()`` function to show viewer content in the notebook.
1. Publish extension on extension manager.

Future plans:
- It will be possible to publish and run Slicer notebooks using [binder](https://mybinder.org/)

# Illustrations

Side-by-side view of a Notebook and 3D Slicer:

![Screenshot of a notebook and Slicer](NotebookSideBySide.png )

Notebook showing code and viewer content:

![Screenshot of a notebook](NotebookOnly.png)

Notebook showing code and viewer content:

![Screenshot of a notebook in JupyterLab](JupyterLab.png)

Complete notebook rendered on GitHub: https://github.com/lassoan/SlicerNotebooks/blob/master/My%20first%20Slicer%20notebook.ipynb

# Background and References

- [SlicerJupyter extension](https://github.com/Slicer/SlicerJupyter)
- https://en.wikipedia.org/wiki/Project_Jupyter
- [Notebook format description](http://nbformat.readthedocs.io/en/latest/format_description.html)
