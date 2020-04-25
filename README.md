# Contribute

La documentation est écrite en .rst soit en reStructuredText, voici quelques ressources si vous souhaitez contribuer:  
The documentation is written in .rst or reStructuredText, here are some resources if you wish to contribute:
- FR : https://github.com/DevDungeon/reStructuredText-Documentation-Reference#introduction  
- EN : http://espe-rtd-reflexpro.u-ga.fr/docs/sandbox2/fr/latest/syntaxe_rest.html  
- EN : http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html
- EN : https://www.sphinx-doc.org/en/master/
- EN : https://www.ericholscher.com/blog/2016/jul/1/sphinx-and-rtd-for-writers/
## Change important inforamtion in conf.py

**In `docs/conf.py`:**
```python
# -- Project information -----------------------------------------------------
# Ne pas modifier | Do not modify
project = u'FriendlyBot'
# Juste modifier l'année ^^ | Just change the year ^^
copyright = u'2020, FriendlyBot Staff'
# Ne pas modifier | Do not modify
author = u'FriendlyBot Staff'

# The short X.Y version
# Adapter à la version de FriendlyBot | Adapting to the FriendlyBot version
version = u'1.0'
# The full version, including alpha/beta/rc tags
# Adapter à la version | Adapting to the FriendlyBot version
release = u'closed-beta'
```

# How to create a PDF with Sphinx documentation tool

Take a look at :

- https://www.sphinx-doc.org/en/master/faq.html

- https://github.com/brechtm/rinohtype