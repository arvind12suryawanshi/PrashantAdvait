signup-
curl -X POST http://localhost:8080/auth/signup -H "Content-Type: application/json" -d '{"email":"testuser@example.com", "password":"password"}'

signin-
curl -X POST http://localhost:8080/auth/signin -H "Content-Type: application/json" -d '{"email":"testuser@example.com", "password":"password"}'

Token Authorization-
curl -X GET http://localhost:8080/protected -H "Authorization: Bearer <token>"

Token Revocation-
curl -X POST http://localhost:8080/auth/revoke -H "Authorization: Bearer <token>"

Token Refreshing-
curl -X POST http://localhost:8080/auth/refresh -H "Authorization: Bearer <refresh_token>"

Sign Up: Create a new user account using email and password.
Sign In: Authenticate user credentials and return a JWT token.
Token Authorization: Validate JWT tokens sent with requests, check for token expiry, and handle errors appropriately.
Token Revocation: Revoke tokens from the backend to invalidate them.
Token Refresh: Refresh the JWT token before it expires to maintain a valid session.
