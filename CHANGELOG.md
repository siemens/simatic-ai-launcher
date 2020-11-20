# Changelog

All notable changes to this project will be documented in this file. See standard-version for commit guidelines.

## 1.0.0 (2020-11-20)


### Features

* **core:** Add jupyterlab (36ecb63)
* **core:** Add MIT license header to all existing files (1558e56)
* **core:** Add TensorBoard to image classification notebook (740ddce)
* **TFS-2878:** Change project structure, use docker compose instead of docker file, add test pipeline, add conda, virtualenv (3b3e576)
* **TFS-3644:** Use standard-version (6d5238c)
* **TFS-3668:** Parameterize test to use smaller epoch than in the actual notebook and timeout notebook tests in 20 minutes instead of 30 minutes. (2001bdd)
* **TFS-4982:** Add ipynb license metadata (cfc5d55)
* **TFS-6127:** Adjust notebooks (c053b51)


### Bug Fixes

* **common:** Update CONTRIBUTING.md header (06a9d84)
* **core:** Fix a bug in Tensorboard call (7f1ef24)
* **TFS-4039:** Fix cit findings on notebooks (de5e206)
* **TFS-4982:** Fix class list in image classification notebook. (a03806d)
* **tfs-6162:** h5py fix version to 2.x (8616259)


### Styling

* **common:** Clean up gitlab-ci and readme.md (4318e22)
* **common:** Rephrasing Readme.md content description (13dfab3)


### Continuous Integration

* **core:** Add pb to artifacts (e36c34f)


### Tests

* **core:** Conda and virtualenv tests for linux (2d77a18)


### Documentation

* **common:** Update CODE_OF_CONDUCT.md, CONTRIBUTING.md, LICENSE.md, and readme files (dd4a949)
* **TFS-3645:** Add MIT License headers & LICENSE.md (b5da370)
* **TFS-6218:** update licensing documents (c7441ca)


### Code Refactoring

* **core:** Remove a lib dependency & save test result ipynb as build artifact (4fdaee0)
* **TFS-2878:** Change structure, use compose instead of docker file, add test pipeline, add conda, virtualenv and docker compose environment (d8756a4)
* **TFS-3674:** Use ipython magic instead of ! (7d6fc9e)
* **TFS-6162:** Simplify Keras model saving (91174ca)
* **TFS-6203:** Fix SET findings (cdba6d6)
* **TFS-6570:** Cherry pick environment changes from master (55ef92d)
* **TFS-6913:** small improvements (3a29475)