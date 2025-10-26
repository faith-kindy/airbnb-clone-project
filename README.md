# airbnb-clone-project
The Airbnb project is a web-based platform that allows users to book accommodations and list their own properties for short-term rentals. It connects hosts, who offer places such as apartments, homes, or rooms, with guests, who are looking for temporary lodging

# Team Roles
Backend Developer:
Builds and manages the server-side logic, APIs, and database connections. Ensures data flows smoothly between the frontend and backend, handling things like user authentication, bookings, and payments.

Frontend Developer:
Designs and develops the user interface that users interact with. Focuses on responsive layouts, search pages, listings, and booking forms using web technologies like HTML, CSS, and JavaScript.

Database Administrator (DBA):
Designs, manages, and secures the project’s database. Handles data storage for users, properties, and bookings, ensuring performance, backups, and reliability.

UI/UX Designer:
Creates the overall look, feel, and user experience of the application. Works on layouts, color schemes, and navigation to make the platform intuitive and user-friendly.

Project Manager:
Oversees the entire project from planning to deployment. Coordinates the team, tracks progress, and ensures the project meets deadlines and goals.

Quality Assurance (QA) Tester:
Tests the system for bugs, performance issues, and usability problems. Ensures all features work as expected before release

# Technology Stack
 1. Django

A high-level Python web framework used to build secure and scalable web applications.
Purpose: Handles the backend logic, routing, and RESTful API creation for managing users, properties, and bookings.

 2. Node.js

A JavaScript runtime environment for running code on the server side.
Purpose: Enables backend development using JavaScript, handling user requests and connecting to databases efficiently.

3. Express.js

A fast and minimalist backend framework built on Node.js.
Purpose: Simplifies building APIs by managing routes, middleware, and data exchange between frontend and backend.

 4. React

A frontend JavaScript library for building dynamic user interfaces.
Purpose: Powers the interactive parts of the website such as property searches, booking forms, and user dashboards.

 5. MySQL

A relational database management system (RDBMS).
Purpose: Stores and organizes structured data like user accounts, property details, and booking information.

 6. MongoDB

A NoSQL database that stores information in flexible, JSON-like documents.
Purpose: Handles unstructured or rapidly changing data, such as reviews, images, and property listings.

 7. PostgreSQL

An advanced open-source relational database system.
Purpose: Provides secure and efficient data storage with strong support for complex queries and geolocation features.

 8. GraphQL

A query language and runtime for APIs.
Purpose: Lets the client request exactly the data it needs, improving performance and reducing unnecessary API calls.

 9. HTML (HyperText Markup Language)

The foundation of all web pages.
Purpose: Defines the structure and content of pages such as property listings, profiles, and booking pages.

🎨 10. CSS (Cascading Style Sheets)

The styling language used to design web pages.
Purpose: Controls layout, colors, and responsiveness to create a clean and attractive user interface.

 11. JavaScript

A programming language used on both frontend and backend.
Purpose: Adds interactivity and dynamic behavior to the website, such as animations, filters, and form validations.

 12. Git & GitHub

Version control and collaboration tools for developers.
Purpose: Manage project versions, track code changes, and collaborate effectively with team members

# Database Design
1. User

Description: Represents individuals who use the platform — both hosts and guests.

Key Fields:

user_id – Unique identifier for each user.

name – Full name of the user.

email – User’s email address (used for login and communication).

role – Defines if the user is a host, guest, or admin.

date_joined – The date the user created their account.

Relationships:

A user (as a host) can list multiple properties.

A user (as a guest) can make multiple bookings.

A user can write multiple reviews for properties they’ve booked.

2. Property

Description: Represents a home, apartment, or space listed by a host for rent.

Key Fields:

property_id – Unique identifier for each property.

host_id – Foreign key referencing the user_id of the host.

title – Name or short description of the property.

location – Address or area where the property is located.

price_per_night – Cost to stay per night.

Relationships:

A property belongs to one user (host).

A property can have multiple bookings.

A property can have multiple reviews.

 3. Booking

Description: Represents a reservation made by a guest for a specific property.

Key Fields:

booking_id – Unique identifier for each booking.

property_id – Foreign key referencing the property being booked.

guest_id – Foreign key referencing the user (guest) who made the booking.

start_date – Check-in date.

end_date – Check-out date.

status – Booking status (e.g., Pending, Confirmed, Cancelled).

Relationships:

A booking belongs to one property.

A booking is made by one user (guest).

A booking may have one payment record.

4. Payment

Description: Represents payment details for a booking.

Key Fields:

payment_id – Unique identifier for the payment.

booking_id – Foreign key referencing the related booking.

amount – Total amount paid.

payment_date – Date when the payment was made.

payment_method – Method used (e.g., credit card, PayPal).

Relationships:

A payment belongs to one booking.

Each booking has one associated payment.

 5. Review

Description: Represents feedback provided by guests after completing a booking.

Key Fields:

review_id – Unique identifier for each review.

property_id – Foreign key referencing the reviewed property.

guest_id – Foreign key referencing the user who wrote the review.

rating – Numeric rating (e.g., 1–5).

comment – Textual feedback from the guest.

Relationships:

A review belongs to one property.

A review is written by one user (guest).

A property can have many review
