# openmw-0.47-changelog-write-out

to set this up i have used following procedure

1) install sphinx and it's reguirements

2) install git gui for windows

3) creating this prepository

4) opening cmd in root directory and executing sphinx-quickstart

5)  then in created conf.py i added

        'sphinx.ext.autodoc',
        'sphinx.ext.doctest',
        'sphinx.ext.todo',
        'sphinx.ext.coverage',
        'sphinx.ext.viewcode',
        'sphinx.ext.autosectionlabel',

    onto extensions and under them

        autosectionlabel_prefix_document = True

    then under "templates_path = ['_templates']"

        # The master toctree document.
        master_doc = 'index'

    as html theme using

        html_theme = 'sphinx_rtd_theme'
