# openmw-0.47-changelog-write-out

the documentation build from this source resides in

  https://openmw-047-changelog-write-out.readthedocs.io/en/latest/
  
for contributing you need a clone (2)

setting this up i have used following procedure

if you are cloning and adding unto this repository, you can skip 3, 4 and 5



1 is needed if you want to build html documentation locally:  

```
( by writing cmd in address field, hit enter and using "make html" command.
it will build the files into _build folder generated by sphinx-quickstart.
for keeping this repository simple, don't commit those files into here. )
```


1) install sphinx and it's reguirements

2) install git gui for windows for cloning (there are other ways but i used this)

```
this is kinda self explanatory, go to the desired folder, 
open git gui via dropdown menu, choose cloning, 
give source address from github page (green "code" dropdown) and
desired source folder name
clone
that's it, now you have a clone which can be used to contribute
```

3) creating this prepository

4) after cloning, opening cmd in root directory and executing sphinx-quickstart

5)  then in created conf.py i added onto extensions

```
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
        
```

6) for formatting, there's quickstart guide in

     https://www.sphinx-doc.org/en/master/usage/quickstart.html

7) for making a pull request you need first a clone of this one.

```
    not sure yet how it works from forked repository but i need different branch
    from default one to get my ide ie. atom to work well. then using that different
    branch as a base for new commits which of i then make a pull request for default branch.
    that pull request i then merge to make it go to readthedocs build process and the document.
```
