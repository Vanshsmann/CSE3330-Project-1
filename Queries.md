2. Enter a city name and retrieve all the movies that are released within that particular city.
- SELECT " Movie_title" FROM Movies, City, Screening, Cinema WHERE " City_name" = 'Arlington' and " Cinema_id" = "Cinema_id" and Movies."Movie_id" = Screening."Movie_id" and City_id = " City_id";
3. List all cinemas that are showing a particular movie.
- SELECT " Cinema_name" FROM Cinema, Movies, BookTicket WHERE " Movie_title" = 'Vertigo' and Movies.Movie_id = BookTicket.Movie_id and Cinema.Cinema_id = BookTicket.Cinema_id;
4. List the seats that are booked in all cinemas for a particular movie.
- SELECT SeatNum FROM BookTicket, Movies WHERE BookTicket.Movie_id = (SELECT Movie_id FROM Movies WHERE " Movie_title" = 'Vertigo');

5. Given a specific cinema and movie list the showing times for that movie.

6.(UPDATED) Given a cinema name list movie title and seat numbers that are reserved.

7. Given a reservation# list the cinema, movie session, and time where seats were booked.
8. List the movies with their corresponding time, city, and cinema name.
9.(UPDATED) Given a cinema name list movie title and seat numbers that are reserved.


