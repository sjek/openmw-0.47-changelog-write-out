# openmw-0.47-changelog-write-out

the documentation build from this source resides in

  https://openmw-047-changelog-write-out.readthedocs.io/en/latest/

to set this up i have used following procedure

if you are cloning and adding unto this repository, you can skip 3, 4 and 5

1) install sphinx and it's reguirements

2) install git gui for windows

3) creating this prepository

4) after cloning, opening cmd in root directory and executing sphinx-quickstart

5)  then in created conf.py i added onto extensions

        'sphinx.ext.autodoc',
        'sphinx.ext.doctest',
        'sphinx.ext.todo',
        'sphinx.ext.coverage',
        'sphinx.ext.viewcode',
        'sphinx.ext.autosectionlabel',

    and under them

        autosectionlabel_prefix_document = True

    then under "templates_path = ['_templates']"

        # The master toctree document.
        master_doc = 'index'

    as html theme using

        html_theme = 'sphinx_rtd_theme'

6) for formatting, there's quickstart guide in

        https://www.sphinx-doc.org/en/master/usage/quickstart.html

7) for making a pull request you need first a clone of this one.

not sure yet how it works from forked repository but i need different branch

from default one to get my ide ie. atom to work well. then using that different

branch as a base for new commits which of i then make a pull request for default branch.

that pull request i then merge to make it go to readthedocs build process and the document. 
