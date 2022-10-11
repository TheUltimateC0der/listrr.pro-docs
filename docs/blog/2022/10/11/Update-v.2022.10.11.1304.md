---
hide:
  - navigation
  - toc
---

# Update v.2022.10.11.1304 is out now

A lot has changed under the hood in this release. The part that changed the most is extensability. I took the time to rewrite most of the code to make it as generic as possible. That way more metadata providers for informations such as ratings, genres, and other stuff can be added quickly.

This update includes two new metadata providers for ratings. A metadata provider integration to securely determine if a movie or show is a anime has been added too.

There are also new donor perks for all the awesome people that donate! So check out https://v2.listrr.pro/Donor/WhyDonate

## :rocket: New features :
- Dropped support for creating lists on trakt.tv. Take a look [here](https://github.com/trakt/api-help/discussions/350){:target="_blank"} to see why
- Added support for [listrr.pro.Sonarr](https://github.com/TheUltimateC0der/listrr.pro.Sonarr){:target="_blank"} bridge to be able to import listrr.pro lists into your Sonarr instances
- `Is Anime` filter to filter explicitly for anime movies or shows
- Added TMDB as metadata provider for ratings 
- Added IMDB as metadata provider for ratings
- List updates will now be triggered according to a users level
- If you connect your Discord account, you will be moved to your donor group automatically
- Added a easier to understand step by step guide to get the donor perks
- Update times for lists have been lowered from 24h to 3h for donors



## :bug: Bug Fixes:
- A few small not noteworthy bugs were fixed :wink:

## :notepad_spiral: Notes:
Nothing :shrug:

## :exploding_head: Known issues:
None, so far atleast... :heavy_check_mark: