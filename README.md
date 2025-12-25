# Simple Key-Value Store

## Project Description
This project is a simple Key-Value Store implemented using Python and Flask.
It allows storing and retrieving values using a key through REST APIs.

## Technologies
- Python
- Flask
- Git & GitHub
- Docker

## How to Run

### Using Docker
1. Build the image:
   docker build -t kv-store .

2. Run the container:
   docker run -p 5000:5000 kv-store

## API Endpoints

### POST /set
Stores a key-value pair.

### GET /get/{key}
Retrieves the value for a given key.

## Author
Hadis Khani  
Student ID: 14016321914
