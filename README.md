# RentalFlix

## Entity-Relationship Diagram
![ERD Image](./RentalFlix/ER/RentalFlixER.png)


### RentalFlix Entity-Relationship Diagram (ERD) 🎬

#### Purpose of the Program
The "RentalFlix" project involves designing an Entity-Relationship Diagram (ERD) for a movie rental service. The purpose of this ERD is to capture the key entities and relationships required to efficiently manage the service, including movie inventory, customer information, and rental records, ensuring a seamless experience for both staff and customers. 🍿🎥

#### Application Specifications

**Movies 🎞️**
- Each movie has a unique identifier (MovieID), title, genre, director, release year, and rating.
- Movies are available in multiple formats (DVD, Blu-ray, Digital).
- Each movie format has a unique identifier and may have different quantities available.

**Customers 🧑‍🤝‍🧑**
- Each customer has a unique CustomerID, name, address, phone number, and email.
- Customers can rent multiple movies but must return them within a specified period.

**Rentals 📅**
- A record of each rental must be kept, including the customer who rented the movie, the movie format rented, the rental date, and the due date.
- The system should also track the return date when a movie is returned.

**Reservations 📖**
- Customers can reserve movies that are currently rented out by others.
- A reservation record includes the customer ID, movie ID, reservation date, and the status of the reservation (active, fulfilled, canceled).

#### ERD Components

**Movie 🎥**
- **MovieID** (PK): Unique identifier for each movie.
- **Title**: Title of the movie.
- **Genre**: Genre or category of the movie.
- **Director**: Director of the movie.
- **ReleaseYear**: The year the movie was released.
- **Rating**: Movie rating (e.g., PG, PG-13, R).

**MovieFormat 💽**
- **MovieFormatID** (PK): Unique identifier for each movie format.
- **MovieID** (FK): Identifier of the movie.
- **FormatType**: Type of format (DVD, Blu-ray, Digital).
- **QuantityAvailable**: Number of copies available for rent.

**Customer 👤**
- **CustomerID** (PK): Unique identifier for each customer.
- **Name**: Name of the customer.
- **Address**: Address of the customer.
- **PhoneNumber**: Contact phone number.
- **Email**: Contact email address.

**Rental 🏷️**
- **RentalID** (PK): Unique identifier for each rental record.
- **CustomerID** (FK): ID of the customer who rented the movie.
- **MovieFormatID** (FK): ID of the movie format that was rented.
- **RentalDate**: Date when the movie was rented.
- **DueDate**: The date when the movie is due to be returned.
- **ReturnDate**: Date when the movie was returned (nullable).

**Reservation 📅**
- **ReservationID** (PK): Unique identifier for each reservation.
- **CustomerID** (FK): ID of the customer who reserved the movie.
- **MovieID** (FK): ID of the reserved movie.
- **ReservationDate**: Date when the reservation was made.
- **Status**: Status of the reservation (active, fulfilled, canceled).

#### Relationships 🔗
- **Each movie** can have multiple **formats** (1:Many).
- **Each customer** can have multiple **rentals** (1:Many).
- **Each rental record** is associated with one **customer** and one **movie format** (Many:1).
- **Each movie** can have multiple **reservations** (1:Many).
- **Each reservation** is associated with one **customer** and one **movie** (Many:1).

This ERD captures the structure and relationships of the RentalFlix movie rental service, facilitating efficient management and operation of the rental system.