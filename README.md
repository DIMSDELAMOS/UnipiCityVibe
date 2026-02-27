# 🏛️ UnipiCityVibe 

**Smart City Event Manager & Booking App** An Android application designed to help citizens and tourists in Piraeus discover local cultural events, book tickets, and receive real-time location-based notifications.

## ✨ Key Features

* **User Authentication:** Secure registration and login powered by Firebase Authentication.
* **Real-Time Event Catalog:** Fetches a dynamic list of city events directly from a Firebase Realtime Database.
* **Ticket Booking System:** Users can reserve spots for events, with transaction data and timestamps saved securely to the cloud.
* **Advanced Geofencing (Location Services):** Tracks user location in the background. If a user enters a 200-meter radius of an event venue, the app triggers a native system notification ("Event Nearby!").
* **Multilingual UI:** Fully localized application supporting **English, Greek, and French**, adapting automatically to the device's system settings.
* **User Preferences:** Includes a Settings screen with a "Dark Mode" toggle, persisting user choices via `SharedPreferences`.

## 🛠️ Tech Stack

* **Language:** Kotlin
* **IDE:** Android Studio
* **Backend / Database:** Firebase Authentication, Firebase Realtime Database
* **Location API:** Google Play Services (GeofencingClient)
* **UI Components:** RecyclerView, ConstraintLayout, Material Components


## 🧪 How to Test the Geofencing Feature (For Reviewers)

Because the app relies on physical movement to trigger notifications, use the Android Emulator's location controls to simulate entry:

1. Run the app on the Android Emulator and log in.
2. Grant "While using the app" or "All the time" location permissions when prompted.
3. Open the Emulator's extended controls (`...` menu) -> **Location**.
4. Set the location far away (e.g., `0, 0`).
5. Change the coordinates to match an event venue in the database (e.g., Latitude: `37.9429`, Longitude: `23.6468`).
6. Click **Set Location**.
7. A background notification stating **"Event Nearby!"** will appear in the system tray within a few seconds.

## ⚙️ Setup & Installation

1. Clone this repository.
2. Open the project in Android Studio.
3. Add your own `google-services.json` file from Firebase to the `app/` directory.
4. Build and Run on an emulator or physical device running Android API 24+.
