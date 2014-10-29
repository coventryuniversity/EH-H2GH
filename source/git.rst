.. highlight:: sh

===============
Git Cheetsheet
===============

General Terminology
===================

Configuring Git
================

These Settings are great for a single user on one machine.
Use the **--local** flag for per-repository settings (i.e. if running on a Flash drive)

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

Check URL's for a given repository::

  $ git remote -v

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

Checkin to a branch::

  $ git push origin <branch>

Merge changes between branches::

  $ git merge <branch>

Remove a branch::

  $ git branch -d <name>

Forks
======

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
  
  Dont forget to push any changes

