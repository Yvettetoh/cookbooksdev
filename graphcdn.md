# GraphCDN

## Links

- [Main Website](https://graphcdn.io/)

<!--
```sh
#
npx graphcdn push

#
cat << EOF > ./graphcdn.yml
name: devparty
originUrl: 'https://example.com/api/graphql'
scopes:
  AUTHENTICATED: 'cookie:devparty_session|header:authorization'
rules:
- types:
    Query:
    - logs
    - post
    - user
    - stats
    - topic
    - users
    - badges
    - product
    - homeFeed
    - products
    - sessions
    - community
    - exploreFeed
    - searchUsers
    - whoToFollow
    - searchTopics
    - featuredUsers
    - waitlistCount
    - featuredTopics
    - suggestedUsers
    - morePostsByUser
  maxAge: 900
  swr: 900
  scope: AUTHENTICATED
  description: Cache Frequent queries
schema: 'https://example.com/api/graphql'
passThroughOnly: false
rootTypeNames:
  query: Query
  mutation: Mutation
EOF
```
-->
