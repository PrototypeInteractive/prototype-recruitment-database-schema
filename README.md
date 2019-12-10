# Recruitment Test Exercise

## Overview
This repository contains the SQL Server schema for the recruitment test excercise.

## Schema
Database consists of tables and their respective fields:
- `films`
  - `id` - number
  - `characters` - an array of numbers (references `people` collection)
  - `created` - datetime
  - `director` - string
  - `edited` - datetime
  - `episode_id` - number
  - `opening_crawl` - string
  - `planets` - an array of numbers (references `planets` collection)
  - `producer` - string
  - `release_date` - string
  - `species` - an array of numbers (references `species` collection)
  - `starships` - an array of numbers (references `starships` collection)
  - `title` - string
  - `vehicles` - an array of numbers (references `vehicles` collection)


- `people`
  - `id` - number
  - `birth_year` - string
  - `created` - datetime
  - `edited` - datetime
  - `eye_color` - string
  - `gender` - string
  - `hair_color` - string
  - `height` - string
  - `homeworld` - number (references `planets` collection)
  - `mass` - string
  - `name` - string
  - `skin_color` - string


- `planets`
  - `id` - number
  - `climate` - string
  - `created` - datetime
  - `diameter` - string
  - `edited` - datetime
  - `gravity` - string
  - `name` - string
  - `orbital_period` - string
  - `population` - string
  - `rotation_period` - string
  - `surface_water` - string
  - `terrain` - string


- `species`
  - `id` - number
  - `average_height` - string
  - `average_lifespan` - string
  - `classification` - string
  - `created` - datetime
  - `designation` - string
  - `edited` - datetime
  - `eye_colors` - string
  - `hair_colors` - string
  - `homeworld` - number (references `planets` collection)
  - `language` - string
  - `name` - string
  - `people` - an array of numbers (references `people` collection)
  - `skin_colors` - string


- `starships`
  - `id` - number
  - `MGLT` - string
  - `hyperdrive_rating` - string
  - `pilots` - an array of numbers (references `people` collection)
  - `starship_class` - string


- `transport`
  - `id` - number
  - `cargo_capacity` - string
  - `consumables` - string
  - `cost_in_credits` - string
  - `created` - datetime
  - `crew` - string
  - `edited` - datetime
  - `length` - string
  - `manufacturer` - string
  - `max_atmospering_speed` - string
  - `model` - string
  - `name` - string
  - `passengers` - string


- `vehicles`
  - `id` - number
  - `pilots` - an array of numbers (references `people` collection)
  - `vehicle_class` - string


- `films_characters`
  - `film_id` - number (reference to `films` table)
  - `people_id` - number (reference to `person` table)

- `films_planets`
  - `film_id` - number (reference to `films` table)
  - `planet_id` - number (reference to `planets` table)

- `films_species`
  - `film_id` - number (reference to `films` table)
  - `species_id` - number (reference to `species` table)

- `films_starships`
  - `film_id` - number (reference to `films` table)
  - `starship_id` - number (reference to `startship` table)

- `films_vehicles`
  - `film_id` - number (reference to `films` table)
  - `vehicle_id` - number (reference to `vehicles` table)

- `species_people`
  - `species_id` - number (reference to `species` table)
  - `people_id` - number (reference to `people` table)

- `starships_pilots`
  - `starship_id` - number (reference to `starships` table)
  - `people_id` - number (reference to `people` table)

- `vehicles_pilots`
  - `vehicle_id` - number (reference to `vehicles` table)
  - `people_id` - number (reference to `people` table)

