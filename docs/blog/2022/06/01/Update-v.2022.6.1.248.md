---
hide:
  - navigation
  - toc
---

# Update v.2022.6.1.248 is out now

## :rocket: New features :
- You are now able to add your radarr instances. When adding a radarr instance, the URL and API Key you enter is saved encrypted in the database.
- When creating a list, you can select the radarr instances you want to add this list to.
- The `Management` menu has been extended to `Starr Instances` to manage your Radarr and Sonarr instances
- You are able to decide if you want to create your list on trakt.tv or not.
- You are now able to decide if you want to create your list on TMDb or not. (Implementation not done yet)
- You can choose to call notifiarr on updates. (Implementation not done yet)


## :bug: Bug Fixes:
- The `Last Processed` timestamp of a new created list was incorrect
- When a list isn´t populated yet, and the `Custom List` URL is added to radarr, the list will fail to add until the list is populated with items. This is now fixed. Even if the list is not populated, the list will be able to get saved
- A few small not noteworthy bugs were fixed
- Re-Added the /Donors/WhyDonate page

## :notepad_spiral: Notes:
Views have been consolidated internally. If you see a wrong labeled button or text input, please report.

## :exploding_head: Known issues:
None, so far atleast...