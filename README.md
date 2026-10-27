# meal-planner-data

Data store for Steven's Weekly Meal Planner.

## plans.json

The public view-only planner page reads `plans.json` from this repo on load and on Refresh:
`https://raw.githubusercontent.com/steven-steven/meal-planner-data/main/plans.json`

Structure:

- `version`: schema version (currently 1)
- `updatedAt`: ISO timestamp of the last update
- `plans`: array of meal plans, each with:
  - `id`, `date` (YYYY-MM-DD), `mealType` (`breakfast` | `lunch` | `dinner`)
  - `title`, `description`, `notes`
  - `prepMinutes`, `cookMinutes`, `servings` (numbers or null)
  - `ingredients`: array of strings
  - `instructions`: array of step strings

This repo is public so the planner page can read it without a login. Public means anyone with the link can view the plans — no one can change them without write access to this repo.
