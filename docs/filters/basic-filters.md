---
hide:
  - navigation
  - toc
---

# Basic filters

Basic filters are for users that either want to quickly create a list, or simply dont want to wrap their head around the way more complex variant [Extensive-Filters](/filters/extensive-filters).

## Limitations
Although Basic filters are a lot easier to create lists, they have some limitations.

### Logical connection on field level

All values of a field are connected via the `AND` operator. So when you select the Genres `Action` and `Adventure`, only Movies/Shows that have `Action` AND `Adventure` set as genre will match your list.

If you select `Netflix`, `Amazon`, `HBO+`, `Disney+` for the `Streaming Service - Flatrate` field, your list will result in items that will be available ONLY on all the selected plattforms. If there are items that are exclusive to one plattform, they wont be included.

### Logical connection on list level

All fields are connected via the `AND` operator. For example: You select `Robert Downey Jr.` for the field `Actor`, and `James Cameron` for the field `Director`.

The result would be a list where `Robert Downey Jr.` will be one of the actors, `AND` one of the directors is `James Cameron`.