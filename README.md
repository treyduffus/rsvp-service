# RSVP Service

## Introduction

In this activity, you will create a new GitHub repo for the RSVP Service. You'll set up the RSVP Service and database, verify the service runs locally, and push the latest code to the new GitHub repo.

## Instructions

1. Create a new public repo named `RsvpService`.

2. Clone the `RsvpService` repo locally.

3. Copy the `rsvp-service` folder from the [starter code](./activities/01-we-rsvp-service/starter) into the folder for your local `RsvpService` repo.

4. Update the application properties.

    * The main application properties file for development is in `rsvp-service\src\main\resources\`

    * Rename the `application-development.properties.example` file to `application-development.properties`

    * Update the connection information with the username and password for your local database.

5. Update the test application properties.

    * The test application properties file for development is in `rsvp-service\src\test\resources\`

    * Rename the `application-development.properties.example` file to `application-development.properties`

    * Update the connection information with the username and password for your local test database.

6. Create the main database for the `rsvp-service` project on your local instance of MySQL using the following SQL:

    ```sql
    create schema if not exists rsvp;
    use rsvp;
            
    create table if not exists rsvp (
    rsvp_id int not null auto_increment primary key,
    guest_name varchar(50) not null,
    total_attending int not null
    );
    ```

7. Create the test database for the `rsvp-service` project on your local instance of MySQL using the following SQL:

    ```sql
    create schema if not exists rsvp_test;
    use rsvp_test;
            
    create table if not exists rsvp (
    rsvp_id int not null auto_increment primary key,
    guest_name varchar(50) not null,
    total_attending int not null
    );
    ```

8. Open the `rsvp-service` starter project in IntelliJ and run all tests to confirm everything is working properly.

9. Once the `rsvp-service` is working locally, use git to add, commit, and push your local files to the remote `RsvpService` repo.

    ```git
    git add .
    git commit -m "initial project"
    git push origin main
    ```

---

© 2023 2U. All Rights Reserved.
