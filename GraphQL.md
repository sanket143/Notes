# GraphQL - Ask for what you need, get exactly that

### **Abstract**

The primary objective of the paper is to provide an analysis of GraphQL, a novel query language for
implementing Web-based APIs. Proposed by Facebook in 2016, the language represents an alternative to
popular REST-based APIs, shifting from servers to clients the decision on the precise data returned by
API calls. The paper inculcates study about the two key characteristics of GraphQL: (a) support to the
nonhierarchical data model, which can contribute to reducing the number of endpoints accessed by clients;
(b) support to client-specific queries, i.e. queries where clients only ask for the precise data they need
to perform a given task.

### **Key features of GraphQL**
- Schemas and Types
- Single Endpoiint
- Subscriptions

### **Architecture and Design**

**1. Schemas and Types**

We define GraphQL schema based on what kind of query we can encounter. GraphQL schema also support types
which we had to specify for each field.

### **Example for GraphQL**

```graphql
type User {
  uid: String!
  posts: [Post!]!
}

type Post {
  text: String!
}
```


### **GraphQL is the better REST**

