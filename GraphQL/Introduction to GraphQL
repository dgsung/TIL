# Introduction to GraphQL
> 출처 [Velopert님의 글](https://velopert.com/2318)와 Ben Award의 유튜브([GraphQL vs REST for Side Projects](https://www.youtube.com/watch?v=AYZOHt6kz6Y)를 보고 정리한 내용입니다.

## 소개
GraphQL 은 페이스북에서 만든 어플리케이션 레이어 쿼리 언어다.
이 GraphQL 기술은, 특정 언어에 제한된것이 아니여서, Node.js, Ruby, PHP, Python, Golang, 등 여러 환경에서 사용 할 수 있다. 심지어, HTTP 프로토콜에 제한되어있지도 않아서, WebSocket 이나 MQTT 프로토콜 위에서 사용 할 수도 있다. 데이터베이스도 어떤 데이터베이스를 사용하던 상관없다.

## 개요
GraphQL API은 다음의 main building blocks으로 구성 된다: the **schema, queries, and resolvers.**

### Operation
GraphQL operations always start at **the query, mutation, or subscription type** in your schema, but **fragments** can be used in any selection set.
#### Query
![](https://i.imgur.com/rAdwxjW.png)
![](https://miro.medium.com/max/1876/1*yI_ZuOy0-22q6pdgVlytCA.png)
#### Mutation
side effect가 있는 버전의 Query.
#### Subscription
Subscriptions allow GraphQL clients to observe specific events and receive updates from the server when those events occur. 
#### Fragments
Fragments let you construct sets of fields, and then include them in queries where you need to.

### Schema
The most basic components of a GraphQL schema are object types, which just represent a kind of object you can fetch from your service, and what fields it has.
```
type Character {
  name: String!
  appearsIn: [Episode!]!
}
```
## GraphQL vs REST
GraphQL의 핵심은, 리소스를 url이 아니라 Query를 통해 표현하는 것이다. GraphQL은 단일 엔드포인트를 권장하고 있었다. 모든 요청을 `/graphql` 한 곳에서 처리.
**Advantages**
* No over/under fetching
    * able to specify data
* Don't have to version an api
    * eg) adding field to query doesn't affect old version's code
    * for API it needs different version:
        * api.example.com/v1/posts
        * api.example.com/v2/posts
* It's a type system
    * catches silly errors
    * self documenting
    * tooling
