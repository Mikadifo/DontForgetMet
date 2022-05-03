# DontForgetMet
DontForgetMe mobile app backend

DontForgetMe is an IOS app which objective is to remeber you each time you are leaving home for work, school, etc to take your important things with you.
## Features
* Account
  * Login
  * Register
  * Update Personal Info
  * Change Password
  * Delete Account
* Things
  * Create new thing
  * Upate a thing
  * Delete things
  * List of your things
* Emergency Contacts
  * Create a new contact
  * Update an existing contact
  * Delete contacts
* Schedules
  * Create a new schedule
  * Update an existing schedule
  * Delete schedules
## API Endpoints
| NAME                  | DESCRIPTION                           | URL    | METHOD | BODY |
| --------------------- | ------------------------------------- | ------ | ------ | ---- |
| Users                 | Returns a list of all users in the app. | /users | GET    | NA   |
| Login                 | Login in the app and return the logged in user. | /login | POST    | ` { "username": "username", "password": "password" } ` |
| Create-User           | Creates a new user and return its information.  | /user/create | POST    | `{ "phone": "1234567890", "password": "password", "things": [], "emergencyContacts": [], "email": "example@exp.exp", "username": "username", "schedules": [] }`   |
| User-by-email         | Returns a specific user information by the passed email. | /user/{email} | GET    | NA   |
| User-by-personal-info | Returns a specific user information by the phone, email and username passed. | /user/by/personal\_info | POST    | `{ "email": "example@exp.exp", "username": "username", "phone": "1234567890" }`   |
| User-update           | Updates a specific user by the passed email. | /user/update/{email} | PUT    | `{ "phone": "1234567890", "username": "username" }`   |
| User-delete           | Deletes a specific user by the passed email. | /user/delete/{email} | DELETE    | NA   |
