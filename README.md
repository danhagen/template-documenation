# Documentation Template

We will use this repository as a template for additional documentation repositories.

## Getting Started

I highly recommend using [Visual Studio Code](https://code.visualstudio.com/)
with the
[LaTeX Workshop extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
for this project. This is the recommended setup because I believe that it provides
the best development environment. Also, the committed VS Code settings file,
[`settings.json`](.vscode/settings.json), will help to keep the repository clean of
build files. All files in the [build](build) are not tracked by the repository, with
the exception of the resulting [PDF document](build/main.pdf).

It is highly recommended that you use [Tex Live](https://www.tug.org/texlive/) as the LaTeX compiler with the extension. Follow the instructions given
[here](https://www.tug.org/texlive/windows.html)
to install for Windows. The default settings for the installer will install A LOT of
packages, which will take a very long time. The default installation is recommended
for now until we can determine the minimal installation required. Perform the
installation when you have at least an hour downtime (e.g., getting lunch or
overnight) to avoid disruption to your work.

### Using LaTeX

The document in this repository is created using
[LaTeX](https://www.latex-project.org/), which is a high-quality typesetting system.
It includes features designed for the production of technical and scientific
documentation. If you are not familiar with LaTeX, or are not familiar with the commands
used in this document, I recommend looking at the
[documentation from Overleaf](https://www.overleaf.com/learn). If you are new to
LaTeX, the
[Learn LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes) tutorial from [Overleaf](https://www.overleaf.com)
is a great place to get started.

### Git Submodules

This repository uses a git submodule. So when you clone use the following command

```bash
git clone --recurse-submodules <repo-url>
```

If you have already cloned the repo and did not use the correct arguments to initialize
the submodule you can use the following command from within the directory that the
repo was cloned into

```bash
git submodule update --init
```

Note that with git submodules any changes made in the submodule
folder will not be made committed when you make a commit from the main repository.
Git submodules are like a repo within a repo. So if you make changes to
the submodule you must first change your current directory to the submodule
directory. From the submodule directory you can add and commit to the
submodule repository like normal. Refer to the
[git submodule documentation](https://git-scm.com/docs/git-submodule)
for more details on using submodules.

### Using Markdown

If you need to update this README but you're not familiar with Markdown I recommend
looking at [this Markdown guide](https://www.markdownguide.org/).
[This cheat sheet](https://www.markdownguide.org/cheat-sheet/) from the
Markdown guide website is an especially helpful resource. Note that since we
use GitLab as our git repository what you see using a
[Markdown preview](https://code.visualstudio.com/docs/languages/markdown#_markdown-preview)
in VS Code might differ slightly from what you see viewing the README in the repository. For details on the differences refer to the
[GitLab Flavored Markdown documentation](https://docs.gitlab.com/ee/user/markdown.html).

### Visual Studio Code

VS Code has a lot of great extensions that can make you a more efficient
developer. One that I recommend when working with projects like this
one that are version controlled using Git is
[GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens).
VS Code comes with a standard source control extension. However, GitLens
provides additional functionality that can be helpful.

One feature in VS Code that can help make you more efficient
is code snippets. Code snippets are templates that make it easier to enter
repeating code patterns, such as loops, conditional-statements, or in
the case of LaTeX figures, tables, etc. Some LaTeX code snippets that we
have created so far are defined in
[latex.code-snippets](.vscode/latex.code-snippets). If you would like
to create and add your own code snippets please refer to the
[VS Code documentation on code snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets).

## Guidelines

- Each section should be its own tex document and should go in the
[sections](sections) directory.
- Images for figures should be place in the [figures](figures)
directory