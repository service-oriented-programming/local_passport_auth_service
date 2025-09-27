## How to Test with Postman

Follow these steps to test the authentication endpoints using Postman:

### 1. Register a User

- **Method:** POST
- **URL:** `http://localhost:3000/auth/register`
- **Body:**  
  Select `raw` and `JSON` format, then enter:
  ```json
  {
    "username": "your_username",
    "password": "your_password"
  }
  ```
- **Expected Response:**  
  `{ "message": "User registered successfully" }`

---

### 2. Login

- **Method:** POST
- **URL:** `http://localhost:3000/auth/login`
- **Body:**  
  Same as registration.
- **Expected Response:**  
  `{ "message": "Logged in successfully", "user": { ... } }`

---

### 3. Access Profile

- **Method:** GET
- **URL:** `http://localhost:3000/auth/profile`
- **Expected Response:**  
  `{ "message": "Profile data", "user": { ... } }`

---

### Notes

- If you get `Not authenticated` on `/auth/profile`.
- All results are stored in `public/results` (if applicable).