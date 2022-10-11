## 2. Enter a city name and retrieve all the movies that are released within that particular city.
SELECT " Movie_title" FROM Movies, City, Screening, Cinema WHERE " City_name" = 'Arlington' and " Cinema_id" = "Cinema_id" and Movies."Movie_id" = Screening."Movie_id" and City_id = " City_id";

![question2](https://user-images.githubusercontent.com/81663980/194986508-ba59581e-af22-446d-b55b-3d345c427c2f.jpg)

## 3. List all cinemas that are showing a particular movie.
SELECT " Cinema_name" FROM Cinema, Movies, Screening WHERE Screening.Movie_id = (SELECT Movies.Movie_id WHERE " Movie_title" = 'Vertigo') and Cinema_id = " Cinema_id";

![question3](https://user-images.githubusercontent.com/81663980/194986537-8b20db15-293c-4513-91ca-fac13e82b5e5.jpg)

## 4. List the seats that are booked in all cinemas for a particular movie.
SELECT SeatNum FROM BookTicket, Movies WHERE BookTicket.Movie_id = (SELECT Movie_id FROM Movies WHERE " Movie_title" = 'Vertigo');

![q4](https://user-images.githubusercontent.com/81663980/194986559-64d9cfdc-4d89-47f0-b63f-271f5e7fa304.jpg)

## 5. Given a specific cinema and movie list the showing times for that movie.
SELECT " Screen_time" FROM Cinema, Movies, Screening WHERE Screening.Movie_id = (SELECT Movies.Movie_id WHERE " Movie_title" = 'Vertigo') and " Cinema_id" = (SELECT Cinema_id WHERE " Cinema_name" = 'Cinemaprism');

![q5](https://user-images.githubusercontent.com/81663980/194986587-8e47f3d0-4e89-4bcf-a4b9-860aa23d286b.jpg)


## 6. (UPDATED) Given a cinema name list movie title and seat numbers that are reserved.
SELECT " Movie_title", SeatNum FROM Movies, BookTicket, Cinema WHERE BookTicket.Cinema_id = (SELECT Cinema.Cinema_id WHERE " Cinema_name" = 'Cinemaprism') and Movies.Movie_id = BookTicket.Movie_id;

![q6](https://user-images.githubusercontent.com/81663980/194986604-8416b4df-0da4-4780-a9ab-f4d0ac1bbedf.jpg)

## 7. Given a reservation# list the cinema, movie session, and time where seats were booked.
SELECT " Cinema_name", " Screen_time", SeatNum FROM Cinema, BookTicket, Screening WHERE Screening.Movie_id = (SELECT BookTicket.Movie_id WHERE BT_ID = 1) and " Cinema_id"= (SELECT Cinema_id FROM BookTicket WHERE BT_ID = 1) and " Cinema_name" = (SELECT " Cinema_name" WHERE Cinema.Cinema_id = BookTicket.Cinema_id);

![q7](https://user-images.githubusercontent.com/81663980/194986618-b64bad0c-002c-48b0-8f95-3f3f91270062.jpg)

## 8. List the movies with their corresponding time, city, and cinema name.
SELECT " Movie_title", " Screen_time", " City_name", " Cinema_name" FROM Screening, Movies, Cinema, City WHERE Movies.Movie_id = Screening.Movie_id and " Cinema_id" = Cinema_id and " City_id"=City_id;

![question8](https://user-images.githubusercontent.com/81663980/194986644-3105be8d-d997-4318-a3b9-acf216d40509.jpg)

## 9. (UPDATED) Given a cinema name list movie title and seat numbers that are reserved.
SELECT " Movie_title", SeatNum FROM Movies, BookTicket, Cinema, Screening WHERE BookTicket.Cinema_id = (SELECT Cinema_id FROM Cinema WHERE " Cinema_name" = 'Cinemaprism');

![q9](https://user-images.githubusercontent.com/81663980/194986665-6fea5f7d-14e2-48d5-8785-0bc079d7584b.jpg)
