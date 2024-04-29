# API Documentation

## Setup

Before running the API server, make sure to follow these setup instructions:

1. Clone the repository:
   ```bash
   git clone <repository_url>
2. cd <project_directory>

npm install
# or
yarn install

cp .env.example .env

### Signup

**Description:** This API endpoint is used for user registration.

**URL:** `/signup`

**Method:** `POST`

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "password123"
}
```
### Login

**Description:** This API endpoint is used for user login.

**URL:** `/login`

**Method:** `POST`

**Request Body:**
```json
{
  "email": "user@example.com",
  "password": "password123"
}
```


Post Event
Description: This API endpoint is used to create a new event.

URL: /addEvents

Method: POST

**Request Body:**

```

{
  "title": "Event Title",
  "description": "Event Description",
  "availableSlots": 100,
  "thumbnail": "event_thumbnail_url"
}
```
Response:

Success Response:
Status Code: 200 OK
Body:
json
```
{
  "message": "Event added",
  "event": {
    "title": "Event Title",
    "description": "Event Description",
    "availableSlots": 100,
    "thumbnail": "event_thumbnail_url"
  }
}
```
Error Response:
Status Code: 500 Internal Server Error
Body:

{
  "error": "Internal server error"
}
Get Events
Description: This API endpoint is used to retrieve a list of events.

URL: /getEvents

Method: GET

Query Parameters:

page (optional): Page number for pagination (default: 1)
Response:

Success Response:
Status Code: 200 OK
Body:
```
{
  "events": [
    {
      "title": "Event Title",
      "description": "Event Description",
      "availableSlots": 100,
      "thumbnail": "event_thumbnail_url"
    },
}
```
Error Response:
Status Code: 500 Internal Server Error
Body:


{
  "error": "Internal server error"
}

Update Event
Description: This API endpoint is used to update an existing event.

URL: /updateEvent/:id

Method: PUT

Request Body:
```
{
  "title": "Updated Event Title",
  "description": "Updated Event Description",
  "availableSlots": 120,
  "thumbnail": "updated_thumbnail_url"
}

```
Response:

Success Response:
Status Code: 200 OK
Body:

{
  "message": "Event updated successfully",
  "event": {
    "title": "Updated Event Title",
    "description": "Updated Event Description",
    "availableSlots": 120,
    "thumbnail": "updated_thumbnail_url"
  }
}
Error Response:
Status Code: 500 Internal Server Error
Body:

{
  "error": "Internal server error"
}
Delete Event
Description: This API endpoint is used to delete an event.

URL: /deleteEvent/:id

Method: DELETE

Response:

Success Response:
Status Code: 200 OK
Body:
```
{
  "message": "Event deleted successfully"
}
```
Error Response:
Status Code: 500 Internal Server Error
Body:

{
  "error": "Internal server error"
}
