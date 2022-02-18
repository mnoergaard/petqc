
.. _reports-bold:

BOLD images
===========
One individual report per input functional timeseries will be generated
in the path ``<output_dir>/reports/sub-IDxxx_task-name_bold.html```.
An example report is given
`here <http://web.stanford.edu/group/poldracklab/mriqc/reports/sub-50013_task-rest_bold.html>`_.

The individual report for the functional images is structured as follows:

.. _reports-bold-summary:

Summary
-------
The first section summarizes some important information:

  * subject identifier, date and time of execution of
    ``mriqc``, software version;
  * workflow details and flags raised during execution; and
  * the extracted IQMs.

.. _reports-bold-visual:

Visual reports
--------------
The section with visual reports contains:

#. Mosaic view of the average BOLD signal.

   .. figure:: ../resources/reports-bold_mean.png
     :alt: mean epi mosaic

#. Mosaic view of the temporal standard deviation.

   .. figure:: ../resources/reports-bold_sd.png
     :alt: sd of epi mosaic

#. Summary plot, showing the slice-wise
   signal intensity at the extremes for the identification
   of spikes, the outliers metric, the DVARS and the
   :abbr:`FD (framewise displacement)`. Finally the
   so-called carpetplot [Power2016]_

   .. figure:: ../resources/reports-bold_summary.png
     :alt: fMRI summary plot

.. _reports-bold-verbose:

Verbose reports
---------------
If mriqc was run with the ``--verbose-reports`` flag, the
following plots will be appended:

#. Mosaic view of the average BOLD signal, zoomed-in
   to the bounding box of brain activation.

   .. figure:: ../resources/reports-bold_mean_zoom.png
     :alt: zoomed mean epi mosaic

#. Mosaic view of the average BOLD signal, with background
   enhancement.

   .. figure:: ../resources/reports-bold_mean_bg.png
     :alt: mean epi background mosaic

#. One rows of axial views at different Z-axis points
   showing the calculated brain mask.

   .. figure:: ../resources/reports-bold_mask.png
     :alt: bold brainmasks

#. Mosaic view with animation for assessment of the
   co-registration to MNI space (roll over the image
   to activate the animation).

   .. figure:: ../resources/reports-bold_mni.png
     :alt: bold-mni coregistration

.. _reports-bold-metadata:

Metadata
--------
If some metadata was found in the BIDS structure, it is
reported here.

.. topic:: References

  .. [Power2016] Power JD, A simple but useful way to assess fMRI scan qualities.
     NeuroImage. 2016. doi: `10.1016/j.neuroimage.2016.08.009 <http://doi.org/10.1016/j.neuroimage.2016.08.009>`_

