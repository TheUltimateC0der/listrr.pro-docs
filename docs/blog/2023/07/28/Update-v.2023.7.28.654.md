---
title: Update v.2023.7.28.654 is out now
author: Ultimate
tags:
  - V2
  - Patchnotes
hide:
  - navigation
---

# Update v.2023.7.28.654 is out now

## :rocket: New features
- Added a link for "API Docs" to the menu to make it more obvious to the user that we have an API
- Added discord url to openapi description, so developers can ask questions and get help quickly


## :bug: Bug Fixes
- Fixed a :bug: where a not existing ExternalId object in the DB lead to failure of the job that should update every movie
  - Found and removed 31 movies from the DB that had the ExternalId object not set
  - Added a null check to the job so that these items get ignored in the future

## :notepad_spiral: Notes
None

## :exploding_head: Known issues
None, so far atleast...