# airbnb-clone-project.
## About
My ALX project on AirBnB Project,this is to bridge tenant and real estate developers.
The Airbnb Clone Project is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security. This project enables learners to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application.
## Tech Stack
+ Frontend Dev.  
+ Backend Dev.  
+ DevOps.  
+ Database Administrator.  
## Team Roles
+ Frontend Dev.: Responsible for designing and implementing the user-facing components of the Airbnb platform.  
+ Backend Dev.: Handles the server-side logic and connects the frontend with the database.  
+ DevOps:  Manages deployment, scalability, and overall system reliability. 
+ Database Administrator: Responsible for designing and maintaining the project’s data layer.  
## Technology Stack  
+ GraphQL / REST APIs : For efficient data fetching from the backend.  
+ React.js – JavaScript library for building fast, reusable UI components.  
+ GraphQL (Apollo Server) : Used for efficient and flexible data querying.  
+ Ruby on Rails: Airbnb’s original core backend framework.  
+ PostgreSQL (formerly MySQL): PostgreSQL ensures reliable relational data management (users, listings, bookings).Redis boosts performance, and Elasticsearch powers instant location-based searches.  
+ OAuth 2.0 / JWT : For secure user authentication.  
+ HTTPS (TLS/SSL) : For encrypted data transfer.   
+ WAF & IAM (AWS) : For secure cloud access control.  
+ Braintree / Stripe / PayPal SDKs: Secure transactions and currency handling.  
+ Amazon S3 : Cloud storage for images and documents.  
## Database Design
+ Users: id(UUID/Primary Key), name(string), email(string,unique), password_hash(string), role(enum:"guest, "host","admin").
+ Propeties: id, user_id, title, description, location.
+ Bookings: id, user_id, property_id, check_in, check _out, total_price
+ Payment: id, booking_id, amount, status, payment_method
+ Review: comment,user_id, id,rating, property_id

__Entity Relationships Overview__  
1. User ↔️ Properties: One-to-Many (a host can list many properties).  
1. User ↔️ Bookings: One-to-Many (a guest can make many bookings).  
1. Property ↔️ Bookings: One-to-Many (each property can be booked many times).  
1. Booking ↔️ Payment: One-to-One (each booking has a single payment).  
1. Property ↔️ Reviews: One-to-Many (each property can be reviewed multiple times).  
1. User ↔️ Reviews: One-to-Many (a user can leave many reviews).  
