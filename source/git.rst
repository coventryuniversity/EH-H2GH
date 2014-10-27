.. highlight:: sh

===============
Git Cheetsheet
===============

General Terminology
===================

Configuring Git
================

Set the username for commits::

   $ git config --global user.name "<name">

Set the Email for commits::

   $ git config --global user.email "<email>"


Create Repositories
===================

Create a new repository::

  $ git init
  ....
  $ git commit -m "First Commit"
  $ git remote add origin <url>
  $ git push -u origin master


Clone an existing repository::

  $ git clone <url>

Making Changes
==============

Get the status of the current repository::

  $get status

Getting the difference between files
------------------------------------

Those not staged::

  $ git diff

For a specific file::

  $ git diff <file>


Branches
---------

List Branches (and show current one)::

  $ git branch

Create a branch::

  $ git branch <name>

Switch to a branch::

  $ git checkout <name>

Commit data to a branch::

  $ git push <origin> <branch>


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

Provide a way to work on a feature without commiting to the main branch.

Create a new branch::

  $ git branch <name>

Navigate between branches::

  $ git checkout <branch>

Merge changes between branches::

  $ git merge <branch>

Remove a branch::

  $ git branch -d <name>


