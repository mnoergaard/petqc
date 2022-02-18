  * Update CONTRIBUTORS.md (#953)
  * update contributer location (#952)
  * 21.0.0rc2

First official release after migrating the repository into the *NiPreps*' organization.
This release updates the Docker image with up-to-date dependencies, updates
*MRIQC*'s codebase to the latest *NiTransforms* and includes some minor bugfixes.
Finally, this release also contains a major code style overhaul by Zvi Baratz.
With thanks to @ZviBaratz, @nbeliy, @octomike, @benkay86, @verdurin, and @utooley for their contributions.

  * FIX: ``template_resolution`` deprecation warning (#941)
  * FIX: Set entity ``datatype`` in ``BIDSLayout`` queries (#942)
  * FIX: T2w image of MNI template unavailable in Singularity (#940)
  * FIX: Release process -- Docker deployment not working + Python package lacks WebAPI token (#938)
  * FIX: Revise building documentation at RTD after migration (#935)
  * FIX: Final touch-ups in the maintenance of Docker image + CI (#928)
  * FIX: Update unit tests (#927)
  * FIX: Update dependencies and repair BOLD workflow accordingly (#926)
  * FIX: Update dependencies and repair T1w workflow accordingly (#925)
  * FIX: Set ``matplotlib`` on ``Agg`` output mode (#892)
  * ENH: Optimize *PyBIDS*' layout initialization (#939)
  * ENH: Refactored long strings to a :mod:`mriqc.messages` module (#901)
  * ENH: Refactored :mod:`mriqc.interfaces.common` module (#901)
  * DOC: Various fixes to "Running mriqc" section (#897)
  * MAINT: Updates to ``CONTRIBUTORS.md`` file
  * MAINT: Revise Docker image settings & CircleCI (#937)
  * MAINT: Finalize transfer to ``nipreps`` organization (#936)
  * MAINT: Relicensing to Apache-2.0, for compliance with *NiPreps* and prior transfer to the org (#930)
  * MAINT: New Docker layer caching system of other *NiPreps* (#929)
  * MAINT: Code style overhaul (#901)
  * MAINT: Update ``Dockerfile`` and catch-up with *fMRIPrep*'s (#924)
  * STY: Run ``black`` at the top of the repo (#932)
 Merge tag '21.0.0rc2'
diff --cc .maint/CONTRIBUTORS.md
index 5bfd46b,c2ca94f..fd55380
--- a/.maint/CONTRIBUTORS.md
+++ b/.maint/CONTRIBUTORS.md
@@@ -20,14 -20,16 +20,15 @@@ Before every release, unlisted contribu
  | Ghosh | Satrajit S. | @satra | 0000-0002-5312-6729 | McGovern Institute for Brain Research, MIT, MA, USA; and Department of Otolaryngology, Harvard Medical School, MA, USA |
  | Goncalves | Mathias | @mgxd | 0000-0002-7252-7771 | Department of Psychology, Stanford University, CA, USA |
  | Gorgolewski | Krzysztof J. | @chrisgorgo | 0000-0003-3321-7583 | Google LLC |
- | Huffman | Adam | @verdurin | | |
+ | Huffman | Adam | @verdurin | | Department of Physics, Imperial College London, London, UK |
  | Kay | Benjamin | @benkay86 | | Washington University School of Medicine, St.Louis, MO, USA |
  | Kent | James D. | @jdkent | 0000-0002-4892-2659 | Neuroscience Program, University of Iowa |
- | Lee | John | @leej3 | | Quansight, Dublin, Ireland |
+ | Krause | Michael | @octomike | | Max Planck Institute for Human Development, Berlin, Germany |
+ | Lee | John A. | @leej3 | | Quansight, Dublin, Ireland |
  | Nichols | Thomas | @nicholst | 0000-0002-4516-5103 | Oxford Big Data Institute, University of Oxford, Oxford, GB |
  | Nielson | Dylan | @Shotgunosine | 0000-0003-4613-6643 | Section on Clinical and Computational Psychiatry, National Institute of Mental Health, Bethesda, MD, USA |
 -| Piccirilli | Aaron | @apiccirilli | | Center for Interdisciplinary Brain Sciences Research, Stanford University, CA, USA |
  | Salo | Taylor | @tsalo | 0000-0001-9813-3167 | Department of Psychology, Florida International University, FL, USA |
  | Tooley | Ursula A. | @utooley | 0000-0001-6377-3885 | Department of Neuroscience, University of Pennsylvania, PA, USA |
+ | Triplett | William | @wtriplett | 0000-0002-9546-1306 | University of Florida: Gainesville, Florida, US |
  | Varada | Jan | @jvarada | | Functional MRI Facility, National Institute of Mental Health, Bethesda, MD, USA |
 -| Velasco | Pablo | @pvelasco | | Center for Brain Imaging, New York University, NY, USA |
 +| Velasco | Pablo | @pvelasco | 0000-0002-5749-6049 | Center for Brain Imaging, New York University, NY, USA |
- | | Michael | @octomike | | Max Planck Institute for Human Development, Berlin, Germany |
21.0.0 (TBD)
============
First official release after migrating the repository into the *NiPreps*' organization.
This release updates the Docker image with up-to-date dependencies, updates
*MRIQC*'s codebase to the latest *NiTransforms* and includes some minor bugfixes.
Finally, this release also contains a major code style overhaul by Zvi Baratz.
With thanks to @ZviBaratz, @nbeliy, @octomike, @benkay86, @verdurin, and @utooley
for their contributions.

  * FIX: ``template_resolution`` deprecation warning (#941)
  * FIX: Set entity ``datatype`` in ``BIDSLayout`` queries (#942)
  * FIX: T2w image of MNI template unavailable in Singularity (#940)
  * FIX: Release process -- Docker deployment not working + Python package lacks WebAPI token (#938)
  * FIX: Revise building documentation at RTD after migration (#935)
  * FIX: Final touch-ups in the maintenance of Docker image + CI (#928)
  * FIX: Update unit tests (#927)
  * FIX: Update dependencies and repair BOLD workflow accordingly (#926)
  * FIX: Update dependencies and repair T1w workflow accordingly (#925)
  * FIX: Set ``matplotlib`` on ``Agg`` output mode (#892)
  * ENH: Optimize *PyBIDS*' layout initialization (#939)
  * ENH: Refactored long strings to a :mod:`mriqc.messages` module (#901)
  * ENH: Refactored :mod:`mriqc.interfaces.common` module (#901)
  * DOC: Various fixes to "Running mriqc" section (#897)
  * MAINT: Updates to ``CONTRIBUTORS.md`` file
  * MAINT: Revise Docker image settings & CircleCI (#937)
  * MAINT: Finalize transfer to ``nipreps`` organization (#936)
  * MAINT: Relicensing to Apache-2.0, for compliance with *NiPreps* and prior transfer to the org (#930)
  * MAINT: New Docker layer caching system of other *NiPreps* (#929)
  * MAINT: Code style overhaul (#901)
  * MAINT: Update ``Dockerfile`` and catch-up with *fMRIPrep*'s (#924)
  * STY: Run ``black`` at the top of the repo (#932)

.. admonition:: Author list for papers based on *MRIQC* 21.0.x

    As described in the `Contributor Guidelines
    <https://www.nipreps.org/community/CONTRIBUTING/#recognizing-contributions>`__,
    anyone listed as developer or contributor may write and submit manuscripts
    about *MRIQC*.
    To do so, please move the author(s) name(s) to the front of the following list:

    Zvi Baratz \ :sup:`1`\ ; Christopher J. Markiewicz \ :sup:`2`\ ; Dylan Nielson \ :sup:`3`\ ; Jan Varada \ :sup:`4`\ ;
    Ross W. Blair \ :sup:`2`\ ; William Triplett \ :sup:`5`\ ; Nikita Beliy \ :sup:`6`\ ; John A. Lee \ :sup:`7`\ ;
    Ursula A. Tooley \ :sup:`8`\ ; Bennet Fauber \ :sup:`9`\ ; James D. Kent \ :sup:`10`\ ; Taylor Salo \ :sup:`11`\ ;
    Mathias Goncalves \ :sup:`2`\ ; Thomas Nichols \ :sup:`12`\ ; Adam Huffman \ :sup:`13`\ ; Joke Durnez \ :sup:`2`\ ;
    Pablo Velasco \ :sup:`14`\ ; Satrajit S. Ghosh \ :sup:`15`\ ; Aaron Piccirilli \ :sup:`16`\ ; Asier Erramuzpe \ :sup:`17`\ ;
    Benjamin Kay \ :sup:`18`\ ; Daniel Birman \ :sup:`2`\ ; Michael G. Clark \ :sup:`19`\ ; Michael Krause \ :sup:`20`\ ;
    Rafael Garcia-Dias \ :sup:`21`\ ; Sean Marret \ :sup:`4`\ ; Adam G. Thomas \ :sup:`22`\ ;
    Russell A. Poldrack \ :sup:`2`\ ; Krzysztof J. Gorgolewski \ :sup:`23`\ ; Oscar Esteban \ :sup:`24`\ .

    Affiliations:

      1. Neuroscience Program, Tel-Aviv University
      2. Department of Psychology, Stanford University, CA, USA
      3. Section on Clinical and Computational Psychiatry, National Institute of Mental Health, Bethesda, MD, USA
      4. Functional MRI Facility, National Institute of Mental Health, Bethesda, MD, USA
      5. University of Florida: Gainesville, Florida, US
      6. CRC ULiege, Liege, Belgium
      7. Quansight, Dublin, Ireland
      8. Department of Neuroscience, University of Pennsylvania, PA, USA
      9. University of Michigan, Ann Arbor, USA
      10. Neuroscience Program, University of Iowa
      11. Department of Psychology, Florida International University, FL, USA
      12. Oxford Big Data Institute, University of Oxford, Oxford, GB
      13. Department of Physics, Imperial College London, London, UK
      14. Center for Brain Imaging, New York University, NY, USA
      15. McGovern Institute for Brain Research, MIT, MA, USA; and Department of Otolaryngology, Harvard Medical School, MA, USA
      16. Center for Interdisciplinary Brain Sciences Research, Stanford University, CA, USA
      17. Computational Neuroimaging Lab, BioCruces Health Research Institute
      18. Washington University School of Medicine, St.Louis, MO, USA
      19. National Institutes of Health, USA
      20. Max Planck Institute for Human Development, Berlin, Germany
      21. Institute of Psychiatry, Psychology & Neuroscience, King's College London, London, UK
      22. Data Science and Sharing Team, National Institute of Mental Health, Bethesda, MD, USA
      23. Google LLC
      24. Department of Radiology, Lausanne University Hospital and University of Lausanne

0.16.1 (January 30, 2021)
=========================
Bug-fix release in 0.16.x series.

This PR improves BIDS Derivatives compliance, fixes an issue with reading datasets with
subjects of the form ``sub-sXYZ``, and improves compatibility with more recent matplotlib.

  * FIX: Participant labels starting with ``[sub]`` cannot be used (#890)
  * FIX: Change deprecated ``normed`` to ``density`` in parameters to ``hist()`` (#888)
  * ENH: Write derivatives metadata (#885)
  * ENH: Add ``--pdb`` option to make debugging easier (#884)

0.16.0 (January 5, 2021)
========================
New feature release in 0.16.x series.

This version removes the FSL dependency from the fMRI workflow.

  * FIX: Skip version cache on read-only filesystems (#862)
  * FIX: Honor ``$OMP_NUM_THREADS`` environment variable (#848)
  * RF: Simplify comprehensions, using easy-to-read var names (#875)
  * RF: Free the fMRI workflow from FSL (#842)
  * CI: Fix up Circle builds (#876)
  * CI: Update machine images on Circle (#874)

0.15.3 (September 18, 2020)
===========================
A bugfix release to re-enable setting of `--omp-nthreads/--ants-nthreads`.

  * FIX: omp_nthreads typo (#846)

0.15.2 (April 6, 2020)
======================
A bugfix release containing mostly maintenance actions and documentation
improvements. This version drops Python 3.5.
The core of MRIQC has adopted the config-module pattern from fMRIPrep.
With thanks to A. Erramuzpe, @justbennet, U. Tooley, and A. Huffman
for contributions.

  * MAINT: revise style of all files (except for workflows) (#839)
  * MAINT: Clear the clutter of warnings (#838)
  * RF: Adopt config module pattern from *fMRIPrep* (#837)
  * MAINT: Clear the clutter of warnings (#838)
  * MAINT: Drop Python 3.5, simplify linting (#833)
  * MAINT: Update to latest Ubuntu Xenial tag (#814)
  * MAINT: Centralize all requirements and versions on ``setup.cfg`` (#819)
  * MAINT: Use recent Python image to build packages in CircleCI (#808)
  * DOC: Improve AQI (and other IQMs) and boxplot whiskers descriptions (#816)
  * DOC: Refactor how documentation is built on CircleCI (#818)
  * DOC: Corrected a couple of typos in ``--help`` text (#809)

0.15.1 (July 26, 2019)
======================
A maintenance patch release updating PyBIDS.

  * FIX: FileNotFoundError when MELODIC (``--ica``) does not converge (#800) @oesteban
  * MAINT: Migrate MRIQC to a ``setup.cfg`` style of installation (#799) @oesteban
  * MAINT: Use PyBIDS 0.9.2+ via niworkflows PR (#796) @effigies

0.15.0 (April 5, 2019)
======================
A long overdue update, pinning updated versions of
`TemplateFlow <https://doi.org/10.5281/zenodo.2583289>`__ and
`Niworkflows <https://github.com/nipreps/niworkflows>`__.
With thanks to @garciadias for contributions.

  * ENH: Revision of QI2 (#606) @oesteban
  * FIX: Set matplotlib backend early (#759) @oesteban
  * FIX: Niworkflows pin <0.5 (#766) @oesteban
  * DOC: Update BIDS validation link. (#764) @garciadias
  * DOC: Add data sharing agreement (#765) @oesteban
  * FIX: Catch uncaught exception in WebAPI upload. (#774) @rwblair
  * FIX/DOC: Append new line after dashes in ``mriqc_run`` help text (#777) @rwblair
  * ENH: Use TemplateFlow and niworkflows-0.8.x (#782) @oesteban
  * FIX: Correctly set WebAPI rating endpoint in BOLD reports. (#785) @oesteban
  * FIX: Correctly process values of rating widget (#787) @oesteban

0.14.2 (August 20, 2018)
========================

  * [FIX] Preempt pandas resolving Path objects (#746) @oesteban
  * [FIX] Codacy issues (#745) @oesteban

0.14.1 (August 20, 2018)
========================

  * [FIX] Calculate relative path with sessions (#742) @oesteban
  * [ENH] Add a toggle button to rating widget (#743) @oesteban

0.14.0 (August 17, 2018)
========================

  * [ENH] New feedback widget (#740) @oesteban

0.13.1 (August 16, 2018)
========================

  * [ENH,FIX] Updates to individual reports, fix table after rating (#739) @oesteban

0.13.0 (August 15, 2018)
========================

  * [MAINT] Overdue refactor (#736) @oesteban
    * [FIX] Reorganize outputs (closes #396)
    * [ENH] Memory usage - lessons learned with FMRIPREP (#703)
    * [FIX] Cannot allocate memory (v 0.9.4) (closes #536)
    * [FIX] Drop inoperative ``--report-dir`` flag (#550)
    * [FIX] Drop misleading WARNING of the group-level execution (#714)
    * [FIX] Expand usernames on input paths (#721)
    * [MAINT] More robust naming of derivatives (related to #661)
  * [FIX] Do not fail with spurious 4th dimension on T1w (#738) @oesteban
  * [ENH] Move on to .tsv files (#737) @oesteban

0.12.1 (August 13, 2018)
========================

  * [FIX] BIDSLayout queries (#735)


0.12.0 (August 09, 2018)
========================

  * [FIX] Reduce tSNR memory requirements (#712)
  * [DOC] Fix typos in IQM documentation (#725)
  * [PIN] Update MRIQC WebAPI version (#734)
  * [BUG] Fix missing library in singularity images (#733)
  * [PIN] nipype 1.1.0, niworkflows (#726)

0.11.0 (June 05, 2018)
======================

  * RF: Resume external nipype dependency (#715)

0.10.6 (May 29, 2018)
=====================

  * [HOTFIX] Bug #659

0.10.5 (May 28, 2018)
=====================

  * [ENH] Report feedback (#659)

0.10.4 (March 22, 2018)
=======================

  * [ENH] Various improvements to reports (#708)
  * [MAINT] Style revision (#704)
  * [PIN] pybids 0.5 (#700)
  * [ENH] Increase FAST memory limits (#702)

0.10.3 (February 26, 2018)
==========================

  * [ENH] Enable T2w metrics uploads (#696)
  * [PIN] Updating niworkflows (#698)
  * [DOC] Option -o is outdated for classifier (#697)

0.10.2 (February 15, 2018)
==========================

  * [ENH] Add warning about mounting relative paths (#690)
  * [FIX] Sanitize inputs (#687)
  * [DOC] Fix documentation to use --version instead of -v (#688)

0.10.1
======

  * [FIX] Fixed a bug in reading outputs of 3dFWHMx (#678)

0.9.10
======

  * [FIX] Updated AFNI to 17.3.03. Resolves errors regarding opening display by 3dSkullStrip (#669)

0.9.9
=====

  * [ENH] Update nipype to fix $DISPLAY problem of AFNI's 3dSkullStrip

0.9.8
=====

With thanks to Jan Varada (@jvarada) for the session/run filtering.

  * [ENH] Report recall in cross-validation (requested by reviewer) (#633)
  * [ENH] Hotfixes to 0.9.7 (#635)
  * [FIX] Implement filters for session, run and task of BIDS input (#612)

0.9.7
=====

  * [ENH] Clip outliers in FD and SPIKES group plots (#593)
  * [ENH] Second revision of the classifier (#555):
    * Set matplotlib plugin to `agg` in docker image
    * Migrate scalings to sklearn pipelining system
    * Add Satra's feature selection for RFC (with thanks to S. Ghosh for his suggestion)
    * Make model selection compatible with sklearn `Pipeline`
    * Multiclass classification
    * Add feature selection filter based on Sites prediction (requires pinning to development sklearn-0.19)
    * Add `RobustLeavePGroupsOut`, replace `RobustGridSearchCV` with the standard `GridSearchCV` of sklearn.
    * Choice between `RepeatedStratifiedKFold` and `RobustLeavePGroupsOut` in `mriqc_clf`
    * Write cross-validation results to an `.npz` file.
  * [ENH] First revision of the classifier (#553):
    * Add the possibility of changing the scorer function.
    * Unifize labels for raters in data tables (to `rater_1`)
    * Add the possibility of setting a custom decision threshold
    * Write the probabilities in the prediction file
    * Revised `mriqc_clf` processing flow
    * Revised labels file for ds030.
    * Add IQMs for ABIDE and DS030 calculated with MRIQC 0.9.6.
  * ANNOUNCEMENT: Dropped support for Python<=3.4
  * WARNING (#596):
    We have changed the default number of threads for ANTs. Using parallelism with ANTs
    causes numerical instability on the calculated measures. The most sensitive metrics to this
    problem are the kurtosis calculations on the intensities of regions and qi_2.

0.9.6
=====

  * [ENH] Finished setting up `MRIQC Web API <https://mriqc.nimh.nih.gov>`_
  * [ENH] Better error message when --participant_label is set (#542)
  * [FIX] Allow --load-classifier option to be empty in mriqc_clf (#544)
  * [FIX] Borked bias estimation derived from Conform (#541)
  * [ENH] Test against web API 0.3.2 (#540)
  * [ENH] Change the default Web API address (#539)
  * [ENH] MRIQCWebAPI: hash fields that may have PI (#538)
  * [ENH] Added token authorization to MRIQCWebAPI client (#535)
  * [FIX] Do not mask and antsAffineInitializer twice (#534)
  * [FIX] Datasets where air (hat) mask is empty (#533)
  * [ENH] Integration testing for MRIQCWebAPI (#520)
  * [ENH] Use AFNI to calculate gcor (#531)
  * [ENH] Refactor derivatives (#530)
  * [ENH] New bold-IQM: dummy_trs (non-stady state volumes) (#524)
  * [FIX] Order of BIDS components in IQMs CSV table (#525)
  * [ENH] Improved logging of mriqc_run (#526)

0.9.5
=====

  * [ENH] Refactored structural metrics calculation (#513)
  * [ENH] Calculate rotation mask (#515)
  * [ENH] Intensity harmonization in the anatomical workflow (#510)
  * [ENH] Set N4BiasFieldCorrection number of threads (#506)
  * [ENH] Convert FWHM in pixel units (#503)
  * [ENH] Add MRIQC client for feature crowdsourcing (#464)
  * [DOC] Fix functional feature labels in documentation (docs_only) (#507)
  * [FIX] New implementation for the rPVE feature (normalization, left-tail values) (#505)
  * [ENH] Parse BIDS selectors (run, task, etc.), improve CLI (#504)


0.9.4
=====

  * ANNOUNCEMENT: Dropped Python 2 support
  * [ENH] Use versioneer to handle versions (#500)
  * [ENH] Speed up spatial normalization (#495)
  * [ENH] Resampling of hat mask and TPMs with linear interp (#498)
  * [TST] Build documentation in CircleCI (#484)
  * [ENH] Use full-resolution T1w images from ABIDE (#486)
  * [TST] Parallelize tests (#493)
  * [TST] Binding /etc/localtime stopped working in docker 1.9.1 (#492)
  * [TST] Downgrade docker to 1.9.1 in circle (build_only) (#491)
  * [TST] Check for changes in intermediate nifti files (#485)
  * [FIX] Erroneous flag --n_proc in CircleCI (#490)
  * [ENH] Add build_only tag to circle builds (#488)
  * [ENH] Update Dockerfile (#482)
  * [FIX] Ignore --profile flag with Linear plugin (#483)
  * [DOC] Deep revision of the documentation (#479)
  * [ENH] Minor improvements: SpatialNormalization and segmentation (#472)
  * [ENH] Fixed typo for neurodebian install via apt-get (#478)
  * [ENH] Updating fs2gif script (#465)
  * [ENH] RF: Use niworkflows.interface.SimpleInterface (#468)
  * [ENH] Add reproducibility of metrics tracking (#466)

Release 0.9.3
=============

* [ENH] Reafactor of the Dockerfile to improve transparency, reduce size, and enable injecting code in Singularity (#457)
* [ENH] Make more the memory consumption estimates of each processing step more conservative to improve robustness (#456)
* [FIX] Minor documentation cleanups (#461)

Release 0.9.2
=============

* [ENH] Optional ICA reports for identifying spatiotemporal artifacts (#412)
* [ENH] Add --profile flag (#435)
* [ENH] Crashfiles are saved in plain text to improve portability (#434)
* [FIX] Fixes EPI mask erosion (#442)
* [ENH] Make FSL and AFNI motion correction more comparable by using the same scheme for defining the reference image (#444)
* [FIX] Temporarily disabling T1w quality classifier until it can be retrained on new measures (#447)


Release 0.9.1
=============

* [ENH] Add mriqc version and input image hash to IQMs json file (#432)
* [FIX] Affine and warp transforms are now applied in the correct order (#431)

Release 0.9.0-2
===============

* [ENH] Revise Docker paths (#429)
* [FIX] Greedy participant selection (#426)
* [FIX] Pin pybids to new version 0.1.0 (#427)
* [FIX] Amends sloppy PR #425 (#428)

Release 0.9.0-1
===============

* [FIX] BOLD reports clipped IQMs after spikes_num (#425)
* [FIX] Unicode error writing group reports (#424)
* [FIX] Respect Nifi header in fMRI conform node (#415)
* [DOC] Deep revision of documentation (#411, #416)
* [ENH] Added sphinx extension to plot workflow graphs (#411)
* [FIX] Removed repeated bias correction on anatomical workflows (#410)
* [FIX] Race condition in bold workflow when using shared workdir (#409)
* [FIX] Tests (#408, #407, #405)
* [FIX] Remove CDN for group level reports (#406)
* [FIX] Unused connection, matplotlib segfault (#403, #402)
* [ENH] Skip SpikeFFT detector by default (#400)
* [ENH] Use float32 (#399)
* [ENH] Spike finder performance improvoments (#398)
* [ENH] Basic T2w workflow (#394)
* [ENH] Re-enable 3dvolreg (#390)
* [ENH] Add T1w classifier (#389)

Release 0.9.0-0
===============

* [FIX] Remove non-repeatable step from pipeline (#369)
* [ENH] Improve group level command line, with more informative output when no IQMs are found for a modality (#372)
* [ENH] Make group reports self-contained (#333)
* [FIX] New mosaics, based on old ones (#361, #360, #334)
* [FIX] Require numpy>=1.12 to avoid casting problems (#356)
* [FIX] Add support for acq and rec tags of BIDS (#346)
* [DOC] Documentation updates (#350)
* [FIX] pybids compatibility "No scans were found" (#340, #347, #342)
* [ENH] Rewrite PYTHONPATH in docker/singularity images (#345)
* [ENH] Move metadata onto the bottom of the individual reports (#332)
* [ENH] Don't include MNI registration report unlesS --verbose-reports is used (#362)


Release 0.8.9
=============

* [ENH] Added registration svg panel to reports (#297)


Release 0.8.8
=============

* [FIX] Bug translating int16 to uint8 in conform image.
* [FIX] Error in ConformImage interface (#297)
* [ENH] Replace BBR by ANTs (#295, #296)
* [FIX] Singularity: user-environment leaking into container (#293)
* [ENH] Report failed cases in group report (#291)
* [FIX] Brighter anatomical --verbose-reports (#290)
* [FIX] X-flip in the mosaics (#289)
* [ENH] Show metadata in the individual report (#288)
* [ENH] Label in the cutoff threshold - fmriplot (#287)
* [ENH] PyBIDS (#286)
* [ENH] Simplify tests (#284)
* [FIX] MRIQC crashed generating csv files (#283)
* [FIX] Bug in setup.py (#281)
* [ENH] Makefile (#280)
* [FIX] Revision of IQMs (#266, #272, #279)
* [ENH] Deprecation of --nthreads, new flags (#260)
* [ENH] Improvements on plots rendering (#254, #257, #258, #267, #268, #269, #270)
* [ENH] FFT detection of spikes (#253, #272)
* [FIX] Labels and links of samples in group plots (#249)
* [ENH] Units in group plots (#242)
* [FIX] More reliable group level (#238)
* [ENH] Add --verbose-reports for fMRI (#236)
* [ENH] Migrate functional reports to html (#232)
* [ENH] Add 0.2 FD cutoff line (#231)
* [ENH] Add AFNI's outlier count to carpet plot confound charts (#230)

Release 0.8.7
=============

* [ENH] Anatomical Group reports in html (#227)
* [ENH] Add kurtosis to summary statistics (#224)
* [ENH] New report layout for fMRI, added carpetplot (#198)
* [ENH] Anatomical workflow refactor (#219).

Release 0.8.6
=============

* [FIX, CRITICAL] Do not chmod in Docker internal scripts
* [FIX] Error creating derivatives folder
* [ENH] Moved MNI spatial normalization to NIworkflows, and made robust.
* [ENH] De-coupled participant and group (reports) levels
* [ENH] Use new FD and DVARs calculations from nipype (#172)
* [ENH] Started with python3 compatibility
* [ENH] Added new M2WM measure #158
* [FIX] QI2 is skipped if background intensity is not appropriate (#147)

Release 0.8.5
=============

* [FIX] Error inverting the T1w-to-MNI warping (#146)
* [FIX] TypeError computing DVARS (#145)
* [ENH] Plot figure of fitted background chi for QI2 (#143)
* [ENH] Move skull-stripping and reorient to NIworkflows (#142)
* [FIX] mriqc crashes if no anatomical scans are found (#141)
* [DOC] Added acknowledgments to CPAC team members (#134)
* [ENH] Use absolute imports (#133)
* [FIX] VisibleDeprecationWarning (#132)
* [ENH] Provide full FD/DVARS files (#128)
* [ENH] Use MCFLIRT to compute motion parameters. AFNI's 3dvolreg now is optional (#121)
* [FIX] BIDS trees with anatomical images with different acquisition tokens (#116)
* [FIX] BIDS trees with anatomical images with several runs (#112)
* [ENH] Options for ANTs normalization: reduced test times (#124),
  and updated options (#115)

Release 0.8.4
=============

* [ENH] PDF reports now use RST templates and jinja2 (#109)
* [FIX] Single-session-multiple-run anatomical files were not correctly located (#112)

Release 0.8.3
=============

* [DOC] Added examples of the PDF reports (#107)
* [FIX] Fixed problems with Python 3 when generating reports.

Release 0.8.2
=============

* [ENH] Python 3 compatibility (#99)
* [ENH] Add JSON settings file for ANTS (#95)
* [ENH] Generate reports automatically if mriqc is run without the -S flag (#93)
* [FIX] Revised implementation of QI2 measure (#90)
* [AGAVE] Fixed docker image for agave (#89)
* [FIX] Problem when generating the air mask with dipy installed (#88)
* [ENH] One-session-one-run execution mode (#85)
* [AGAVE] Added an agave app description generator (#84)

Release 0.3.0
=============

* [ENH] Updated CircleCI and Docker to use the version 2.1.0 of ANTs
  compiled by their developers.
* [ENH] New anatomical workflows to compute the air mask (#56)

Release 0.2.0
=============

Release 0.1.0
=============

* [FIX] #55
* [ENH] Added rotation of output csv files if they exist


Release 0.0.2
=============

* [ENH] Completed migration from QAP
* [ENH] Integration with ReadTheDocs
* [ENH] Submission to PyPi


Release 0.0.1
=============

* Basic mriqc functionality
