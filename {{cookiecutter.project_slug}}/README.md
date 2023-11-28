---
title: "{{ cookiecutter.project_slug }}: {{ cookiecutter.project_name }}"
author: {{ cookiecutter.full_name }}
date: {{ cookiecutter.date }}
---

This folder contains all files related to the project "{{ cookiecutter.project_name }}" directed by …
The team members are …

This folder is called `{{ cookiecutter.project_slug }}`. Notice …

The structure of this folder follows good practices for project data management. The first-level subdirectories should not be changed or renamed. Anything new should be inside these folders. If you think you need another folder, please discuss with Dr. Aravena before. The roles of these subdirectories are the following.

# data

This folder contains raw and preprocessed data generated outside the project. Raw data (stored in the `data/raw` subfolder) should be exactly as downloaded from external sources. It should never be modified.

Processed data is stored directly in the `data` folder. It is derived from raw data using a script (stored in the `code` folder) that tidies up the values so they can be used by the programs in the **code** folders.

None of the files in data/raw is created by us. If there is no need for data preprocessing or tidying up, then raw data can be stored directly in `data`.

A `README` file should be included describing how and when the data was obtained, and how it can be downloaded again.

# code

This folder contains executable code that reads files from the `data` folder, does some calculations and manipulations, and stores the results in the `results` folder. Temporary files should ideally be stored outside the project folder, in storage local to the user's computer.

The code should be designed assuming that the current directory is the project root `IBD_ML`.

All (or almost all) the files in this folder are created by the team. Anything derived from online resources should be documented as such, indicating the source.

The versions of programs in this folder are experimental and may be changed by anybody in the team. The official code should be stored in a *git* repository outside this project folder. Files managed by git should not be placed in this shared folder, since they are easily corrupted when several persons work on the same code. An alternative is to create a separate project folder in local storage with links to all the folders described here, except for the `code` subdirectory, which in that case will be a *git* repository.

# results

This folder holds the results of applying `code` into `data`. We expect that most files are in text format (maybe comma separated or tab separated) or application specific formats. When the code produces images that can be used as figures in the document, it may be convenient to store them in the `docs` folder.

All files in this folder should be produced by programs in `code` in a reproducible way. Data produced outside the project should **not** be stored here.

# docs

This folder contains the documents describing the project, including the final report or paper to be submitted. It is a means of communication between the team members. The preferred format is Google Documents. It may also contain the images produced by programs in `code`.

# bib

This folder contains PDF versions of all papers and scientific literature relevant to the project. It may also contain a bibliography file in BiBTeX format or equivalent.

These are documents that can be cited in the partial or final reports, or in the paper reporting this research. Basically, if the document has a *doi*, then it should be stored here.

# extra

This folder contains reference material that may be relevant to the project, besides published papers. For instance, presentations or web pages that cannot be cited easily.

