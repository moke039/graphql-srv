https://graphql.org/code/

graphql + express を使ったサーバ  
https://graphql.org/graphql-js/  
"express": "^4.18.2",  
"express-graphql": "^0.12.0",  
npm i でバージョンエラーが出るのを --force で無理やり入れてみた。

```
npm run nonapollo
```

サーバ起動ログの url にアクセスすると GraphiQL が開く

```
{hello}
```

```
curl -X POST \
-H "Content-Type: application/json" \
-d '{"query": "{ hello }"}' \
http://localhost:4000/graphql
```

apollo-server  
https://www.apollographql.com/docs/apollo-server/getting-started  
構築して比較してみる。

```
npm start
```

サーバ起動ログの url にアクセスすると Apollo Sandbox が開く

```
query GetBooks {
  books {
    title
    author
  }
}
```

```
curl -X POST \
-H "Content-Type: application/json" \
-d '{"query": "query GetBooks { books\n { title\n author\n } }"}' \
http://localhost:4000/graphql
```
