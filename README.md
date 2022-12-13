# Book Store Services

- A Book Store Management System, CRUD APIs built using GoLang.
- Used GORM and Gorilla Mux libraries for ORM and routing.
- Used MySql as the database


## Tech Stack

- `Backend Framework:` `GoLang`
- `Databases:` `MySQL`
- `Libraries` `Gorilla Mux, GORM`



## Schema
|    books     |  |  
| -------- | ------- |
|   `id`      | `token` |
|   `created_at`      | `DATE TIME` |
|   `updated_at`      | `DATE TIME` |
|   `deleted_at`      | `DATE TIME` |
|   `name`      | `VARCHAR(255)` |
|   `author`      | `VARCHAR(255)` |
|   `publication`      | `VARCHAR(255)` |




## API Reference 

### API Endpoints


#### Get Available Books
```javascript
  GET http://localhost:8080/book
```
#### Example Response
```javascript
  200 OK

```

```json 
[
    {
        "ID": 1,
        "CreatedAt": "2022-12-13T02:41:31+05:30",
        "UpdatedAt": "2022-12-13T02:41:31+05:30",
        "DeletedAt": null,
        "name": "Harry Potter",
        "author": "J. K. Rowling",
        "publication": "Bloomsbury"
    },
    {
        "ID": 2,
        "CreatedAt": "2022-12-13T15:07:16+05:30",
        "UpdatedAt": "2022-12-13T15:07:16+05:30",
        "DeletedAt": null,
        "name": "THE GREAT GATSBY",
        "author": "F. Scott Fitzgerald",
        "publication": "Charles Scribner's Sons"
    },
    {
        "ID": 3,
        "CreatedAt": "2022-12-13T15:13:45+05:30",
        "UpdatedAt": "2022-12-13T15:13:45+05:30",
        "DeletedAt": null,
        "name": "A PORTRAIT OF THE ARTIST AS A YOUNG MAN",
        "author": "James Joyce",
        "publication": "B W Huebsch"
    },
    {
        "ID": 4,
        "CreatedAt": "2022-12-13T15:16:28+05:30",
        "UpdatedAt": "2022-12-13T15:16:28+05:30",
        "DeletedAt": null,
        "name": "THE GRAPES OF WRATH",
        "author": "John Steinbeck",
        "publication": "The Viking Press-James Lloyd"
    },
    {
        "ID": 5,
        "CreatedAt": "2022-12-13T15:17:36+05:30",
        "UpdatedAt": "2022-12-13T15:17:36+05:30",
        "DeletedAt": null,
        "name": "TO THE LIGHTHOUSE",
        "author": "Virginia Woolf",
        "publication": "Hogarth Press"
    },
    {
        "ID": 6,
        "CreatedAt": "2022-12-13T15:18:17+05:30",
        "UpdatedAt": "2022-12-13T15:18:17+05:30",
        "DeletedAt": null,
        "name": "THE HEART IS A LONELY HUNTER",
        "author": "Carson McCullers",
        "publication": "Houghton Mifflin"
    }
]
```

#### Add Book
```javascript
  POST http://localhost:8080/book
```
```json 
{
    "name":"THE GREAT GATSBY",
    "author":"F. Scott Fitzgerald",
    "publication":"Charles Scribner's Sons"
}
```
#### Example Response
```javascript
  201 CREATED
```
```json 
{
    "ID": 2,
    "CreatedAt": "2022-12-13T15:07:15.70465+05:30",
    "UpdatedAt": "2022-12-13T15:07:15.70465+05:30",
    "DeletedAt": null,
    "name": "THE GREAT GATSBY",
    "author": "F. Scott Fitzgerald",
    "publication": "Charles Scribner's Sons"
}
```

#### Get Book By Id


```javascript
  GET http://localhost:8080/book/4
```
#### Example Response

```javascript
  200 OK
```

```json 
{
    "ID": 4,
    "CreatedAt": "2022-12-13T15:16:28+05:30",
    "UpdatedAt": "2022-12-13T15:16:28+05:30",
    "DeletedAt": null,
    "name": "THE GRAPES OF WRATH",
    "author": "John Steinbeck",
    "publication": "The Viking Press-James Lloyd"
}
```

#### Update Book Details
```javascript
  PUT http://localhost:8080/book/4
```

```json 
{
    "name": "the grapes of wrath",
    "author": "john Steinbeck",
    "publication": "the viking press-james lloyd"
}
```
#### Example Response
```javascript
  200 OK
```
```json
{
    "ID": 4,
    "CreatedAt": "2022-12-13T15:16:28+05:30",
    "UpdatedAt": "2022-12-13T15:34:08.2978858+05:30",
    "DeletedAt": null,
    "name": "the grapes of wrath",
    "author": "john Steinbeck",
    "publication": "the viking press-james lloyd"
}
```


#### Delete Book By Id

```javascript
  DELETE http://localhost:8080/book/4
```
#### Example Response

```javascript
  204 NO CONTENT
```

```json 
{
    "ID": 0,
    "CreatedAt": "0001-01-01T00:00:00Z",
    "UpdatedAt": "0001-01-01T00:00:00Z",
    "DeletedAt": null,
    "name": "",
    "author": "",
    "publication": ""
}
```
