# openmw-0.47-changelog-write-out

to set this up i have used following procedure

install sphinx and it's reguirements

install git gui for windows

creating this prepository and cloning it

opening cmd in root directory and executing sphinx-quickstart

then in created conf.py i added

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
