# graphql-typescript-cheatsheet

Resources for End-to-End typing with GraphQL and TypeScript

## Notes

There is something informally called the "keying-in" operator that is very handy for accessing generated TypeScript types from your GraphQL schema.

```ts
// generated typescript response from schema
type APIResponse = {
  user: {
    userId: string
    friendList: {
      count: number
    }
  }
}
you need to the type of APIResponse.user.friendList but don't know it upfront
type FriendList = APIResponse['user']['friendList']
```

It looks kinda obvious but can be really handy.

## Libraries

- typegraphql: https://github.com/19majkel94/type-graphql/ Create GraphQL schema and resolvers with TypeScript, using classes and decorators! [now at 1.0](https://dev.to/michallytek/announcing-typegraphql-1-0-1d7h)
- `graphql-code-generator`: https://github.com/dotansimha/graphql-code-generator ([Usage example](https://formidable.com/blog/2019/strong-typing/))
- graphql nexus
- smalller libs
  - https://github.com/capaj/decapi
  - https://github.com/prismake/typegql

## Podcasts

- Natalie Qabazard on the [Real Talk JS Podcast on GraphQL + Typescript](https://realtalkjavascript.simplecast.fm/42ba5d10) adoption at Zillow
