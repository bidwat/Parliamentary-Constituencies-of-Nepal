# Parliamentary Constituencies of Nepal

The full list of parliamentary constituencies of Nepal in a single JSON file. The contents was scraped and formatted form the wikipedia page for (parliamentary constituencies)[https://en.wikipedia.org/wiki/List_of_parliamentary_constituencies_of_Nepal] and the children pages of individual constituencies.

The repository only contains the following file:

- `nepal_election_constituencies_area.json`

## What the file contains

The JSON is an array of district objects.

Each district has:

- `district` (string)
- `constituencies` (array)

Each constituency has:

- `name` (string)
- `population` (integer electorate)
- `municipalities` (array)
  - each municipality has `name`
  - optional `wards` array when only specific wards belong to that constituency

### Notes

- If `municipalities` is empty, that constituency covers the whole district.
- A municipality can appear in multiple constituencies with different `wards`.

## Quick example

```json
{
  "district": "Ilam",
  "constituencies": [
    {
      "name": "Ilam 1",
      "population": 109535,
      "municipalities": [
        { "name": "Sandakpur Rural Municipality" },
        { "name": "Ilam Municipality", "wards": [10, 13, 14] }
      ]
    }
  ]
}
```
