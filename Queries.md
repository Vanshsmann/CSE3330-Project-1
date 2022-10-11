## 2. Enter a city name and retrieve all the movies that are released within that particular city.
SELECT " Movie_title" FROM Movies, City, Screening, Cinema WHERE " City_name" = 'Arlington' and " Cinema_id" = "Cinema_id" and Movies."Movie_id" = Screening."Movie_id" and City_id = " City_id";

## 3. List all cinemas that are showing a particular movie.
SELECT " Cinema_name" FROM Cinema, Movies, Screening WHERE Screening.Movie_id = (SELECT Movies.Movie_id WHERE " Movie_title" = 'Vertigo') and Cinema_id = " Cinema_id";

## 4. List the seats that are booked in all cinemas for a particular movie.
SELECT SeatNum FROM BookTicket, Movies WHERE BookTicket.Movie_id = (SELECT Movie_id FROM Movies WHERE " Movie_title" = 'Vertigo');

## 5. Given a specific cinema and movie list the showing times for that movie.
SELECT " Screen_time" FROM Cinema, Movies, Screening WHERE Screening.Movie_id = (SELECT Movies.Movie_id WHERE " Movie_title" = 'Vertigo') and " Cinema_id" = (SELECT Cinema_id WHERE " Cinema_name" = 'Cinemaprism');

## 6. (UPDATED) Given a cinema name list movie title and seat numbers that are reserved.
SELECT " Movie_title", SeatNum FROM Movies, BookTicket, Cinema WHERE BookTicket.Cinema_id = (SELECT Cinema.Cinema_id WHERE " Cinema_name" = 'Cinemaprism') and Movies.Movie_id = BookTicket.Movie_id;

## 7. Given a reservation# list the cinema, movie session, and time where seats were booked.
SELECT " Cinema_name", " Screen_time", SeatNum FROM Cinema, BookTicket, Screening WHERE Screening.Movie_id = (SELECT BookTicket.Movie_id WHERE BT_ID = 1) and " Cinema_id"= (SELECT Cinema_id FROM BookTicket WHERE BT_ID = 1) and " Cinema_name" = (SELECT " Cinema_name" WHERE Cinema.Cinema_id = BookTicket.Cinema_id);

## 8. List the movies with their corresponding time, city, and cinema name.
SELECT " Movie_title", " Screen_time", " City_name", " Cinema_name" FROM Movies, Screening, Cinema, City;

## 9. (UPDATED) Given a cinema name list movie title and seat numbers that are reserved.
SELECT " Movie_title", SeatNum FROM Movies, BookTicket, Cinema, Screening WHERE BookTicket.Cinema_id = (SELECT Cinema_id FROM Cinema WHERE " Cinema_name" = 'Cinemaprism');

