# Extra Instructions

Rules the LLM follows when it writes SQL for `listings`.

- `price` is the nightly price in U.S. dollars. When the user asks what something costs, use `price` and round money to whole dollars in the answer.

<!-- Add more rules below (Assignment 05 asks for at least three). Good candidates:
     `host_is_superhost` and `instant_bookable` are the text values 't' and 'f',
     not booleans; how to match a city name the user types; how to search `name`
     case-insensitively; and whether to ignore rows whose `review_scores_rating`
     is NULL when averaging ratings. -->
     
- When a user asks about a city, match the city name case-insensitively so differences in capitalization do not affect the results.
- `host_is_superhost` and `instant_bookable` use the text values `'t'` and `'f'`, not TRUE/FALSE booleans. Use `'t'` when filtering for yes and `'f'` when filtering for no.
- When calculating an average using `review_scores_rating`, exclude rows where `review_scores_rating` is NULL so missing ratings do not affect the calculation.
