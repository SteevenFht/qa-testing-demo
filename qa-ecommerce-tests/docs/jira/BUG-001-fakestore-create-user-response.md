# BUG-001 - POST /users response does not match API documentation

**Type**: Bug  
**Priority**: Medium  
**Environment**: Fake Store API (public sandbox)  
**Endpoint**: POST /users  

---

## Description
When creating a user using the `POST /users` endpoint, the API response does not match the structure described in the official documentation.

The documentation indicates that the API should return the created user object, but the actual response only contains an `id`.

---

## Steps to Reproduce
1. Send a POST request to `/users` with a valid user payload
2. Observe the response body

---

## Expected Result
The API should return the full user object as described in the documentation.

---

## Actual Result
The API returns only:
```json
{
  "id": 11
}
