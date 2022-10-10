1. Enter a city name and retrieve all the movies that are released within that particular city.
- SELECT " Movie_title" FROM Movies, City, Screening, Cinema WHERE " City_name" = 'Arlington' and " Cinema_id" = "Cinema_id" and Movies."Movie_id" = Screening."Movie_id" and City_id = " City_id";
2. List all cinemas that are showing a particular movie.
- SELECT " Cinema_name" FROM Cinema, Screening WHERE Screening.Movie_id = 3 and Cinema_id = " Cinema_id"
3. List the seats that are booked in all cinemas for a particular movie.
- SELECT SeatNum FROM BookTicket WHERE BookTicket.Movie_id = 3;




6. Given a movie and session time how many seats are available.  SELECT “Movie_id” FROM Movies, Screening,BookTicket WHERE “Movie_id” = “Gladiator” and Screen_time = “4 pm - 6 pm”
