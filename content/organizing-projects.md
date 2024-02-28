# Organizing your projects

```{objectives}
- Get an introduction to version control
- Get an overview on how to organize research projects
```

```{instructor-note}
- 15 min teaching incl. demo and discussions
```

One of the most basic steps to make your work reproducible is to organize your projects well.
Let's go over some of the basic things which people have found to work (and not to work).


## Directory structure for projects

- Project files in a **single folder**
- **Different projects** should have **separate folders**
- Use **consistent and informative directory structure**
  - Avoid spaces in directory and file names – it is uglier for humans but handy for computers.
- If you need to separate public/private, you can put them in public and private Git repos
  - If you need to separate public/secret, use `.gitignore` or a separate folder that's not in Git
- Add a **README file** to describe the project and instructions on reproducing the results
- If a software is reused in several projects it can make sense to put them in own repo

A project directory can look something like this:
```shell
project_name/
├── README.md             # overview of the project
├── data/                 # data files used in the project
│   ├── README.md         # describes where data came from
│   └── sub-folder/       # may contain subdirectories
├── processed_data/       # intermediate files from the analysis
├── manuscript/           # manuscript describing the results
├── results/              # results of the analysis (data, tables, figures)
├── src/                  # contains all code in the project
│   ├── LICENSE           # license for your code
│   ├── requirements.txt  # software requirements and dependencies
│   └── ...
└── doc/                  # documentation for your project
    ├── index.rst
    └── ...
```
---

## Tracking files with git

### Demonstration with graphical user interface

````{challenge} Demonstration
We use a simple word-count repository in demonstrations and exercises
(<https://github.com/coderefinery/word-count>). We should clone the
repository already to prepare to work on it.

On VSCode (many other interfaces exist and are just as good)
 - Open command palette and type clone
 - paste the URL of the repository to clone
 - use the file dialog to find a place for it
 - Create a new file and make a change to an existing one.
 - Add them to the repository and push online.
 - See the changes online.
````

* Git workflow:
  1. Add files
  2. Commit (save to Git)
  3. Push (save online)

* Check the [Git-intro lesson](https://coderefinery.github.io/git-intro/) for a lot more details.


## Licensing

Software and data is only usable by others if you include a license. You cannot use someone else's
public code if it does not have a license attached.

- Publishing you work openly also allows you to access it in the future. Otherwise it might belong
  to the institution you are working for.
- Everyone who contributed should agree to the license. So do this early rather than late.

Examples:
 - MIT: Very open, your code can be used in commercial applications.
 - GPL: Copyleft, any code derived from yours must be GPL and open
 - Creative Commons: Mostly for data, text and artistic work. This course is published under CC-by

See the [CodeRefinery course](https://coderefinery.github.io/social-coding/software-licensing/) for
details.


## Citations

Software can be a scientific publication, similarly to a dataset.

Making citing as easy as possible:
 - Add a file called [CITATION.cff](https://citation-file-format.github.io/)
   ([example](https://github.com/bast/runtest/blob/main/CITATION.cff)).
 - Get a [digital object identifier (DOI)](https://en.wikipedia.org/wiki/Digital_object_identifier)
   from [Zenodo](https://zenodo.org/)

There are also journals that focus on software 
([“In which journals should I publish my software?” (Neil P. Chue Hong)](https://www.software.ac.uk/top-tip/which-journals-should-i-publish-my-software)).
They guarantee a higher standard for scientific software. For example, they can require automated
testing and documentation of the software.


## Tracking source code, data, and results

- All code is version controlled and goes in the `src/` or `source/` directory
- Include appropriate LICENSE file and information on software requirements
- You can also version control data files or input files under `data/`
- If data files are too large (or sensitive) to track, untrack them using `.gitignore`
- Intermediate files from the analysis are kept in `processed_data/`
- Consider using Git tags to mark specific versions of results (version
  submitted to a journal, dissertation version, poster version, etc.)

---

## Reproducible publications

- Git can be used to collaborate on manuscripts written in, e.g., LaTeX and other text-based formats but other tools exist:
  - [Overleaf](https://www.overleaf.com): an online, collaborative LaTeX editor (has Git integration)
  - [Authorea](https://www.authorea.com): collaborative platform for preprints (apparently also has Git integration)
  - [HackMD](https://hackmd.io/): an online collaborative Markdown editor (has Git integration)
  - [Manuscripts.io](https://www.manuscripts.io/): a collaborative authoring tool that support scientific content and reproducibility.
  - Google Docs can be a good alternative

- Many tools exist to assist in making scholarly output reproducible:
  - [rrtools](https://github.com/benmarwick/rrtools): instructions, templates, and functions for writing a reproducible article or report with R.
  - [Jupyter Notebooks](https://jupyter.org): web-based computational environment for creating code and text based notebooks that can be used as, see also our [Jupyter lesson](https://coderefinery.github.io/jupyter/) later in this workshop.
    supplementary material for articles.
  - [Binder](https://mybinder.org): makes a repository with Jupyter notebooks available in an executable environment (discussed later in the [Jupyter lesson](https://coderefinery.github.io/jupyter/)).
  - ["Research compendia"](http://inundata.org/talks/rstd19/#/): a set of good practices for
    reproducible data analysis in R, but much is transferable to other languages.

```{seealso}
Do you want to practice your reproducibility skills and get inspired by working with other people's code/data? Join a [ReproHack event](https://www.reprohack.org/event/)!
```


---

## Discussion on reproducibility

````{discussion} Discuss in collaborative document or with your team members
**How do you collaborate on writing academic papers?**
```
- Are you using version control for academic papers?
  - ...
  - ...
  - (share your experience)

- How do you handle collaborative issues e.g. conflicting changes?
  - ...
  - ...
  - (share your experience)
```
> Please write or discuss your ideas before opening solution!

```{solution}
- Consider using version control for manuscripts as well. It may help you when keeping track of edits + if you sync it online then you don't have to worry about losing your work.

- Collaboration can be done efficiently by
  - real time collaboration tools like HackMD/HedgeDoc where conflicts are resolved on the fly
  - version control where conflicts are detected and shown – and solved manually
```
````

````{discussion} Discuss in collaborative document or with your team members
```
- What tools are you using when organizing your projects?
  - ...
  - ...
  - (share your experience)
```
````


```{keypoints}
- An organized project directory structure helps with reproducibility.
- Reproducibility makes work easier for the next person working on the project - and that might be you in a few years!
```
