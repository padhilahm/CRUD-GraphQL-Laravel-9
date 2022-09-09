Method POST
http://localhost:8000/graphql

Pakai Postman, tab Body GraphQL


QUERY

Get semua data movies
{
  movies {
	id,
	title,
	director
  }
}

Get berdasarkan ID
{
  movie(id: 4) {
	title,
	director
  }
}

Create data movie
mutation createMovie {
createMovie(
    title: "Gone Girl", 
    director: "David Fincher", 
    language: "English", 
    year_released: "2014") 
	{
        id
	    title
	    director
	}
}

Update data movie
mutation updateMovie {
mutation updateMovie {
updateMovie(
  id: 2, 
  title: "Stand by Me", 
  director: "Rob Reiner", 
  language: "English", 
  year_released: "1986") 
  {
 	id
	title
	director
  }
}

Delete data movie
mutation deleteMovie {
deleteMovie(
    id: 2
  )
}
