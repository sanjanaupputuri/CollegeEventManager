# College Event Manager App

A comprehensive Android application for managing college events, built with Android Studio using Java/Kotlin and modern Android development practices.

## Overview

The College Event Manager App streamlines event management for our college by providing separate interfaces for students and organizers. Students can discover and register for events, while organizers can create and manage events efficiently.

## Project Structure

```
CollegeEventManagement/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/college/eventmanager/
│   │   │   │   ├── activities/
│   │   │   │   │   ├── SplashActivity.java
│   │   │   │   │   ├── LoginActivity.java
│   │   │   │   │   ├── DashboardActivity.java
│   │   │   │   │   ├── EventListActivity.java
│   │   │   │   │   ├── EventDetailActivity.java
│   │   │   │   │   ├── CreateEventActivity.java
│   │   │   │   │   ├── MyEventsActivity.java
│   │   │   │   │   └── ProfileActivity.java
│   │   │   │   ├── adapters/
│   │   │   │   │   ├── EventListAdapter.java
│   │   │   │   │   └── ParticipantAdapter.java
│   │   │   │   ├── models/
│   │   │   │   │   ├── Event.java
│   │   │   │   │   ├── User.java
│   │   │   │   │   └── Registration.java
│   │   │   │   ├── database/
│   │   │   │   │   ├── DatabaseHelper.java
│   │   │   │   │   └── EventDAO.java
│   │   │   │   ├── utils/
│   │   │   │   │   ├── NotificationHelper.java
│   │   │   │   │   ├── QRCodeGenerator.java
│   │   │   │   │   └── DateUtils.java
│   │   │   │   └── fragments/
│   │   │   │       ├── EventListFragment.java
│   │   │   │       └── ProfileFragment.java
│   │   │   ├── res/
│   │   │   │   ├── layout/
│   │   │   │   ├── values/
│   │   │   │   ├── drawable/
│   │   │   │   └── menu/
│   │   │   └── AndroidManifest.xml
│   │   └── test/
│   ├── build.gradle
│   └── google-services.json
├── gradle/
├── build.gradle
├── settings.gradle
└── README.md
```

## Features

### User Authentication
- Email-password login system with Firebase Auth or local authentication
- Two distinct user roles: Student and Organizer/Admin
- Secure session management and user state persistence
- Role-based access control for different app features

### Event Management

#### For Organizers:
- **Create Events**: Complete event creation with title, date, venue, description, and poster upload
- **Edit Events**: Update existing event information and details
- **Delete Events**: Remove events when necessary
- **Participant Management**: Set participant limits and capacity controls
- **Registration Tracking**: Monitor registrations and view detailed participant lists
- **Real-time Analytics**: Live participant count and event statistics
- **Event Status Control**: Manage event visibility and registration status

#### For Students:
- **Event Discovery**: Browse comprehensive list of upcoming events
- **Search and Filter**: Search events by title, category, date, and venue
- **Category Filtering**: Filter events by type (Cultural, Tech, Management, Sports)
- **Event Details**: View complete event information including venue, timing, and description
- **One-click Registration**: Simple registration process with confirmation
- **Favorites System**: Save events to personal favorites list
- **Registration History**: Track all registered and attended events
- **Event Reminders**: Personal reminder system for registered events

### Notification System
- **Push Notifications**: Firebase Cloud Messaging (FCM) integration for:
  - New event announcements
  - Event reminders before start time
  - Event updates and schedule changes
  - Registration confirmations
- **Local Notifications**: AlarmManager-based reminders for offline functionality
- **Notification Preferences**: User-controlled notification settings

### QR Code Integration
- Generate unique QR codes for each event
- Quick event entry and attendance tracking
- Digital check-in system for organizers

### Theme Support
- Dark and Light theme options
- User preference persistence
- System theme integration

### Offline Mode
- Local SQLite database for offline functionality
- Data synchronization when online
- Cached event information

### Event Analytics
- Comprehensive statistics dashboard for organizers
- Registration trends and patterns
- Attendance tracking and reporting

### Real-time Updates
- Live participant count updates
- Instant event status changes
- Real-time registration notifications

## User Interface Screens

### Core Application Screens:

1. **Splash Screen**
   - Application logo display
   - User authentication status check
   - App initialization and setup

2. **Login/Signup Screen**
   - Email and password authentication
   - User role selection (Student/Organizer)
   - Account creation and validation
   - Forgot password functionality

3. **Dashboard Screen**
   - Role-based interface customization
   - Quick access to main features
   - Recent events and notifications
   - User-specific action buttons

4. **Event List Screen**
   - RecyclerView with event cards
   - Search bar with real-time filtering
   - Category filter options
   - Pull-to-refresh functionality

5. **Event Detail Screen**
   - Complete event information display
   - Event banner/poster image
   - Date, time, and venue details
   - Registration button and status
   - Map integration (optional)
   - Share event functionality

6. **Create Event Screen (Organizer)**
   - Comprehensive event creation form
   - Input validation and error handling
   - Image upload for event posters
   - Date and time picker integration
   - Venue selection and mapping

7. **My Events Screen**
   - Students: List of registered events
   - Organizers: List of created events with participant counts
   - Event status indicators
   - Quick action buttons

8. **Profile Screen**
   - User information display and editing
   - College ID and contact details
   - Notification preferences
   - Theme selection
   - Logout functionality

## User Workflows

### Organizer Workflow
```
Login → Dashboard → Create Event → Fill Event Form → Save Event
                                        ↓
                            Event appears in public event list
                                        ↓
                            Students discover and register for event
                                        ↓
                            Organizer monitors registrations and analytics
                                        ↓
                            Event execution with QR code check-in
```

### Student Workflow
```
Login → Browse Event List → Apply Filters/Search → View Event Details
                                                            ↓
                                                    Register for Event
                                                            ↓
                                                    Receive Confirmation
                                                            ↓
                                                    Get Reminder Notifications
                                                            ↓
                                                    Attend Event (QR Check-in)
```

## Technical Implementation

### Technology Stack
- **Platform**: Android (Minimum API Level 21, Target API Level 33+)
- **Programming Languages**: Java/Kotlin
- **UI Framework**: XML layouts with Material Design Components
- **Architecture Pattern**: MVVM (Model-View-ViewModel)
- **Database**: 
  - Firebase Firestore (Cloud database)
  - SQLite (Local database for offline mode)
- **Authentication**: Firebase Authentication
- **Cloud Messaging**: Firebase Cloud Messaging (FCM)
- **Image Loading**: Glide or Picasso
- **Development Environment**: Android Studio

## Event Categories

The application supports multiple event categories:
- Cultural Events (Music, Dance, Drama, Art)
- Technical Workshops (Programming, AI/ML, Web Development)
- Management Seminars (Leadership, Entrepreneurship, Finance)
- Sports Competitions (Indoor, Outdoor, E-sports)
- Academic Conferences (Research, Symposiums, Guest Lectures)
- Social Activities (Community Service, Networking, Fun Events)

## Installation and Setup

### Prerequisites
- Android Studio (Latest version recommended)
- Android SDK (API Level 21 or higher)
- Firebase project setup (for cloud features)
- Google Services configuration

### Setup Instructions
1. Clone the repository to your local machine
2. Open the project in Android Studio
3. Configure Firebase services:
   - Create a new Firebase project
   - Add Android app to Firebase project
   - Download and add `google-services.json` to the app directory
   - Enable Authentication, Firestore, and Cloud Messaging
4. Sync project with Gradle files
5. Build and run the application on device/emulator

### Configuration
- Update package name in `build.gradle` and Firebase console
- Configure notification channels for different Android versions
- Set up proper permissions in `AndroidManifest.xml`
- Configure ProGuard rules for release builds

## Key Performance Metrics

### Application Metrics
- Event creation and management efficiency
- User engagement and session duration
- Registration conversion rates
- Push notification open rates
- App crash rates and performance monitoring

### Business Metrics
- Total events created per semester
- Average registrations per event
- Student participation rates
- Organizer satisfaction scores
- Event attendance tracking accuracy

## Future Enhancements

- Integration with college calendar systems
- Analytics dashboard with charts and graphs
- Social sharing and event promotion features
- Event feedback and rating system
- Integration with college LMS platforms
- Automated event recommendations based on user preferences
- Video streaming integration for virtual events
- Payment gateway integration for paid events
- Advanced reporting and export functionality

## Technical Improvements

- Migration to Jetpack Compose for modern UI
- Implementation of Clean Architecture
- Enhanced offline capabilities with Room database
- Performance optimization and caching strategies
- Automated testing implementation (Unit, Integration, UI)
- CI/CD pipeline setup for automated deployments

## Target Audience

### Primary Users
- **Students**: Discover, register, and participate in college events
- **Event Organizers**: Create, manage, and promote campus events efficiently
- **College Administration**: Oversee and coordinate all campus activities

### User Benefits
- Centralized event management platform
- Improved communication between organizers and students
- Enhanced event discovery and participation
- Streamlined registration and attendance tracking
- Data-driven insights for better event planning

## Support and Maintenance

### Version Control
- Git-based version control with feature branching
- Regular releases with semantic versioning
- Comprehensive commit messages and documentation

### Testing Strategy
- Unit testing for business logic
- Integration testing for database operations
- UI testing for critical user flows
- Performance testing for scalability

### Deployment
- Google Play Store distribution
- Beta testing program for early feedback
- Staged rollout for major updates
- Crash reporting and analytics integration

---

This College Event Manager App represents a comprehensive solution for enhancing student engagement and streamlining event management processes through technology.
