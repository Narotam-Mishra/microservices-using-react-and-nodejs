
## Section 1 :- Fundamental Ideas around Microservices

# Lec 3 - What is a Microservice? (3:19)

# Monolithic Architecture - In monolithic server architecture, we have all of our code needed to implement our application inside of one single code base and we deploy that code base as one discrete unit. A monolith contains all the routing, all the middleware, all the business logic in all the database access code required to implement all features of our application.

# Microservice Architecture -  A single microservice contains all of the routing, all the middleware, all the business logic and database access required to implement one feature of our application.

# Monolithic vs Microservice :- A monolith has all the code needed to implement every feature of our application whereas a microservice has all the code needed to implement just one feature.

# Feature of microservice :- The best thing about this approach is that if for some reason, if every other feature or every other service inside of our application crashes or just mysteriously disappears, a portion of our app is still going to work just fine, as service, say is 100% standalone and doesn't necessarily require any other service to work correctly.

# A microservice contains all of the code required to make one feature work correctly.

# Each of microservices are entirely self contained which means it has all of the code required to make feature a work correctly. It has its own middleware, it's got its own router and its own DB. The nice thing about this approach is that if for some reason, if every other feature or every other service inside of our application crashes or just mysteriously disappears, a portion of our app is still going to work just fine, as service, say is 100% standalone and doesn't necessarily require any other service to work correctly.


# Lec 4 - Data in Microservices (7:34)

# A single microservice contains routing, middlewares, business logic and database access to implement one feature of our app.

# Big challenges with the microservices :-

1). Data management between services :- It means the way in which we store data inside of a service and how we communicate that data between different services.

# With microservices, the way in which we store data and access data is a little bit weird. 

Q. How do we store data in a microservices system?
# In microservice, there is a separate DB for each service. So whenever we are making use of microservices, we are going to create a separate database for each service. If the service actually needs a database, if a service doesn't need a database, that's fine.

1). Each service gets its own database (if it needs one)

2). Services will never, ever reach into another services database.

# Database-Per-Service - The idea of giving every service its own database is known Database-Per-Service.

Q. Why Database-Per-Service?
# We want each service to run independently of other services,

# Database schema/structure might change unexpectedly,

# Some services might function more efficiently with different types of DB's (SQL vs NOSQL)

# Problem with 1st approach - The problem with this approach is that if anything bad ever happens to this database, all of our services are going to crash immediately. The other big problem is that scaling this database right here would be really challenging. It would be a lot easier to scale just the databases that need additional capacity or throughput.

# Problem with 2nd approach - If anything ever goes wrong with the database, be right there. Then all of a sudden service is going to start to crash because we have introduced a dependency between service A and service B.

# Lec 5 - Big problems with data (5:08)

