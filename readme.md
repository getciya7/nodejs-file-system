# NodeJS File System

This project is a simple Node.js API for creating and retrieving text files with timestamps. The API allows you to create text files with the current timestamp and retrieve all text files along with their content from a specified folder.

---

## Documentation

The API documentation is available in following Postman URL: [https://documenter.getpostman.com/view/37164917/2sA3kVm1pB](https://documenter.getpostman.com/view/37164917/2sA3kVm1pB)

---

## Endpoints

### POST `/create-file`

Creates a new text file with the current timestamp.

#### Response

- `200 OK`: File created successfully.
- `500 Internal Server Error`: Error writing file.

#### Example Response

```json
{
  "message": "File 2024-07-23T07-09-59.043Z.txt created successfully"
}
```

### GET `/get-files`

Retrieves all text files from the specified folder along with their content.

#### Response

- `200 OK`: List of files with their content.
- `500 Internal Server Error`: Error reading files.

#### Example Response

```json
[
  {
    "fileName": "2024-07-23T06-58-19.890Z.txt",
    "content": "2024-07-23T06:58:19.890Z"
  },
  {
    "fileName": "2024-07-23T07-09-59.043Z.txt",
    "content": "2024-07-23T07:09:59.043Z"
  }
]
```

---

## Getting Started

### Installation

1. Clone the repository:

   ```sh
   git clone https://github.com/getciya7/nodejs-file-system.git
   cd nodejs-file-system
   ```

2. Install dependencies:

   ```sh
   npm install
   ```

### Running the Server

1. Start the server:

   ```sh
   node server.js
   ```

2. The server will be running at `http://localhost:3000`.

### Testing the API

Use an API testing tool like [Postman](https://www.postman.com/) to test the endpoints.

---
