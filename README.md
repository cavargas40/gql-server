# Graphql Server

### Installation

The server requires node.js and npm installed in your system, then you can run

```sh
$ npm i
```

### Run Server

The simple server (actually just a hello world) you can make it run with the command
```sh
$ npm run server
```

A small example of courses is with the other server
```sh
$ npm run server2
```

then in your web browser just navigate to `http://localhost:4000/graphql` and you can start making querys.


### Make Querys

You can create querys in several ways here just some examples:

for the simple server:

```graphql
{
    message
}
```

for the courses example server

```graphql
{
  courses {
    id,
    title,
    author,
    description,
    topic,
    url
  }
}
```

for a specific query
```graphql
query getSingleCourse($courseID: Int!) {
    course(id: $courseID) {
        title
        author
        description
        topic
        url
    }
}
```

and in this case the query variables are:
```graphql
{
  "courseID": 1
}
```

This is based in https://medium.com/codingthesmartway-com-blog/creating-a-graphql-server-with-node-js-and-express-f6dddc5320e1

License
----

MIT
