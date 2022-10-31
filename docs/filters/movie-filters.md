# Movie filters

## Basic filters

| Filter name       | Type     | Description                                                 |
|-------------------|----------|-------------------------------------------------------------|
| Budget            | integer  | How much budget the movie had for production                |
| Collection - Name | string   | The name of the collection a movie belongs to               |
| Genre - Name      | genre    | The genre of a movie                                        |
| Homepage          | string   | The homepage of the movie                                   |
| IsAdult           | bool     | If the movie is flagged as xxx content                      |
| IsAnime           | bool     | If the movie is flagged as anime content                    |
| Keyword - Name    | string   | A keyword the movie belongs to                              |
| Original Language | language | The original language a movie was shot                      |
| Original Title    | string   | The original title in the country the movie was released in |
| Overview          | string   | A short overview about the movie                            |
| Popularity        | decimal  | The popularity of the movie                                 |
| Release date      | date     | The exact release date of the movie                         |
| Revenue           | integer  | The revenue a movie made                                    |
| Runtime           | integer  | The runtime of a movie in minutes                           |
| Status            | status   | The release state of a movie                                |
| Tagline           | string   | The tagline of the movie                                    |
| Title             | string   | The title of the movie                                      |
| Video             | bool     | If the movie is only a video instead of a full movie        |


## Actor

| Filter name            | Type    | Description                              |
|------------------------|---------|------------------------------------------|
| Actor - Character name | string  | The name of the character an actor plays |
| Actor - Gender         | gender  | The gender of the actor                  |
| Actor - Name           | string  | The name of the actor                    |
| Actor - Populatity     | decimal | The popularity of the actor. Between 0-10|


## Alternative Title

| Filter name                 | Type    | Description                                                     |
|-----------------------------|---------|-----------------------------------------------------------------|
| Alternative Title - Country | country | The country where the alternative title is used                 |
| Alternative Title - Title   | string  | The alternative title for a movie                               |
| Alternative Title - Type    | string  | The type of title (e.g. working title, DVD title, modern title) |


## Crew

| Filter name       | Type    | Description                                        |
|-------------------|---------|----------------------------------------------------|
| Crew - Department | string  | The department in which the crew member has worked |
| Crew - Gender     | gender  | The gender of the crew member                      |
| Crew - Job        | string  | The job of the crew member                         |
| Crew - Name       | string  | The name of the crew member                        |
| Crew - Popularity | decimal | The popularity of the crew member                  |

## External Id

| Filter name             | Type   | Description                             |
|-------------------------|--------|-----------------------------------------|
| External Id - Facebook  | string | The facebook page handle                |
| External Id - Twitter   | string | The twitter handle                      |
| External Id - Instagram | string | The instagram handle                    |
| External Id - IMDb      | string | The id from https://www.imdb.com/       |
| External Id - TMDb      | string | The id from https://www.themoviedb.org/ |
| External Id - TvRage    | string | The id from https://www.tvrage.com/     |
| External Id - Trakt     | string | The id from https://trakt.tv/           |


## Production Company

| Filter name                  | Type    | Description                                     |
|------------------------------|---------|-------------------------------------------------|
| Production Company - Country | country | The country where a production company is based |
| Production Company - Name    | string  | The name of the production company              |


## Production Country

| Filter name                  | Type    | Description                                          |
|------------------------------|---------|------------------------------------------------------|
| Production Country - Country | country | The country where the movie was produced             |
| Production Country - Name    | string  | The name of the country where the movie was produced |


## Ratings

| Filter name                  | Type    | Description                                             |
|------------------------------|---------|---------------------------------------------------------|
| Ratings - IMDb average       | decimal | The average of all votes on https://imdb.com/           |
| Ratings - IMDb votes         | integer | The amount of votes on https://imdb.com/                |
| Ratings - TMDb average       | decimal | The average of all votes on https://www.themoviedb.org/ |
| Ratings - TMDb votes         | integer | The amount of votes on https://www.themoviedb.org/      |
| Ratings - Trakt average      | decimal | The average of all votes on https://trakt.tv/           |
| Ratings - Trakt votes        | integer | The amount of votes on https://trakt.tv/                |
| Ratings - Metacritic average | decimal | The average of all votes on https://www.metacritic.com/ |
| Ratings - Rotten average     | decimal | The amount of votes on https://www.rottentomatoes.com/  |

## Release

| Filter name             | Type          | Description                               |
|-------------------------|---------------|-------------------------------------------|
| Release - Certification | certification | The certification of the release          |
| Release - Country       | country       | The country of the release                |
| Release - Primary       | bool          | Flag if this release is a primary release |


## Release Date

| Filter name                  | Type          | Description                               |
|------------------------------|---------------|-------------------------------------------|
| Release Date - Certification | certification | The certification for the release date    |
| Release Date - Country       | country       | The country for the release date          |
| Release Date - Language      | language      | The language for the release date         |
| Release Date - Note          | string        | A note that has been added to the release |
| Release Date - Type          | releaseType   | The type of release for a release date    |

## Spoken language

| Filter name                | Type     | Description                        |
|----------------------------|----------|------------------------------------|
| Spoken Language - Language | language | Indicates in what dubs a movie has |
| Spoken Language - Name     | country  | The name of the language           |

## Streaming Service

| Filter name                         | Type              | Description                                                                                   |
|-------------------------------------|-------------------|-----------------------------------------------------------------------------------------------|
| Streaming Service - Ads - Name      | streaming service | The name of the streaming service where a movie could be watched with ads                     |
| Streaming Service - Buy - Name      | streaming service | The name of the streaming service where a movie could be bought                               |
| Streaming Service - Flatrate - Name | streaming service | The name of the streaming service where a movie is included the mothly fee without extra cost |
| Streaming Service - Free - Name     | streaming service | The name of the streaming service where a movie could be watched for free                     |
| Streaming Service - Rent - Name     | streaming service | The name of the streaming service where a movie could be rented                               |
| Streaming Service - Country         | country           | The country a movie is available for a streaming service                                      |

## Translation

| Filter name            | Type     | Description                                              |
|------------------------|----------|----------------------------------------------------------|
| Translation - Country  | country  | The country a movie has been translated for              |
| Translation - Language | language | The language a movie has been translated for             |
| Translation - Name     | name     | The name of the language a movie has been translated for |