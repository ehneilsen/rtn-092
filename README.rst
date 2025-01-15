.. image:: https://img.shields.io/badge/rtn--092-lsst.io-brightgreen.svg
   :target: https://rtn-092.lsst.io
.. image:: https://github.com/lsst/rtn-092/workflows/CI/badge.svg
   :target: https://github.com/lsst/rtn-092/actions/

##########################################################################
schedview: Tools for Visualizing Survey Progress and Scheduler Performance
##########################################################################

RTN-092
=======

Over the course of ten years of observing, the NSF-DOE Vera C. Rubin Observatory, funded by the U.S. National Science Foundation and the U.S. Department of Energy's Office of Science, will complete the Legacy Survey of Space and Time (LSST), collecting approximately 2 million images over the 18000 square degree footprint in the southern sky. An automated scheduler, rubin_scheduler, will schedule the exposures that comprise this survey.  schedview is a python module with tools for collecting, processing, and visualizing survey progress and scheduler performance metadata. These components can be combined into online dashboards (or other user interfaces), used within jupyter notebooks, or with automatically generated parameterized notebooks using tools such as Times Square. The current version includes the pre-night briefing, a report that summarizes a simulation of a night of observing before it takes place to catch problems and prepare staff for the night ahead; the scheduler snapshot dashboard, a web application for examining the state of the scheduler at different times during observing; and the scheduler-focused night summary, which summarizes a completed night. Examples of figures supported for these dashboards and reports include interactive sky maps of visits, basis function evaluations used by the scheduler, timelines of visits and logging events, plots of visit metadata, and others.

Links
=====

- Live drafts: https://rtn-092.lsst.io
- GitHub: https://github.com/lsst/rtn-092

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst/rtn-092

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
