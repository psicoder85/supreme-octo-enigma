# Question 1. General Description of the API
The REST API we're discussing provides endpoints for managing employee data. It allows clients to perform CRUD (Create, Read, Update, Delete) operations on employee records. Below are the key features and functionalities:

### 1. All Employee Retrieval (GET /employee/):
  -This endpoint retrieves information about all employee on a specific company database.
  -The client sends a GET request with the employee ID as a path parameter.
  -The server responds with the employee’s details (such as name, department, contact information, etc.) in JSON format.
  -If the employee with the specified ID does not exist, the API returns an appropriate error response (e.g., 404 Not Found).

### 2. Employee Retrieval (GET /employee/{id}):
  -This endpoint retrieves information about a specific employee based on their unique identifier (id).
  -The client sends a GET request with the employee ID as a path parameter.
  -The server responds with the employee’s details (such as name, department, contact information, etc.) in JSON format.
  -If the employee with the specified ID does not exist, the API returns an appropriate error response (e.g., 404 Not Found).

### 3. Employee Creation (POST /create):
  -Clients can use this endpoint to create a new employee record.
  -The client sends a POST request with a JSON payload containing employee details (e.g., name, job title, salary, etc.).
  -The server validates the input data, creates a new employee entry in the database, and assigns a unique ID.
  -The API responds with a success message (e.g., 201 Created) along with the newly created employee’s ID.
  -If the input data is invalid or incomplete, the API returns an error response (e.g., 400 Bad Request).

### 4. Employee Update (PUT /employee/{id}) 
 - These endpoints allow clients to update or delete an existing employee record.
 - For updating, the client sends a PUT request with the employee ID and updated details in the JSON payload.
 - The server validates the input, modifies the employee data, and responds with a success message.

### 5. Employee Deletion (DELETE /employee/{id}):
 - For deletion, the client sends a DELETE request with the employee ID.
 - The server removes the employee from the database and returns a success message.
 - If the specified employee ID is not found during update or delete operations,   appropriate error responses are returned.

### Table
| Route     |    Method   |  Type  |    Full Route                                       |    Description                  | 
| /employee |    GET      |  JSON  | https://dummy.restapiexample.com/api/v1/employees   |   Get all employee data         |
| Route     |    GET      |  JSON  | https://dummy.restapiexample.com/api/v1/employee/1  |   Get a single employee data    |
| Route     |    POST     |  JSON  | https://dummy.restapiexample.com/api/v1/create      |   Create new record in database |
| Route     |    PUT      |  JSON  | https://dummy.restapiexample.com/api/v1/update/21   |   Update an employee record     |
| Route     |   DELETE    |  JSON  | https://dummy.restapiexample.com/api/v1/delete/2    |   Delete an employee record     |



# Question 2. cURL Commands and JSON Payloads
 1. Retrieve Employee Details (GET /employee/{id}):
  -cURL Command:
   ``curl -X GET https://api.example.com/employee/123``

 -Expected Result (JSON):
     JSON

      ``{
       "id": 123,
       "name": "John Doe",
       "department": "Engineering",
       "email": "john.doe@example.com"
       // Other employee properties...
      }``
 2. Create New Employee (POST /create):
  - cURL Command:
   ``curl -X POST -H "Content-Type: application/json" -d '{
  "name": "Jane Smith",
  "department": "Marketing",
  "email": "jane.smith@example.com"
  // Other employee properties...
}' https://api.example.com/create ``

  - Expected Result (Response):
  -Employee created successfully. ID: 124


# Question 3. Explain required field for /employee and what kind of data they can hold. What other elements should be included, in your opinion?

## Elements that could be included:
 - Other Optional Fields (Depending on Business Requirements):
 - Job Title (String): Describes the employee’s role (e.g., "Software Engineer", "Marketing Manager").
 - Phone Number (String): Contact number for the employee.
 - Address (String): Physical address or location.
 - Start Date (Date): When the employee joined the company.
 - Supervisor ID (Integer): ID of the employee’s supervisor (if applicable).

 ## Required Fields for /employee
When designing the /employee endpoint, it’s essential to define the required fields that a client must provide when creating or updating an employee record. Here are the fundamental fields and their data types:


 1. Employee ID.
    -Unique value identifier of every employee at the X company.
 
 2. Employee Name (String):
   - Represents the full name of the employee.
   - Example: "John Doe"

 3. Employee (Numeric).
   - Represents the employee’s annual salary (e.g., 75000)..
   

 4. Employee age.
    - Eg. "35" / "49"

 5. Employee profile image

 ## Elements that could be included:
 1. Department (String or Enum):
   - Indicates the department or team to which the employee belongs.
   - You can use a string (e.g., "Engineering", "Marketing") or an enumeration (e.g., 1 for Engineering, 2 for Marketing).
   - Consider using an enum if you want to enforce consistency and avoid typos.
   - Example: "Engineering"
 
 2. Email (String - Valid Email Format):
   - The employee’s email address for communication.
   - Ensure that the email follows a valid format (e.g., john.doe@example.com).
   - Example: "john.doe@example.com"

 ### Other Optional Fields (Depending on Business Requirements):
    1. Job Title (String): 
     -Describes the employee’s role (e.g., "Software Engineer", "Marketing Manager").

   2. Phone Number (String): 
    - Contact number for the employee.

   3. Address (String):
    - Physical address or location.

   4. Start Date (Date): 
    - When the employee joined the company.

   5. Supervisor ID (Integer): 
    - ID of the employee’s supervisor (if applicable).

 ### Additional Considerations:
 1. Validation:
   - Implement validation rules for each field (e.g., minimum/maximum length, valid email format, salary range).
   - Handle edge cases gracefully (e.g., duplicate email addresses, missing fields).

 2. Authentication and Authorization:
   - Ensure that only authorized users (e.g., HR personnel) can create or update employee records.
   - Use authentication tokens or API keys.

 3. Response Format:
   - Define the format of the response when creating or retrieving an employee (e.g., JSON).

# Question 4. Guide for an Entry-level how to use `/employee/` and `/delete/{id}` feature.

## Creating or Updating an Employee (`/employee`)
 1. Create a New Employee:
   - Send a POST request to `/employee` with a JSON payload containing the required fields (name, department, email, etc.).
   - Example:
     ``curl -X POST -H "Content-Type: application/json" -d '{
     "name": "Jane Smith",
     "department": "Marketing",
     "email": "jane.smith@example.com"
      // Other employee properties...
     }' https://api.example.com/employee``

   - Expect a success response (e.g., 201 Created) with the newly assigned employee ID.
 
 2. Update an Existing Employee:
   - Send a PUT request to /employee/{id} with the employee ID and updated details in the JSON payload.
   - Example:
     ``curl -X PUT -H "Content-Type: application/json" -d '{
      "name": "Jane Doe",
      "department": "Sales"
      // Other updated properties...
      }' https://api.example.com/employee/123``

   - Expect a success response (e.g., 200 OK) after the update.
   
## Deleting an Employee (`/delete/{id}`)
  1. Delete an Employee:
    - Send a DELETE request to /delete/{id} with the employee ID.
    - Example:
       ``curl -X DELETE 
       https://api.example.com/delete/123``

    - Expect a success response (e.g., 204 No Content) indicating successful deletion.

## Examples:
  | Route                | Method | Type  | Full Route                                              | Description                    |
|----------------------|--------|-------|---------------------------------------------------------|--------------------------------|
| /employee            | GET    | JSON  | `https://api.example.com/api/v1/employees`              | Get all employee data          |
| /employee/{id}       | GET    | JSON  | `https://api.example.com/api/v1/employee/1`             | Get a single employee data     |
| /create              | POST   | JSON  | `https://api.example.com/api/v1/create`                 | Create new record in database  |
| /update/{id}         | PUT    | JSON  | `https://api.example.com/api/v1/update/21`              | Update an employee record      |
| /delete/{id}         | DELETE | JSON  | `https://api.example.com/api/v1/delete/2`               | Delete an employee record      |

## Notes: 
Dont forget the status codes responses:

 | Status Code     | Description   | Description                                                      |
 | 1xx             | Informational | Communicates transfer protocol-level information.                |
 | 2xx             | Success       | Indicates that the client’s request was accepted successfully.    |
 | 3xx             | Redirection   | Indicates that the client must take some additional action in order to complete their request.     |
 | 4xx             | Client error  | This category of error status codes points the finger at clients.   |
 | 5xx             | Server Error  | The server takes responsibility for these error status codes.   |

 ### List of Code Responses:
 #### 1. 1×× Informational

  - 100 Continue
  - 101 Switching Protocols
  - 102 Processing

#### 2. 2×× Success

  - 200 OK
  - 201 Created
  - 202 Accepted
  - 203 Non-authoritative Information
  - 204 No Content
  - 205 Reset Content
  - 206 Partial Content
  - 207 Multi-Status
  - 208 Already Reported
  - 226 IM Used

#### 3. 3×× Redirection

-300 Multiple Choices
-301 Moved Permanently
-302 Found
-303 See Other
-304 Not Modified
-305 Use Proxy
-307 Temporary Redirect
-308 Permanent Redirect

#### 4. 4×× Client Error

-400 Bad Request
-401 Unauthorized
-402 Payment Required
-403 Forbidden
-404 Not Found
-405 Method Not Allowed
-406 Not Acceptable
-407 Proxy Authentication Required
-408 Request Timeout
-409 Conflict
-410 Gone
-411 Length Required
-412 Precondition Failed
-413 Payload Too Large
-414 Request-URI Too Long
-415 Unsupported Media Type
-416 Requested Range Not Satisfiable
-417 Expectation Failed
-418 I’m a teapot
-421 Misdirected Request
-422 Unprocessable Entity
-423 Locked
-424 Failed Dependency
-426 Upgrade Required
-428 Precondition Required
-429 Too Many Requests
-431 Request Header Fields Too Large
-444 Connection Closed Without Response
-451 Unavailable For Legal Reasons
-499 Client Closed Request

#### 5×× Server Error

-500 Internal Server Error
-501 Not Implemented
-502 Bad Gateway
-503 Service Unavailable
-504 Gateway Timeout
-505 HTTP Version Not Supported
-506 Variant Also Negotiates
-507 Insufficient Storage
-508 Loop Detected
-510 Not Extended
-511 Network Authentication Required
-599 Network Connect Timeout Error
 
#### For more information and in-depth, visit:
  [RESTfulapi]https://restfulapi.net/http-status-codes/
