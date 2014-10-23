.. highlight:: sh

===============
Git Cheetsheet
===============

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
  % git push -u origin master


Clone an existing repository::

  $git clone <url>

