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

### Mutation: Add reaction

```graphql
mutation {
  addReaction(input: {
    subjectId: "MDExOlB1bGxSZXF1ZXN0OTE3NTkxMTE=",
    content: THUMBS_UP
  }) {
    reaction {
      content
      id
    }
  }
}
```
