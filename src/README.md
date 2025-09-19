# Mergington High School Activities

A comprehensive web application for managing extracurricular activities at Mergington High School. Teachers can manage student registrations while students and parents can browse available activities with advanced filtering and search capabilities.

## Features

### For Teachers
- **Authentication System**: Secure login/logout functionality for teachers
- **Student Registration Management**: Register students for activities with email validation
- **Student Unregistration**: Remove students from activities with confirmation
- **Real-time Updates**: View current enrollment numbers and participant lists

### For Students and Parents
- **Activity Browsing**: View all available extracurricular activities with detailed information
- **Advanced Filtering**: Filter activities by:
  - Category (Sports, Arts, Academic, Community, Technology)
  - Day of the week (Monday through Sunday)
  - Time slot (Before School, After School, Weekend)
- **Search Functionality**: Search activities by name or description
- **Detailed Information**: View activity schedules, descriptions, participant limits, and current enrollment

### Activity Categories
- **Sports**: Basketball, Soccer, Morning Fitness
- **Arts**: Art Club, Drama Club, Manga Maniacs
- **Academic**: Chess Club, Math Club, Debate Team, Science Olympiad, Sunday Chess Tournament
- **Technology**: Programming Class, Weekend Robotics Workshop
- **Community**: Various community service activities

### Technical Features
- **Database Support**: MongoDB with automatic fallback to in-memory storage
- **RESTful API**: FastAPI-based backend with automatic API documentation
- **Responsive Design**: Mobile-friendly interface with filter sidebar
- **Real-time Data**: Live participant counts and availability status

## Technology Stack

- **Backend**: FastAPI (Python web framework)
- **Database**: MongoDB (with in-memory fallback)
- **Frontend**: Vanilla HTML, CSS, and JavaScript
- **Server**: Uvicorn ASGI server
- **Authentication**: SHA-256 password hashing

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/activities` | Get all activities with optional filtering |
| GET | `/activities/days` | Get available days for activities |
| POST | `/activities/{name}/signup` | Register a student for an activity |
| POST | `/activities/{name}/unregister` | Remove a student from an activity |
| POST | `/auth/login` | Teacher authentication |
| GET | `/auth/check-session` | Validate teacher session |

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
