# Google meet clone

Google meet is an app that lets you do video conferencing with other people. It also lets you share your screen with other people.

## Requirements

- User sign up & login
- Create meeting
- Join meeting by id
- Screen sharing
- Muting & un-muting

### Backend Service

- Users sign up & sign in (users table)
- Create a new meeting (meetings table)
- WebRTC handshake
- Event & chat relay between users

### Frontend service

- Google Meet clone in Angular

## Workflow

### User Sign-up and Login

- User visits website
- User clicks on "Sign Up" button
- User enters name, email address, and password
- User clicks on "Create Account" button
- An email verification link is sent to the user's email address
- User clicks on the verification link to activate their account
- User can now log in to the platform using their email address and password

### Meeting Creation

- User clicks on "Create Meeting" button
- User enters meeting title, date, time, and duration
- User selects meeting type (e.g., public, private, team meeting)
- User clicks on "Create Meeting" button
- A unique meeting link is generated and shared with the user

### Meeting Link Sharing

- User can share the meeting link with other users
- Other users can click on meeting link to join

### Joining a Meeting

- User clicks on meeting link
- User enters name and email address (if not already logged in)
- User clicks on "Join Meeting" button
- User is connected to meeting and can see and hear other participants

### Stream Processing and Compression

- Audio and video streams from participants are captured and processed in real-time
- Streams are compressed using a suitable codec (e.g., VP8, H.264) to reduce bandwidth usage

### Stream Decompression at Frontend

- Compressed streams are decompressed at frontend
- Decompressed streams are rendered in user's browser

### Streaming Meeting Audio/Video Using WebSockets

- WebSockets are used to establish a real-time connection between frontend and backend
- Compressed audio and video streams are sent from backend to frontend over WebSocket connection
- Frontend receives streams and decompresses them for rendering
