# OneTapUpload

OneTapUpload is a Spring Boot application that works similarly to Google Drive.
It allows users to register using their phone number and verify their identity via the Twilio Verify API.
Once authenticated, users can upload various file types, including images, PDFs, and documents to **OneTapUpload**, which internally interacts with **Google Cloud Platform (GCP)** for secure storage and easy access.
Users do not directly interact with GCP; instead, the application handles storage and retrieval on their behalf.
After a successful upload, users receive a confirmation message along with an object URL for each file.
This URL enables users to download their files and share them with others easily.
Additionally, users can retrieve a list of all their uploaded files.

## Features

### User Registration & Verification

- Users sign up using their phone number.
- OneTapUpload uses **Twilio Verify API** to verify user identity via OTP authentication.

### File Upload & Management

- Upload multiple file types, including images, PDFs, and documents.
- Receive a success message upon a successful file upload.
- Retrieve a list of all files uploaded by the user.
- Each file is assigned a unique **Object URL** for download and sharing.

### Cloud Storage Integration

- OneTapUpload securely stores files by interacting with **Google Cloud Platform (GCP)**.
- Ensures scalability and reliability for file storage while abstracting direct user interaction with GCP.

## Installation & Setup

### Prerequisites

- **Java 17** or later
- **Maven**
- **Spring Boot**
- **Twilio ** (for Verify API)
- **Google Cloud Storage** 



## API Endpoints

### User Authentication

| Method | Endpoint           | Description                   |
| ------ | ------------------ | ----------------------------- |
| POST   | `/auth/sendotp`    | Send OTP for authentication   |
| POST   | `/auth/verifyotp`  | Verify OTP for authentication |
| PATCH  | `/auth/user/update`| Update user details           |

### File Management

| Method | Endpoint                      | Description              |
| ------ | ----------------------------- | ------------------------ |
| POST   | `/files/upload`               | Upload a file            |
| GET    | `/files/download/user/{userId}` | Get all uploaded files for a user |

## Swagger
http://localhost:8080/swagger-ui/index.html#/

![image](https://github.com/user-attachments/assets/b0d8243e-4de2-4555-b90c-645314f29d55)
![image](https://github.com/user-attachments/assets/079b83a4-73ff-4598-8e08-e63f88674d5c)
![image](https://github.com/user-attachments/assets/72f1a7da-197c-427a-840a-d11a0a26aa45)
![image](https://github.com/user-attachments/assets/83c98af6-efb1-4b0e-8835-5526a672e937)
![image](https://github.com/user-attachments/assets/b158e06f-6de1-41d1-9d0b-47e99d8af6e3)




















