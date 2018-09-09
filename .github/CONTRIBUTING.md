How to contribute to the Runbook
================================

This guide is a short introduction on how to contribute to the Runbook.
Follow these steps to make a new contribution.


## Style guide

All documents are written in **reStructuredText**.
reStructuredText is a markup language (similar to GitHub-Flavored Markdown).
See the [reStructuredText quick reference](http://docutils.sourceforge.net/docs/user/rst/quickref.html "How to write reStructuredText") to get started.
Optionally, the [Sphinx documentation](https://media.readthedocs.org/pdf/sphinx/stable/sphinx.pdf "Further reading on Sphinx syntax and other advanced features") may be useful.
All contributions should follow the [**style guide for Sphinx-based documentation**](https://documentation-style-guide-sphinx.readthedocs.io/en/latest/index.html "Style guide for Sphinx-based reStructuredText documentation").

For examples, see any pre-existing documentation.

### Line convention

Our style guide breaks from the above style guide in one key way: **write each sentence in a document on a new line**.
This is awkward to write, but it renders the same and makes changes (i.e. _diffs_) easier to read.
Make a paragraph by leaving an empty line between sections.
Inside of a pull request, it takes less time to figure out what someone actually changed.

Advanced writing tip: it also makes you more conscious of how long your sentences are.
Shorter sentences are always preferred.


## How to test changes

**Use pipenv to set up your environment and _make_ the Runbook.**

### Set up environment

The Runbook uses [**pipenv**](https://pipenv.readthedocs.io/en/latest/) to manage virtual environments (a.k.a. virtualenvs).
`pipenv` is a tool to make dependency management easier.
It also makes using Python virtual environments easier.
See the [pipenv installation guide](https://pipenv.readthedocs.io/en/latest/install/) to get started.

Once installed, run these commands inside the Runbook directory to initialize your project:

```bash
pipenv shell
pipenv sync
```

### Build new changes

Once your environment is set up, test your changes and check the appearance in the browser.

`pipenv shell` sets up a new virtualenv for the project.
It pre-loads both the documentation toolchain and the same theme we use for [runbook.ritlug.com](http://runbook.ritlug.com/).
When these dependencies are loaded, testing changes is easy.

Run the **`test.sh` script** to build updated documentation.
After completing, rendered HTML is placed into `docs/_build`.
All HTML files are found in `docs/_build/html/`.
If you are using a Linux machine with Firefox installed, run this command in the terminal for a handy shortcut:

```bash
firefox docs/_build/html/index.html
```

Review your changes.
Make sure links still work and formatting is not broken.
If it looks good, it is time to make a pull request.


## How to get your pull request merged

Follow these steps to get your pull request merged:

1. Follow the style guide (explained above)
2. Test your changes and make sure it appears correctly (explained above)
3. Make a pull request to RITlug/runbook.
    * In the side bar for **Labels**, choose the `doc:` label for any categories with docs you changed in your PR (for example, if I edit the _Semester Checklist_, I choose the `doc: Tasks` label)
    * In the side bar for **Projects**, add the PR to **[RITlug operations](https://github.com/orgs/RITlug/projects/1?fullscreen=true)** project board
4. [_recommended_] Add a screenshot of the rendered documentation in your PR
    * This makes PRs way easier for fellow eboard members to review!
5. Get two other approved reviews by eboard members
    * This requirement helps keep everyone current on additions and removals to the Runbook

