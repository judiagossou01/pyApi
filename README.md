# pyAPI v1.0.0

## Introduction

An open-source mini project api written in native Python3 to test and build projects

## Usage

* Connect to the API using Postman or Thunder Client

## API Endpoints

    <details>

        <code>POST</code> <code><b>/sessions/login</b></code>

        ##### This route allows users to log in with their email address and password

        ##### Parameters

        > | name      |  type     | data type               | description                                                           |
        > |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
        > | email     |  required | string                  | email                                                                 |
        > | password  |  required | string                  | password                                                              |


        ##### Responses

        > | http code     | content-type                      | response                                                                   |
        > |---------------|-----------------------------------|----------------------------------------------------------------------------|
        > | `200`         | `application/json`                | `{"status":"200", "message":"Login successful", "token": "TOKEN_HERE"}`    |
        > | `401`         | `application/json`                | `{"status":"401", "message":"Incorrect password"}`                         |
        > | `404`         | `application/json`                | `{"status":"500", "message":"User not found"}`                             |

    </details>

    <details>

        <code>POST</code> <code><b>/sessions/register</b></code>

        ##### This route allows a new user to register

        ##### Parameters

        > | name      |  type     | data type               | description                                                           |
        > |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
        > | firstname |  required | string                  | firstname                                                             |
        > | lastname  |  required | string                  | lastname                                                              |
        > | email     |  required | string                  | email                                                                 |
        > | password  |  required | string                  | password                                                              |


        ##### Responses

        > | http code     | content-type                      | response                                                              |
        > |---------------|-----------------------------------|-----------------------------------------------------------------------|
        > | `201`         | `application/json`                | `{"status":"201", "message":"User created successfully"}`             |
        > | `400`         | `application/json`                | `{"status":"401", "message":"Bad Request"}`                           |
        > | `409`         | `application/json`                | `{"status":"409", "message":"Email already exists"}`                  |

    </details>
