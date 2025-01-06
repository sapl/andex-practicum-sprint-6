# Задание 5. Проектирование GraphQL API

Пример запроса имени и паспорта:

```graphql
query GetClientNameAndPassport($id: String!) {
  client(id: $id) {
    name
  }
  clientDocuments(id: $id, type: "passport") {
    type
    number
  }
}
```

Пример запроса всех данных:

```graphql
query GetAllClientData($id: String!) {
  client(id: $id) {
    id
    name
    age
  }
  clientDocuments(id: $id) {
    id
    type
    number
    issueDate
    expiryDate
  }
  clientRelatives(id: $id) {
    id
    relationType
    name
    age
  }
}
```