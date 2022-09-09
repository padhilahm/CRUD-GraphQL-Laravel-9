### Method POST
http://localhost:8000/graphql

Pakai Postman, tab Body GraphQL

### QUERY

#### Get semua data movies
```graphql
{
  movies {
	id,
	title
  }
}
```

#### Get berdasarkan ID
```graphql
{
  movie(id: 1) {
	title,
	director
  }
}
```

#### Create data movie
```graphql
mutation createMovie {
createMovie(
    title: "Spider-Man: No Way Home", 
    director: "Jon Watts", 
    language: "English", 
    year_released: "2021") 
	{
        id
	    title
	}
}
```

#### Update data movie
```graphql
mutation updateMovie {
updateMovie(
  id: 1, 
  title: "Thor: Love and Thunder", 
  director: "Taika Waititi", 
  language: "English", 
  year_released: "2022") 
  {
 	id
	title
  }
}
```

#### Delete data movie
```graphql
mutation deleteMovie {
deleteMovie(
    id: 2
  )
}
```
