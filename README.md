# Assignment 2 - Traffic Racer Android Game

## Overview
**Traffic Racer** is an interactive, sensor-driven Android game developed as part of an academic assignment. The application challenges players to navigate a vehicle through a hazardous road, avoiding obstacles (stones) while collecting rewards (coins). It demonstrates the integration of hardware sensors, local data persistence, and Google Maps API into a cohesive mobile experience.

## Features

### 🎮 Immersive Gameplay
*   **Dynamic Obstacles:** Randomly generated stones fall down the lanes, requiring quick reflexes to avoid.
*   **Reward System:** Collect coins to increase your score.
*   **Life System:** Players start with three lives (hearts). Colliding with a stone costs a life and triggers a vibration and sound effect.

### 🕹️ Multiple Control Modes
*   **Sensor Mode:** Utilize the device's accelerometer to steer the vehicle by tilting.
*   **Button Mode:** Use on-screen arrows for precise control.

### ⚡ Adjustable Difficulty
*   **Speed Settings:** Choose between **Slow** and **Fast** modes to adjust the falling speed of obstacles.

### 🏆 Score Management & Location Tracking
*   **Top 10 Leaderboard:** View the highest scores achieved locally.
*   **Google Maps Integration:** Every high score is saved with the geographic location where it was achieved. Players can visualize their records on an interactive map.
*   **Persistence:** Scores and locations are saved using `SharedPreferences` and serialized via `Gson`.

## Technical Architecture

The project follows a modular structure to ensure maintainability and separation of concerns:

*   **Activities:**
    *   `MainActivity`: Handles the core game loop, collision detection, and UI updates.
    *   `ScoreMapActivity`: Integrates Google Maps to display score locations.
    *   `GameOver`: Summary screen displayed when lives are exhausted.
*   **Fragments:**
    *   `MapFragment`: Encapsulates the Google Map logic.
    *   `ScoreFragment`: Manages the display of the high-score list.
*   **Managers/Utilities:**
    *   `MoveDetector`: Abstracts sensor logic for tilt-based movement.
    *   `StoneManager` / `CoinManager`: Manage the lifecycle and positioning of game objects.
    *   `SharePreferencesManager`: Handles data storage and retrieval.
    *   `SoundCrash`: Manages audio feedback during gameplay events.

## Technologies Used
*   **Language:** Java
*   **UI Framework:** Material Design Components, Jetpack Compose (where applicable)
*   **Storage:** SharedPreferences with GSON
*   **Hardware:** Accelerometer Sensor, Vibrator Service
*   **APIs:** Google Maps SDK, Fused Location Provider
*   **Build System:** Gradle (Kotlin DSL)

## Getting Started

### Prerequisites
*   Android Studio Jellyfish or newer.
*   Android SDK 34 (UpsideDownCake).
*   Google Maps API Key (configured in `local.properties` or `AndroidManifest.xml`).

### Installation
1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/assignment2.git
    ```
2.  Open the project in Android Studio.
3.  Add your Google Maps API Key to the project.
4.  Sync Gradle and run the app on an emulator or physical device.

## Academic Context
This project was developed for the Android Development Course. It focuses on:
*   Activity and Fragment lifecycle management.
*   Custom `RecyclerView` adapters.
*   Sensor integration and real-time UI updates.
*   Asynchronous tasks using `Handler`.
*   Location-based services and third-party API integration.

---
*Created by Emily - Android Development Assignment 2*
