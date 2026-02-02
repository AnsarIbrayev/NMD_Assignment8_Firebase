# NMD Assignment 8 – Firebase Integration (WeatherApp)
# Ibrayev Ansar
# SE-2424
## Project Overview
This project is an extension of the WeatherApp developed for the NMD course.  
The goal of Assignment 8 is to integrate Firebase services into an Android application.

Firebase Authentication and Firebase Realtime Database are used to store and manage user data in real time.

---

## Technologies Used
- Kotlin
- Android Jetpack Compose
- Firebase Authentication (Anonymous)
- Firebase Realtime Database
- Git & GitHub

---

## Firebase Configuration
1. A Firebase project was created in Firebase Console.
2. An Android app with package name `com.example.weatherapp` was registered.
3. The `google-services.json` file was added to the `app/` directory.
4. Firebase dependencies and Google Services plugin were configured in Gradle.
5. Anonymous Authentication was enabled.
6. Realtime Database was created with custom security rules.

---

## Security Rules
```json
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "auth != null && auth.uid == $uid",
        ".write": "auth != null && auth.uid == $uid"
      }
    }
  }
}
Application Features
Favorites & Notes
The application includes a new feature called Favorites & Notes, which allows users to manage favorite cities.

Implemented functionality:

Create – add a favorite city with a note

Read – load favorites from Firebase

Update – edit an existing favorite

Delete – remove a favorite item

All changes are synchronized in real time using Firebase Realtime Database listeners.

Data Structure
Data is stored in Firebase using the following structure:

users/{uid}/favorites/{favoriteId}
Each favorite item contains:

id

title

note

createdAt

createdBy