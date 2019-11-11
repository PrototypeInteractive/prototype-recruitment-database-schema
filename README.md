# Recruitment Test Exercise

## Overview
This repository contains the MongoDB schema for the recruitment test excercise.

## Schema
Database consists of 7 collections and their respective fields:
- `films`
  - `id` - number
  - `characters` - an array of numbers (references `people` collection)
  - `created` - string
  - `director` - string
  - `edited` - string
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
  - `created` - string
  - `edited` - string
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
  - `created` - string
  - `diameter` - string
  - `edited` - string
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
  - `created` - string
  - `designation` - string
  - `edited` - string
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
  - `created` - string
  - `crew` - string
  - `edited` - string
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
