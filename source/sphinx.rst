==================
Sphinx Quick start
==================

About Sphinx
=============

Sphinx is a tool that makes it easy to create documentation.
It was designed (and is used) for the python documentation, but can be used to document projects in several other languages. It can also be used (like in the H^2GH) to document non programming projects

Sphinx uses 
`Restructured Text (RST) <http://docutils.sourceforge.net/rst.html>`_
as a markup language.  
This guide is intended to give a basic introduction to RST and the use of sphinx


Using Sphinx
============

Adding new content to the master document
------------------------------------------

To create a new document make a file with a *.rst* extension in the source folder.

To include this in the sphinx build we need to edit the *index.rst* file.
Add the new document (without the rst extension) to the Contents section of the index.rst file::

  Contents:

  .. toctree::
   :maxdepth: 2

   sphinx
   git
   <whatever>




Building the documentation
---------------------------

Sphinx supports many output formats (just type make to see what is supported)
To build the documentation use the Makefile::

  make html


The generated documentation can be found in the *build* directory


Restructured Text Primer
=========================

This section is intended to act as a quick reference to restructured text markup
for more details see the `Sphinx Docs <http://sphinx-doc.org/rest.html>`_

General Text formatting
-------------------------

Paragraphs are made up of lines of text separated by *one or more* blank lines. 

Text can also have basic formatting applied

* One asterisk ``*text*`` for *italics*
* Two asterisks ``**text**`` for **Bold**

.. NOTE::

   As in python indentation is significant in reST.
   All lines of the same paragraph (or block of text) should have the
   same level of indentation


Comments can also be included::

  .. single line comment

  .. 
     Multiple line comment
     It stops when indentation goes back to normal



Headings
--------

Headings are defined as follows::

  ============
  Part Heading
  ============


  Section Heading
  ===============

  subsection heading
  -------------------


Lists
------

Lists are defined using::

  * Bullet List
  * Another Bullet
    * Sub Bullet

  #. Numbered List
  #. Second numbered item

  Term (up to a line)
    Definition of the term


Sourcecode
----------

There are two ways of defining sections of sourcecode.
The first is to end a paragraph with ``::`` then add source code (indented) in a new paragraph below.::

  Normal Text::

    This will be rendered as source code
    Note that the first line of indentation (defining the block) will be removed 

    The source can span multiple paragraphs

  Removing the indent will return us to normal text mode


The second way of defining source code is to use a ``.. code-block::`` directive::

  .. code-block:: <language>

    Some python code can go here.


     
  



  










