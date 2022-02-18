petqc: image quality metrics for quality assessment of PET
==========================================================

|DOI| |Zenodo| |Package| |Pythons| |DevStatus| |License| |Documentation| |CircleCI| |Codacy|

PETQC extracts no-reference IQMs (image quality metrics) from
structural (T1w and T2w) and PET (Positron Emission Tomography)
data.

PETQC is an open-source project, developed under the following
software engineering principles:

#. **Modularity and integrability**: PETQC implements a
   `nipype <http://nipype.readthedocs.io>`_ workflow to integrate modular
   sub-workflows that rely upon third party software toolboxes such as
   FSL, ANTs and AFNI.

#. **Minimal preprocessing**: the PETQC workflows should be as minimal
   as possible to estimate the IQMs on the original data or their minimally
   processed derivatives.

#. **Interoperability and standards**: PETQC follows the the `brain imaging data structure
   (BIDS) <http://bids.neuroimaging.io>`_, and it adopts the `BIDS-App
   <http://bids-apps.neuroimaging.io>`_ standard.

#. **Reliability and robustness**: the software undergoes frequent vetting sprints
   by testing its robustness against data variability using images from `OpenNeuro <https://openneuro.org>`_.
   Its reliability is permanently checked and maintained with
   `CircleCI <https://circleci.com/gh/nipreps/petqc>`_.

Citation
--------
.. topic:: **When using PETQC, please include the following citation:**

Support and communication
-------------------------
The documentation of this project is found here: http://petqc.readthedocs.io/.

Users can get help using the `petqc-users google group <https://groups.google.com/forum/#!forum/petqc-users>`_.

All bugs, concerns and enhancement requests for this software can be submitted here:
https://github.com/nipreps/petqc/issues.

License information
-------------------
*PETQC* adheres to the
`general licensing guidelines <https://www.nipreps.org/community/licensing/>`__
of the *NiPreps framework*.

*PETQC* originally derives from, and hence is heavily influenced by, the
`PCP Quality Assessment Protocol
<http://preprocessed-connectomes-project.github.io/quality-assessment-protocol>`__.
Please check the ``NOTICE`` file for further information.

License
~~~~~~~
Copyright (c) 2021, the *NiPreps* Developers.

As of the 21.0.x pre-release and release series, *PETQC* is
licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
`http://www.apache.org/licenses/LICENSE-2.0
<http://www.apache.org/licenses/LICENSE-2.0>`__.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Acknowledgements
----------------
This work is steered and maintained by the `NiPreps Community <https://www.nipreps.org>`__.

.. topic:: **Thanks**

.. |DOI| image:: https://img.shields.io/badge/doi-10.1371%2Fjournal.pone.0184661-blue.svg
   :target: https://doi.org/10.1371/journal.pone.0184661
.. |Zenodo| image:: https://zenodo.org/badge/DOI/10.5281/zenodo.2630889.svg
   :target: https://doi.org/10.5281/zenodo.2630889
.. |Package| image:: https://img.shields.io/pypi/v/petqc.svg
   :target: https://pypi.python.org/pypi/petqc/
.. |Pythons| image:: https://img.shields.io/pypi/pyversions/petqc.svg
   :target: https://pypi.python.org/pypi/petqc/
.. |DevStatus| image:: https://img.shields.io/pypi/status/petqc.svg
   :target: https://pypi.python.org/pypi/petqc/
.. |License| image:: https://img.shields.io/pypi/l/petqc.svg
   :target: https://pypi.python.org/pypi/petqc/
.. |Documentation| image:: https://readthedocs.org/projects/petqc/badge/?version=latest
   :target: http://mriqc.readthedocs.io/en/latest/?badge=latest
.. |CircleCI| image:: https://circleci.com/gh/nipreps/petqc/tree/master.svg?style=shield
   :target: https://circleci.com/gh/nipreps/petqc/tree/master
.. |Codacy| image:: https://api.codacy.com/project/badge/grade/fbb12f660141411a89ba1ae5bf873717
   :target: https://www.codacy.com/app/code_3/petqc
