studyforrest.org Dataset
************************

|license| |access| |doi|

Localization of higher-level visual ROIs
========================================

For all participants in the phase2 extension of the studyforrest dataset, the
following visual areas were localized:

- fusiform face area (FFA)
- occipital face area (OFA)
- parahippocampal place area (PPA)
- extrastriate body area (EBA)
- lateral occipital complex (LOC)
- early visual cortex (VIS)

More information on the procedure and the results can be found in:

     Ayan~Sengupta, Falko R. Kaule, J. Swaroop Guntupalli,
     Michael B. Hoffmann, Christian Häusler, Jörg Stadler,
     Michael Hanke. An extension of the studyforrest
     dataset for vision research. (submitted for publication)

For further information about the project visit: http://studyforrest.org

Content
-------

``code/``:
   all source code to perform the analysis of the block-design
   localizer fMRI data

``src/``:
   links to repositories containing all inputs for the analysis

``sub-??/``:
   analysis results per participant

   ``onsets/``:
     per-stimulus condition timing in FSL's EV3 format (converted from the BIDS
     event specifications)

   ``2ndlvl.gfeat/``:
     Full output folder of the 2nd level fixed-effects analysis aggregating
     1st-level GLM parameters across all four experiment runs. This contains
     thresholded and unthresholded Z-stat maps which were the basis for the
     subsequent titration of ROI masks per participant.

   ``rois/``:
     One mask volume per isolated voxel cluster in the results. Each filename
     starts with the ROI label (e.g. lFFA for left fusiform face area). There
     can be more than one file/cluster per ROI per subject, if more than one
     isolated voxel cluster was present in the results.

How to obtain the data files
----------------------------

This repository contains metadata and information on the identity of all
included files. However, the actual content of the (sometime large) data
files is stored elsewhere. To obtain any dataset component, git-annex_ is
required in addition to Git_.

1. Clone this repository to the desired location.
2. Enter the directory with the local clone and run::

     git annex init

   Older versions of git-annex may require you to run the following
   command immediately afterwards::

     git annex enableremote mddatasrc

Now any desired dataset component can be obtained by using the ``git annex get``
command. To obtain the entire dataset content run::

     git annex get .

Keep data up-to-date
--------------------

If updates to this dataset are made in the future, update any local clone by
running::

     git pull

followed by::

     git annex get .

to fetch all new files.



.. _Git: http://www.git-scm.com

.. _git-annex: http://git-annex.branchable.com/

.. |license|
   image:: https://img.shields.io/badge/license-PDDL-blue.svg
    :target: http://opendatacommons.org/licenses/pddl/summary
    :alt: PDDL-licensed

.. |access|
   image:: https://img.shields.io/badge/data_access-unrestricted-green.svg
    :alt: No registration or authentication required

.. |doi|
   image:: https://img.shields.io/badge/doi-missing-lightgrey.svg
    :target: http://dx.doi.org/
    :alt: DOI
