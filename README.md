# AuthSystem: Secure Node.js Authentication with JWT & Cloudinary 🌐🔐

![AuthSystem](https://img.shields.io/badge/AuthSystem-Node.js-brightgreen) ![Version](https://img.shields.io/badge/version-1.0.0-blue) ![License](https://img.shields.io/badge/license-MIT-yellowgreen)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Verification](#verification)
- [Image Uploads](#image-uploads)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

AuthSystem is a secure authentication solution built with Node.js. It provides a robust framework for user management and security. The system uses JSON Web Tokens (JWT) for secure authentication and includes features for email and text verification. Additionally, it supports image uploads through Cloudinary, ensuring that your application remains scalable and secure. 

For the latest releases, visit [here](https://github.com/Abijah-Mbala-Mbala/AuthSystem/releases).

## Features

- **Secure Authentication**: Uses JWT for secure user sessions.
- **Email Verification**: Ensures users verify their email before accessing the system.
- **Text Verification**: Adds an extra layer of security via SMS verification.
- **Image Support**: Upload images using Cloudinary.
- **Scalable Architecture**: Built on MongoDB for high scalability.
- **RESTful API**: Easy integration with front-end applications.
- **User Roles**: Manage user permissions effectively.

## Technologies Used

- **Node.js**: Server-side JavaScript runtime.
- **Express**: Web framework for Node.js.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: ODM library for MongoDB and Node.js.
- **JWT**: For secure authentication tokens.
- **Cloudinary**: Image and video management.
- **Nodemailer**: For sending emails.
- **Twilio**: For SMS verification.

## Installation

To get started with AuthSystem, follow these steps:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Abijah-Mbala-Mbala/AuthSystem.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd AuthSystem
   ```

3. **Install dependencies**:

   ```bash
   npm install
   ```

4. **Set up environment variables**:

   Create a `.env` file in the root directory and add the following:

   ```
   MONGODB_URI=your_mongodb_uri
   JWT_SECRET=your_jwt_secret
   CLOUDINARY_URL=your_cloudinary_url
   EMAIL_USER=your_email_user
   EMAIL_PASS=your_email_password
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_PHONE_NUMBER=your_twilio_phone_number
   ```

5. **Run the application**:

   ```bash
   npm start
   ```

## Usage

After setting up, you can access the API endpoints. Use tools like Postman or cURL to test the endpoints.

### Example Request

To register a user, send a POST request to `/api/auth/register` with the following body:

```json
{
  "username": "exampleUser",
  "email": "user@example.com",
  "password": "yourPassword"
}
```

## API Endpoints

### Authentication Endpoints

- **Register User**: `POST /api/auth/register`
- **Login User**: `POST /api/auth/login`
- **Verify Email**: `GET /api/auth/verify/:token`
- **Send Verification SMS**: `POST /api/auth/verify-sms`

### User Management

- **Get User Profile**: `GET /api/user/profile`
- **Update User Profile**: `PUT /api/user/profile`
- **Delete User**: `DELETE /api/user/:id`

### Image Uploads

- **Upload Image**: `POST /api/upload`

## Verification

### Email Verification

Upon registration, the user receives an email with a verification link. Clicking this link verifies their email address. 

### SMS Verification

Users can request an SMS verification code. They must enter this code to complete their registration. 

## Image Uploads

AuthSystem supports image uploads via Cloudinary. To upload an image, send a POST request to `/api/upload` with the image file included in the form data.

### Example Upload Request

```bash
curl -X POST http://localhost:5000/api/upload \
-F "image=@/path/to/your/image.jpg"
```

## Contributing

We welcome contributions to AuthSystem. To contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/YourFeature`
3. Make your changes.
4. Commit your changes: `git commit -m 'Add your feature'`
5. Push to the branch: `git push origin feature/YourFeature`
6. Create a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, reach out via GitHub or open an issue in the repository. 

For the latest releases, visit [here](https://github.com/Abijah-Mbala-Mbala/AuthSystem/releases).