# Online Contact Management System

## Features

### User Management

- **Create User**: Allows the addition of a new user with the user details stored in the database.
  
- **Update User**: Enables modification of existing user details. Throws a `UserNotFoundException` if the user does not exist.

- **Delete User**: Permits the removal of an existing user. Throws a `UserNotFoundException` if the user does not exist.

- **Get User**: Facilitates the retrieval of details for an existing user. Throws a `UserNotFoundException` if the user does not exist.

### Logging

- **User Creation Logging**: Generates logs after a new user is created.

- **User Update Logging**: Generates logs both before and after a user is updated.

## Running the Application

Execute the main function in the `OnlineContactManagementSystemApplication` class located [here](src/main/java/com/signify/onlinecontactmanagementsystem/OnlineContactManagementSystemApplication.java).

## API Usage Guide

The API runs on `localhost` at port `8080`.

### User Management

- **Create User**: Send a `POST` request to `http://localhost:8080/api/v1/users` with user details in the request body, formatted as JSON. For example:

    ```json
    {
        "userName": "Kallol Kumar Rath",
        "email": "kallolrath20@gmail.com",
        "phoneNumber": "8249588122"
    }
    ```

- **Get User**: Send a `GET` request to `http://localhost:8080/api/v1/users/{userId}`, replacing `{userId}` with the user's id.

- **Update User**: Send a `PUT` request to `http://localhost:8080/api/v1/users/{userId}`, replacing `{userId}` with the user's id. Include updated user details in the request body, following the same format as the `POST` request.

- **Delete User**: Send a `DELETE` request to `http://localhost:8080/api/v1/users/{userId}`, replacing `{userId}` with the user's id.

Ensure that all requests include the `Content-Type` header set to `application/json`.

This guide assumes the use of a tool like `Visual Studio Code using Thunder Client` for sending HTTP requests. If using a different tool, the steps may vary.

## Accessing the H2 Database Console

1. Open your web browser and go to `http://localhost:8080/h2-console`.

2. Complete the login form with the following details:

    - **JDBC URL**: `jdbc:h2:mem:testDb`
    - **User Name**: `sa`
    - **Password**: `1234`

3. Click the "Connect" button.

## Testing

Test for creating a user is available in the `UserControllerTest` class found [here](src/test/java/com/signify/onlinecontactmanagementsystem/controller/UserControllerTest.java).

## Submission Requirements

Screenshots required for submission can be found [here](Results.pdf).
