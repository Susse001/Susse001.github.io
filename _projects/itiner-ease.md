---
layout: default
title: Itiner-ease
excerpt: AI-powered itinerary creation and recommendation application.
tech:
  - Laravel
  - OpenAI
  - CSV
  - TALL Stack
---

## Itiner-ease

AI-powered itinerary creation and recommendation application that builds personalized travel plans based on user preferences.

---

## Project Scope

Itiner-ease is designed to reduce the friction of travel planning by automating itinerary creation. Instead of manually researching destinations, activities, and dining options, users define their interests once and receive a tailored itinerary aligned with those preferences.

The system emphasizes:
- User-driven personalization
- Automated itinerary generation
- Transparent, preference-based recommendations

---

## User Flow Overview

The application follows a three-step user flow:

1. Create a Personalization Profile  
2. Generate an Itinerary  
3. Review and Customize Selections  

Each step builds on the previous one to ensure recommendations align with user interests while remaining flexible.

---

## 1. Personalization Profile

Users begin by creating a Personalization Profile, where they define their travel preferences. These preferences are used throughout the application to guide itinerary recommendations.

Preferences include (but are not limited to):
- Activity types (e.g., museums, nightlife, outdoors)
- Dining preferences
- Travel pace
- Group type (solo, couple, family)
- Budget sensitivity

This profile serves as the foundation for all itinerary generation logic.

![Personalization Profile Example](/assets/itiner-ease/preferences.PNG)

---

## 2. Itinerary Generation

Once a profile is created, the user can generate an itinerary for a selected destination.  
The system processes personalization data and automatically builds a multi-day itinerary aligned with the user’s stated interests.

Each itinerary includes:
- Recommended activities
- Suggested locations
- Dining options matched to preferences

The generated itinerary provides a structured starting point that users can further refine.

![Generated Itinerary Example](/assets/itiner-ease/itinerary1.PNG)

---

## 3. Review and Customize Selections

After an itinerary is generated, users can review individual itinerary items and make changes as needed.

At this stage, users can:
- Modify or remove recommended activities
- Design and add their own custom activities
- Collaborate with a local expert — a user with local experience who can provide informed recommendations and make targeted modifications

Each itinerary item includes preference tags that reflect how the recommendation aligns with the user’s personalization profile, helping users understand and validate the selections made by the system.

![Itinerary Item with Tags](/assets/itiner-ease/itinerary_item.PNG)

---

## My Contributions

My primary contributions focused on the **data pipeline, personalization logic, and system coordination**, including:

- CSV-based data ingestion and normalization for locations and activities
- Automated itinerary generation driven by personalization profiles
- Tag-based matching between user preferences and itinerary items
- Support for user-defined activities and expert-driven recommendations
- Project coordination and feature-level task management
- Integration of the OpenAI API to assist with data preprocessing and recommendation support

---

## Tech Stack

- **Backend:** Laravel (TALL stack)
- **Data Processing:** CSV Reader / Normalization Pipelines
- **AI Integration:** OpenAI API
- **Frontend:** Blade templates with Tailwind CSS


[View on GitHub](https://github.com/jandraarias/f25-Copper)
