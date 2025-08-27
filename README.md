# Americana Geofence CLI

A simple Java command-line tool to check if a given GPS coordinate is within a 300-meter radius of The Americana at Brand in Glendale, CA.

## Prerequisites

You must have a **Java Development Kit (JDK)** installed on your system to compile and run this application.

## How to Use

Follow these steps from your terminal.

### 1. Compile the Application

Navigate to the project's root directory and compile the `.java` source file into Java bytecode.

```bash
javac AmericanaGeofence.java
2. Run the Application
Execute the compiled code by providing a latitude and longitude as command-line arguments.

Bash

java AmericanaGeofence <latitude> <longitude>
Examples
Check a location inside the geofence:

Bash

java AmericanaGeofence 34.1465 -118.2558
Check a location outside the geofence:

Bash

java AmericanaGeofence 34.1808 -118.3090

**For Android:** You'll build the app in **Kotlin** (or Java) using Android Studio. Instead of taking command-line arguments, you'll use Android's native **`GeofencingClient` API**. This is a highly efficient system that lets your app:
    1.  Register the Americana's coordinates and radius with the operating system.
    2.  Let Android monitor the user's location in the background with very little battery drain.
    3.  Receive a notification automatically when the device enters or exits that defined "fence."
    4.  Your app would then trigger a custom push notification to the user.

* **For iOS:** The process is conceptually the same, but you would write the application in **Swift** using Xcode. You'd use Apple's **Core Location** framework, which has its own powerful geofencing and region monitoring capabilities to achieve the same result.
