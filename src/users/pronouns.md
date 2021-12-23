# Pronouns

A user may optionally set their set of preferred pronouns.

Some caveats to note:
* Bots cannot set their pronouns: they will always be `None`
* Custom pronouns are not supported: you must use Other/Ask for those.

## In Requests
You must use the integer ID when sending a pronoun to the API.

You will always receive the ID as an integer from the API.

Keep in mind the pronoun field can be null.

## Enum Variants
| Code Representation | Integer ID | English name    |
|---------------------|------------|-----------------|
| HeHim               | 0          | he/him          |
| HeIt                | 1          | he/it           | 
| HeShe               | 2          | he/she          |
| HeThey              | 3          | he/they         |
| ItHim               | 4          | it/him          |
| ItIts               | 5          | it/its          |
| ItShe               | 6          | it/she          |
| ItThey              | 7          | it/they         |
| SheHe               | 8          | she/he          |
| SheHer              | 9          | she/her         |
| SheIt               | 10         | she/it          |
| SheThey             | 11         | she/they        |
| TheyHe              | 12         | they/he         |
| TheyIt              | 13         | they/it         |
| TheyShe             | 14         | they/she        |
| TheyThem            | 15         | they/them       |
| Any                 | 16         | any of above    |
| OtherAsk            | 17         | ask this person |
| Avoid               | 18         | use name        |
