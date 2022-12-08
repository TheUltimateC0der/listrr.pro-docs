# Sonarr Bridge Setup

## Get your stuff together
For setting up the Sonarr bridge, you need the follwing:

1. The domain/hostname/ip of your Sonarr instance
2. The API Key of your Sonarr instance
3. Your listrr.pro API Key which you can find [here](https://listrr.pro/Identity/Account/Manage){:target="_blank"}
4. Docker installed on your server
5. docker-compose installed on your server
6. Create a directory for your sonarr bridge instance where you can store files for it

## General setup
In the directory you created for your sonarr bridge, create a file named `docker-compose.yml`. We will add the following content to it.


## Example docker-compose.yml
```yml
version: "3.9"
   
services:
  sonarrbridge:
    image: ghcr.io/theultimatec0der/listrr.pro.sonarr:latest
    environment:
      # This is your Sonarr instance setting
      - SonarrInstance__Url=https://sonarr.mydomain.tld
      - SonarrInstance__ApiKey=YOUR-SONARR-API-KEY
      # This is for automatically importing your own lists from your listrr.pro V2 account
      - listrr__AutoImport__ImportLists=true
      - listrr__AutoImport__ApiKey=YOUR-LISTRR-PRO-V2-API-KEY
      - listrr__AutoImport__QualityProfileId=1
      - listrr__AutoImport__RootFolderId=1
      - listrr__AutoImport__LanguageProfileId=1
      - listrr__AutoImport__Monitored=true
      - listrr__AutoImport__SearchForMissingEpisodes=true
      - listrr__AutoImport__SearchForCutoffUnmetEpisodes=true
      - listrr__AutoImport__SeasonFolder=true
      - listrr__AutoImport__Tags__0=1
      - listrr__AutoImport__Tags__1=5
      # This is for importing listrr.pro V2 lists by their Ids
      - listrr__Lists__0__Id=A-LISTRR-V2-LIST-ID
      - listrr__Lists__0__QualityProfileId=1
      - listrr__Lists__0__RootFolderId=1
      - listrr__Lists__0__LanguageProfileId=1
      - listrr__Lists__0__Monitored=true
      - listrr__Lists__0__SearchForMissingEpisodes=true
      - listrr__Lists__0__SearchForCutoffUnmetEpisodes=true
      - listrr__Lists__0__SeasonFolders=true
      - listrr__Lists__0__Tags__0=1
      - listrr__Lists__0__Tags__1=35
      - listrr__Lists__0__Tags__2=50
      - listrr__Lists__1__Id=A-LISTRR-V2-LIST-ID
      - listrr__Lists__1__QualityProfileId=1
      - listrr__Lists__1__RootFolderId=1
      - listrr__Lists__1__LanguageProfileId=1
      - listrr__Lists__1__Monitored=true
      - listrr__Lists__1__SearchForMissingEpisodes=true
      - listrr__Lists__1__SearchForCutoffUnmetEpisodes=true
      - listrr__Lists__1__SeasonFolders=true
      - listrr__Lists__1__Tags__0=1
      - listrr__Lists__1__Tags__1=3
      - listrr__Lists__1__Tags__2=7

```

## Settings explained
This `docker-compose.yml` is divided into multiple blocks. Each block has a seperate purpose. The purpose of each block is explained below.

### Sonarr Instance
```yml
# This is your Sonarr instance setting
- SonarrInstance__Url=https://sonarr.mydomain.tld
- SonarrInstance__ApiKey=YOUR-SONARR-API-KEY
```
These setting are used to talk to your Sonarr instance. 

The `SonarrInstance__Url` setting tells the Sonarr bridge where your Sonarr instance can be found. This setting is typically what you type in your browser to reach your Sonarr instance.

The `SonarrInstance__ApiKey` is used to authenticate against the API of your Sonarr instance. You can get this from `https://sonarr.mydomain.tld/settings/general`


### AutoImport
```yml
# This is for automatically importing your own lists from your listrr.pro V2 account
- listrr__AutoImport__ImportLists=true
- listrr__AutoImport__ApiKey=YOUR-LISTRR-PRO-V2-API-KEY
- listrr__AutoImport__QualityProfileId=1
- listrr__AutoImport__RootFolderId=1
- listrr__AutoImport__LanguageProfileId=1
- listrr__AutoImport__Monitored=true
- listrr__AutoImport__SearchForMissingEpisodes=true
- listrr__AutoImport__SearchForCutoffUnmetEpisodes=true
- listrr__AutoImport__SeasonFolder=true
- listrr__AutoImport__Tags__0=1
- listrr__AutoImport__Tags__1=5
```
These settings are important, if you want to import ALL Show lists from your listrr.pro account.

`listrr__AutoImport__ImportLists` is the setting you use to enable (`true`) or disable (`false`) the automatic import of ALL lists into your Sonarr instance.

`listrr__AutoImport__ApiKey` is used to authenticate against the listrr.pro API. That way the listrr.pro API knows which account requests stuff.

`listrr__AutoImport__QualityProfileId` is used to set everything that is imported to a specific Quality Profile.

`listrr__AutoImport__RootFolderId` is used to set everything that is imported to a specific Root folder.

`listrr__AutoImport__LanguageProfileId` is used to set everything that is imported to a specific Language profile.

`listrr__AutoImport__Monitored` is used to tell your Sonarr instance if a show gets added as monitored (`true`) or unmonitored (`false`).

`listrr__AutoImport__SearchForMissingEpisodes` is used to tell if your Sonarr instance should search (`true`) for episodes when the Sonarr bridge adds a show or not (`false`).

`listrr__AutoImport__SearchForCutoffUnmetEpisodes` is used to tell your Sonarr instance to search for Cutoff unmet (`true`) or not (`false`).

`listrr__AutoImport__SeasonFolder` is used to tell your Sonarr instance to create a folder for each season (`true`) or not (`false`).

`listrr__AutoImport__Tags__0` is used to add Tags to a show when adding it to your Sonarr instance. Be aware to bump the number for each Tag you add. 

### Import a list by ID
```yml
# This is for importing listrr.pro V2 lists by their Ids
- listrr__Lists__0__Id=A-LISTRR-V2-LIST-ID
- listrr__Lists__0__QualityProfileId=1
- listrr__Lists__0__RootFolderId=1
- listrr__Lists__0__LanguageProfileId=1
- listrr__Lists__0__Monitored=true
- listrr__Lists__0__SearchForMissingEpisodes=true
- listrr__Lists__0__SearchForCutoffUnmetEpisodes=true
- listrr__Lists__0__SeasonFolders=true
- listrr__Lists__0__Tags__0=1
- listrr__Lists__0__Tags__1=35
- listrr__Lists__0__Tags__2=50
```
This will allow you to import a single list by the ID you get from listrr.pro. You can take a look for existing lists at [https://listrr.pro/Home/Lists](https://listrr.pro/Home/Lists){:target="_blank"}. Hit the share button to copy the ID of a list.

For each list, you have to bump the number `Lists__0__`. So if you have 2 lists, you start with `Lists__0__` for the first list, and `Lists__1__` for your second list, and so on.

`listrr__Lists__0__Id` is used to tell the Sonarr bridge the ID of your list. For example: `6374d7332d52d9b21fd91f86`

`listrr__Lists__0__QualityProfileId` is used to set everything that is imported to a specific Quality Profile.

`listrr__Lists__0__RootFolderId` is used to set everything that is imported to a specific Root folder.

`listrr__Lists__0__LanguageProfileId` is used to set everything that is imported to a specific Language profile.

`listrr__Lists__0__Monitored` is used to tell your Sonarr instance if a show gets added as monitored (`true`) or unmonitored (`false`).

`listrr__Lists__0__SearchForMissingEpisodes` is used to tell if your Sonarr instance should search (`true`) for episodes when the Sonarr bridge adds a show or not (`false`).

`listrr__Lists__0__SearchForCutoffUnmetEpisodes` is used to tell your Sonarr instance to search for Cutoff unmet (`true`) or not (`false`).

`listrr__Lists__0__SeasonFolders` is used to tell your Sonarr instance to create a folder for each season (`true`) or not (`false`).

`listrr__Lists__0__Tags__0` is used to add Tags to a show when adding it to your Sonarr instance. Be aware to bump the number for each Tag you add.







## How to run your Sonarr Bridge ?

### First Run
Copy the content of the example `docker-compose.yml` and save it in the directory you created earlier.

Set your Sonarr Instance settings, and your listrr.pro API key. Save the file.

In the directory where the `docker-compose.yml` file is saved, execute `docker-compose up`. Sonarr Bridge will now get all you need from your Sonarr instance to set `QualityProfileId`, `RootFolderId`, `LanguageProfileId`, and `Tags`.

There should be an output similar to this:
```
LOG: Connecting to Sonarr: https://sonarr.mydomain.tld with API Key: 'MY-SONARR-API-KEY'
INFO: Found QualityProfile 1:1080p
INFO: Found RootFolder 5:/mnt/unionfs/Media/TV
INFO: Found LanguageProfile 1:English
```

You can see the lines `INFO: Found QualityProfile 1:1080p` where the the left part of `1:1080p` is the Id, and the right part is the name of the quality profile of your sonarr instance. This will be the same for `RootFolderId`, `LanguageProfileId`, and `Tags`.

Hit CTRL+C on your keyboard to stop the Sonarr Bridge. Edit your `docker-compose.yml` to add the `QualityProfileId`, `RootFolderId`, `LanguageProfileId`, and `Tags` for your lists or AutoImport.

Execute `docker-compose up`. Your Sonarr Bridge should now run.