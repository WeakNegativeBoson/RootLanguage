```
# pinned repos
# https://dev.to/thomasaudo/get-started-with-github-grapql-api--1g8b
echo -e "\n$hr\nPINNED  REPOSITORIES\n$hr"
AUTH="Authorization: bearer $JEKYLL_GITHUB_TOKEN"
curl -L -X POST "${GITHUB_GRAPHQL_URL}" -H "$AUTH" \
--data-raw '{"query":"{\n  user(login: \"'${GITHUB_REPOSITORY_OWNER}'\") {\n pinnedItems(first: 6, types: REPOSITORY) {\n nodes {\n ... on Repository {\n name\n }\n }\n }\n }\n}"'

```

[![default](https://user-images.githubusercontent.com/8466209/200241752-e70d2eeb-5885-4f99-9362-4a05aeeb4435.png)](https://dev.to/thomasaudo/get-started-with-github-grapql-api--1g8b)

![default](https://user-images.githubusercontent.com/8466209/200250136-7fe7a768-08a5-4bfb-ad19-c2a93cda363b.png)
