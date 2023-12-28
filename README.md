# Standalone Database

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Overview

The Standalone Database is a simple SQLite-based database designed for [Your Application Name]. It provides storage for events and invitations in a standalone manner.

## Features

- **Events Table:** Stores information about events.
- **Invitations Table:** Manages invitations for each event.

## Getting Started

### Download

Clone this repository or download the ZIP file.

### Integration

1. Copy the `StandaloneDatabaseHelper.kt` file to your project's package.
2. Update the `Event` and `EventsInvitation` data models based on your application's requirements.
3. Copy the `DatabaseManager.kt` file to your project's package.

### Usage

In your activity or fragment, create an instance of `DatabaseManager` and use it to insert, retrieve, or manage events.

```kotlin
val databaseManager = DatabaseManager(context)

// Example: Insert a new event
val newEvent = Event(
    // provide event details
)
databaseManager.insertEvent(newEvent)

// Example: Retrieve all events
val events = databaseManager.getEvents()
Data Structure
Events Table Columns
id
user_id
cc_status
room_alhub
room_type
host_id
scheduled_time
description
institution
security_token
room_status
modified
is_host
EventsInvitation Table Columns
id
event_id
host_id
participant_id
participant_name
accepted
