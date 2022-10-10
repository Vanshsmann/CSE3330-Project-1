1. Enter a city name and retrieve all the movies that are released within that particular city.
SELECT " Movie_title" FROM Movies, City, Screening, Cinema WHERE " City_name" = 'Arlington' and " Cinema_id" = "Cinema_id" and Movies."Movie_id" = Screening."Movie_id" and City_id = " City_id";
