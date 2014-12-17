.. highlight:: sh

===
Git 
===

General Terminology
===================


Configuring Git
================

These Settings are great for a single user on one machine.

.. NOTE::

    Use the **--local** flag for per-repository settings (i.e. if running on a Flash drive)


Set the username for commits::

   $ git config --global user.name "<name">

Set the Email for commits::

   $ git config --global user.email "<email>"


Create Repositories
===================

Create a new repository from scratch::

  $ git init
  ....
  $ git commit -m "First Commit"
  $ git remote add origin <url>
  $ git push -u origin master


Clone an existing repository::

  $ git clone <url>

Check URL's for a given repository::

  $ git remote -v

Making Changes
==============

Get the status of the current repository::

  $ git status

Add a modified file to the staging area::

  $ git add <file>
  #Or to add all
  $ git add

Remove a file from the staging area (keeping original)::

  $ git rm --cache <file>
  #Or to remove original too
  $ git rm <file>


Getting the difference between files
------------------------------------

Those not staged::

  $ git diff

For a specific file::

  $ git diff <file>



General Workflow
================

Pull any recent changes from the remote repository::

  $ git pull 
  #... HACK AWAY ...
  $ git status  #Shows status of files
  $ git add <whatever>  #Add file to list of changes
  $ git commit -m <sensible commit message>

  #Push changes to remote repo
  $ git push


Branches
========

Provide a way to work on a feature without committing to the main branch.

Create a new branch::

  $ git branch <name>

Navigate between branches::

  $ git checkout <branch>

Check in to a branch::

  $ git push origin <branch>

Merge changes between branches::

  $ git merge <branch>

Remove a branch::

  $ git branch -d <name>


Forks
======

A fork is a copy of a repository.  Forking allows us to modify the code within 
a repository without affecting the original project.  Forks can be used as a a starting point for your own project, or to propose changes to the original code.


Forking a repository
---------------------

In github click fork and define the forked repository name
You can then clone and work in your forked version of the repo.

Synchronising Forks with the upstream repository
-------------------------------------------------
Setting up so changes to upstream repository can also be pulled::

  $ git remote add upstream <upstream-url>

Fetch the latest upstream repo::

  $ git fetch upstream

Checkout the master branch::

  $ git checkout master

And Merge with the upstream/master::

  $ git merge upstream/master

.. NOTE::  
  
  Don't forget to push any changes


Submitting Pull Requests
-------------------------

After forking a project, you may want the features you have developed to be 
integrated into the original code base.  For this we can use a pull request.

To submit a pull request use the *compare and review* button in github.

This will bring up a screen that allows you to check the review you have made, before submitting a pull request.




