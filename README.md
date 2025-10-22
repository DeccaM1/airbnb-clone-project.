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
2. User ↔️ Bookings: One-to-Many (a guest can make many bookings).  
3. Property ↔️ Bookings: One-to-Many (each property can be booked many times).  
4. Booking ↔️ Payment: One-to-One (each booking has a single payment).  
5. Property ↔️ Reviews: One-to-Many (each property can be reviewed multiple times).  
6. User ↔️ Reviews: One-to-Many (a user can leave many reviews).
## Feature Breakdown.  
This section outlines the key features implemented in the Airbnb-style project. Each feature is designed to replicate essential functionality found in modern rental platforms, contributing to a full end-to-end user experience for both hosts and guests.  
+ __User Management__  
Allows users to register, log in, and manage their profiles.  
Includes authentication via email/password and social logins, as well as role-based access (e.g., guest vs. host).  
+ __Property Management__   
Enables hosts to list properties with details like photos, location, pricing, and amenities.  
Hosts can create, update, or remove listings through an intuitive dashboard.  
+ __Booking System__   
Guests can view property availability and make reservations for specific dates.  
Includes dynamic pricing calculations and availability checks to prevent double-bookings.  
+ __Payment Integration__  
Secure payment processing is handled using Stripe or PayPal.  
Ensures smooth transactions, supports multiple currencies, and handles booking confirmations after successful payment.  
+ __Reviews & Ratings__  
Guests can leave reviews and ratings after completing a stay.  
These reviews are visible on property pages, helping future guests make informed decisions.  
+ __Search & Filtering__  
Users can search for properties based on location, dates, price, and amenities.  
Powered by full-text search and filters for a tailored browsing experience.  
+ __Booking History & Receipts__  
Users can view their past and upcoming bookings, along with digital receipts.  
Provides transparency and a reliable booking record for both guests and hosts.  
+ __Host Dashboard__  
Hosts have access to a dashboard to manage listings, view earnings, and track booking analytics.  
Helps hosts make informed decisions about their property offerings.  
## API Security  
1. __Authentication__  
User authentication is handled using secure methods such as hashed passwords (bcrypt) and OAuth 2.0 for third-party logins (Google, Facebook).  Authentication ensures only verified users can access their accounts, protecting personal data and preventing unauthorized access.
2. __Authorization__  
Role-based access control (RBAC) is enforced to differentiate between guests, hosts, and admins.  
Certain actions (e.g., creating listings or viewing host dashboards) are restricted based on user roles.  
Prevents users from performing actions beyond their permissions (e.g., a guest accessing admin routes), maintaining data integrity and platform safety.
3. __Rate Limiting__  
Rate limiting and IP throttling are implemented using tools like Express-rate-limit or API Gateway throttling.  
Protects the API from abuse, brute-force attacks, and bot traffic by limiting the number of requests per user or IP over time.
4. __Secure Payments__  
Payments are processed using secure, PCI-compliant platforms like Stripe or PayPal. Payment data is never stored on our servers.  
Ensures compliance with financial regulations and protects users' financial data from theft or misuse.
5. __Database Security__  
Parameterized queries and ORM-level protections (e.g., with Prisma).  
Regular database backups and access control via roles.  
Encrypted environment variables for sensitive credentials.  
Protects stored user data and prevents unauthorized access or data leaks.
6. __HTTPS (TLS Encryption)__  
All communication between the client and server is encrypted via SSL/TLS, enforced via HTTPS.  
Prevents man-in-the-middle (MITM) attacks and ensures that sensitive data like login credentials and payments cannot be intercepted.
## CI/CD Pipeline  
CI/CD (Continuous Integration and Continuous Deployment) refers to a set of practices that automate the process of building, testing, and deploying code whenever changes are made. This ensures that updates are delivered quickly, reliably, and with minimal manual intervention.  
CI/CD is essential to maintain stability, speed up feature delivery, and ensure users have a seamless experience during updates.  
__CI/CD Tools__  
+ GitHub Action
+ Docker
+ Terraform
+ AWS


