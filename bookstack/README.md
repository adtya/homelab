1. Generate a db password
```
head /dev/urandom | LC_ALL=C tr -dc 'A-Za-z0-9' | head -c 32 > .db_password
```
2. Set the url at which bookstack will be hosted on, eg. https://example.com in the file `.app_url`.
`printf "https://example.com" > .app_url` should do the trick.

Since both these files are loaded as docker secrets, they should not contain the trailing new line character. The command above to generate the password, and the printf command should make sure it's like that. But if you create the files manually from a text editor or by any other means, make sure the new line character is not present.
