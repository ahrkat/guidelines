# Methods Hub's Guidelines

You are interested in contributing a method or tutorial to the [Methods Hub](https://methodshub.gesis.org)? Here you can find all the information you need, for example:

* What is the aim of Methods Hub?
* What qualifies as a method? What qualifies as a tutorial?
* What are the Methods Hub's submission criteria?
* What do you need to prepare for your submission?
* Where and how can you get support?

## Aim of the Methods Hub
The Methods Hub aims to provide social scientists with high-quality, open-access, and easy-to-use computational resources. We want to promote the use of computational methods in the social sciences, lower technical barriers, and build a community-driven space for the field. We offer interactive execution environments so everyone can try the methods with the click of a button.

A **method** for the Methods Hub is a sequence of instructions that a computer should execute to perform a specific task and that is bundled for reusability, as well as its documentation (e.g., an R package).

A **tutorial** is an instructional resource that may be used as part of a self-guided learning process. Tutorials on the Methods Hub should focus on very concrete tasks and offer code that helps researchers to solve the task. This could be via applications of methods that are featured on the Methods Hub, but could also refer to methods published elsewhere. A tutorial can feature more than one method. Tutorials will be prefaced with what prior knowledge is expected from the user such that the user can judge themselves if they have the required skills to follow the tutorial.


## Publishing checklist
The Methods Hub accepts only resources that follow the principles of open science, are available in a format accessible to social scientists, and are relevant to social science research. A special focus of the Methods Hub is on resources that work on [digital behavioral data](https://www.gesis.org/en/institute/about-us/digital-behavioral-data), but other resources are also welcome.

To be included in the Methods Hub, a resource is checked to see if it fulfills the criteria in the [publishing checklist](#publishing-checklist) below. If you believe your resource meets these criteria, submit it for review on the [Methods Hub Portal](https://methodshub.gesis.org). More details on documentation and code quality, check the [Quality Criteria](guidelines.md#quality-criteria) section of the guidelines.

Each method or tutorial submitted to the [Methods Hub](https://methodshub.gesis.org/) is checked for compliance with the following criteria before publication.

### Openness criteria

- [ ] The method or tutorial is developed in an open-source programming language (e.g., Python or R).
- [ ] The method or tutorial is publicly accessible in a Git repository.
  - [ ] If a method, the Git repository has one and only one method.
- [ ] The method or tutorial is [published under an open license](https://opensource.guide/legal/#which-open-source-license-is-appropriate-for-my-project).

### Scoping criteria

- [ ] The method or tutorial is relevant for the social sciences.
- [ ] The method or tutorial belongs to a relevant task of the [Tasks Taxonomy].

  If none of the current tasks in the [Tasks Taxonomy] fits a method or tutorial, contact us at [methodshub@gesis.org][methodshub-email] to extend the taxonomy.

### Quality criteria

#### Documentation quality criteria

- [ ] The method or tutorial repository contains the [necessary files for setting up a binder environment](https://mybinder.readthedocs.io/en/latest/examples/sample_repos.html#managing-languages) for Methods Hub.
  - [ ] The method or tutorial repository contains the configuration files for installing all requirements (e.g., `environment.yml`, `requirements.txt`, `install.R`).
  - [ ] The method or tutorial repository contains the [postBuild](https://methodshub.gesis.org/snippet/postBuild) file that facilitates Quarto installation.
  - [ ] The binder environment is set up without errors.
- [ ] The method or tutorial repository contains a `LICENSE` file (corresponding to an [open license](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-license-to-a-repository)) at the root level of the repository.
- [ ] The method or tutorial repository contains a [`CITATION.cff`](https://citation-file-format.github.io/) file at the root level of the repository.
- [ ] The method or tutorial repository contains file, selected in the submission form, that follows the structure of the templates.

  If a method, this file must be a [Methods Hub friendly README](./method/template.md?plain=1) (can be  `README.me` or another file).

  If a tutorial, this file must be the tutorial itself in one of the accepted formats.

  | Format | File extension | Template | Notes |
  | --- | --- | --- | --- |
  | [Quarto](https://quarto.org/) | `.qmd` | [`tutorial/template.qmd`](tutorial/template.qmd) | |
  | [Jupyter Notebook Format](https://nbformat.readthedocs.io/en/latest/index.html) | `.ipynb` | [`tutorial/template.ipynb`](tutorial/template.ipynb) | Limited to a single programming language. |
  | [R Markdown](https://rmarkdown.rstudio.com/) |`.rmd` | | If possible, should be ported to Quarto. |
  | [(Pandoc) Markdown](https://pandoc.org/MANUAL.html#pandocs-markdown) | `.md` | | |
  
- [ ] All examples in the method or tutorial repository can be reproduced with reasonable accuracy using only publicly available resources.

#### Code quality criteria

The code quality criteria can be skipped for methods for which a paper is published by the following [trusted third-party review venues](guidelines.md#trusted-third-party-review-venues).

- [Journal of open source software](https://joss.theoj.org/)
- [The R journal](https://journal.r-project.org/)
- [R open science](https://ropensci.org/)

You can suggest further venues by mail to the [Methods Hub team][methodshub-email].

- [ ] The method code contains documentation (comments) for parameters and decisions that allows one to adjust the method.
- [ ] The method code is structured into modules (if need be).


## Frequently asked questions

1.  What is the Methods Hub?

    The Methods Hub is an infrastructure platform that provides openly accessible, reusable computational methods for working with digital behavioral data in social science research.

1.  Who can submit a method or tutorial to the Methods Hub?

    Researchers, practitioners, and developers in computational social science, computer science, natural language processing and related fields can submit methods or tutorial.

1.  Can I publish my computational method on Methods Hub?

    Yes, only if it is open access and open licensed, and belongs to a relevant task of the [Tasks Taxonomy].

1.  How can I increase my chances of getting my method published?

    By providing well written documentation following README template, providing all necessary files and making the code reusable without/with minimal user involvement.

1.  Which programming languages are supported?

    The platform supports **only** open source programming languages such as Python and R.

1.  Can I publish my method or tutorial using paid API or tool?

    No, the methods or tutorial on Methods Hub must be fully resusable with all resources used by the method including APIs, packages being openly accessible to all.

1.  What if my method is already published in a peer-reviewed journal?

    Methods published in trusted third-party venues with proper documentation and code quality can be submitted directly.

1.  Should I write tutorial about my method?

    Yes, tutorials increase the reach of a method to researchers and practitioners with limited practical experience of artificial intelligence methods. It is therefore, highly advised to write tutorial demonstrating the use of your method to a research question as step-by-step guide.

1.  Can I write tutorial about someone else's method?

    Yes, you can write a tutorial about other developers methods as your contribution. You can also write tutorials about methods not published on Methods Hub but are of interest to the Methods Hub audience.

1.  Where should the method or tutorial code be hosted?

    The method or tutorial must be publicly accessible from a Git repository, this includes GitHub, GitLab and others.

1.  What happens when I submit my method?

    When the method is submitted, it is held for review. During this period the reviewer(s) can add issues to the Git Repository if modifications are needed. Once there is no issue to resolve, the method is published on the portal.

1.  What does it mean that a method is published?

    When a method is published, it appears in the Methods Hub gallery and (from next day) is searchable through GESIS Search.

1.  What are the differences between code processed by `knitr` and `jupyter`?

    There is one subtle, but important, difference between the code execution between `knitr` (the default renderer for R code in `quarto`) and jupyter. For example, this R code block (see the provided file `code_exec.qmd`)

    ````
    ```{r}
    mean(mtcars$mpg)
    plot(mtcars$mpg, mtcars$wt)
    ```
    ````

    When rendering this into notebook by [Quarto] using

    ```sh
    quarto render code_exec.qmd --to=ipynb
    ```

    All code blocks will be rendered but also will get modified with the plotting line removed. It's not ideal. So, there two ways to fix this:

    Convert it is by using `quarto convert` instead to generate an empty ipynb.

    ```sh
    quarto convert code_exec.qmd -o code_exec.ipynb
    ```

    Or, to split the code block into one line per block. And for the plot code, you must add the execution option. Only in this case, `quarto render` will not eat the visualization code.

    ````
    ```{r}
    mean(mtcars$mpg)
    ```

    ```{r}
    #| echo: true
    plot(mtcars$mpg, mtcars$wt)
    ```
    ````

## Contact

Methods Hub Team &lt;[methodshub@gesis.org][methodshub-email]&gt;

[methodshub-email]: mailto:methodshub@gesis.org
[Tasks Taxonomy]: https://methodshub.gesis.org/about/how-to-submit/taxonomy
