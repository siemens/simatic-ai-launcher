# Changelog

All notable changes to this project will be documented in this file. See standard-version for commit guidelines.

### 1.0.6 (2021-05-07)


### Features

* **TFS-11385:** use gherkin in tests (0172178)
* **TFS-11626:** Pipeline preprocess job (a3896d6)
* **TFS-11914:** Refactor pipeline job (041e067)
* **TFS-9402:** pep8 notebooks (e64db09)


### Bug Fixes

* **TFS-12035:** renaming typo in notebook filename (5348bf3)

### 1.0.5 (2021-04-01)


### Features

* **TFS-10675, TFS-10674:** automate release jobs (53b4602)
* **TFS-10933:** update copyright (0ac1ef1)
* **TFS-11259:** remove venv and conda tests (56c7839)
* **TFS-9511, TFS-11320:** save model to .pt and .onnx (4df3326)


### Bug Fixes

* **TFS-11054:** update pillow version (b55c112)

### 1.0.4 (2021-03-19)


### Bug Fixes

* **TFS-11007:** clearing (eafd715)


### Tests

* **TFS-9485:** contains TFS-8831, adapting tests to Robot framework (a977aa3)

### 1.0.3 (2021-02-19)


### Documentation

* **TFS-8030:** add issue and pull request templates (a27dd21)

### 1.0.2 (2021-01-28)

### 1.0.1 (2021-01-25)


### Features

* **TFS-8019:** Remove object detection (e994825)
* **TFS-8045:** Automatic release to GitHub (8a7b177)
* **TFS-8827:** Deploy to artifactory (a1486ed)
* **TFS-9376:** Synchronize GitHub (3045ead)


### Documentation

* **TFS-8515:** Update Readme.md files (b344c47)

## 1.0.0 (2020-11-20)


### Features

* **core:** Add JupyterLab (36ecb63)
* **core:** Add MIT license header to all existing files (1558e56)
* **core:** Add TensorBoard to image classification notebook (740ddce)
* **TFS-2878:** Change project structure, use docker compose instead of docker file, add test pipeline, add Conda, virtualenv (3b3e576)
* **TFS-3644:** Use standard-version (6d5238c)
* **TFS-3668:** Parameterize test to use smaller epoch than in the actual notebook and timeout notebook tests in 20 minutes instead of 30 minutes. (2001bdd)
* **TFS-4982:** Add ipynb license metadata (cfc5d55)
* **TFS-6127:** Adjust notebooks (c053b51)


### Bug Fixes

* **common:** Update CONTRIBUTING.md header (06a9d84)
* **core:** Fix a bug in TensorBoard call (7f1ef24)
* **TFS-4039:** Fix cit findings on notebooks (de5e206)
* **TFS-4982:** Fix class list in image classification notebook. (a03806d)
* **TFS-6162:** h5py fix version to 2.x (8616259)


### Styling

* **common:** Clean up gitlab-ci and Readme.md (4318e22)
* **common:** Rephrasing Readme.md content description (13dfab3)


### Continuous Integration

* **core:** Add pb to artifacts (e36c34f)


### Tests

* **core:** Conda and virtualenv tests for Linux (2d77a18)


### Documentation

* **common:** Update CODE_OF_CONDUCT.md, CONTRIBUTING.md, LICENSE.md, and Readme.md files (dd4a949)
* **TFS-3645:** Add MIT License headers & LICENSE.md (b5da370)
* **TFS-6218:** Update licensing documents (c7441ca)


### Code Refactoring

* **core:** Remove a lib dependency & save test result ipynb as build artifact (4fdaee0)
* **TFS-2878:** Change structure, use compose instead of docker file, add test pipeline, add Conda, virtualenv and docker compose environment (d8756a4)
* **TFS-3674:** Use IPython magic instead of ! (7d6fc9e)
* **TFS-6162:** Simplify Keras model saving (91174ca)
* **TFS-6203:** Fix SET findings (cdba6d6)
* **TFS-6570:** Cherry pick environment changes from master (55ef92d)
* **TFS-6913:** Small improvements (3a29475)