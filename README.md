# github-graphql-workshop
For MLH Prime: Europe Regional

## Examples


### Query for your own name:
```graphql
query {
  viewer {
    login
  }
}
```

### Query for facebook/react issues and their labels

```graphql
query {
  repository(owner:"facebook", name: "react") {
    issues(first: 20) {
      edges {
        node {
          title
          labels(first: 100) {
            edges {
              node {
                name
              }
            }
          }
        }
      }
    }
  }
}
```
