# iGameDeployable
all deployable features; branch for updates

## CONFIG VARS:
1. FOR [IGDB](https://api-docs.igdb.com) API connection:
- ***CLIENT_ID***
- ***CLIENT_SECRET***
2. FOR DEPLOYMENT:
- ***DATABASE_URL*** to connect to app's database
- ***FLASK_APP*** for entry into the application "factory"
- ***FLASK_CONFIG*** to select execution configuration, eg, Heroku
- ***REDIS_TLS_URL*** memoizing functions
- ***REDIS_URL*** memoizing functions
- ***SECRET_KEY*** Flask requirement for data security
- ***SALT*** for user password security

## includes
- registration
- login
- initial preferences:
  1. based on 3 likes
    - generates platform list from likes
  2. based on 2 dislikes
  3. similar games to likes
  4. similar games to likes SUBTRACTING games that contain attributes found ONLY in dislikes
  4. uses set operations on set:int for game attr (genre ID, theme ID, keyword ID)
  5. SUBTRACTING from recommendations if not in platform list

### NOTES
- this branch is read-only; create a new branch for updates

### BUGS
- todo
