# skincare-agent
A modular, Firestore-powered user profile system built for personalized skincare recommendations using Google ADK Agents.
This project forms the memory and personalization layer for a full multi-agent skincare ecosystem — including intake, routine generation, product analysis, and safety workflows.

Overview
Skincare routines must be personalized. Most apps give generic suggestions that don’t evolve with the user’s skin changes, habits, or concerns.
This project solves that by storing a structured skincare user profile and exposing it to agents that intelligently generate AM/PM routines, evaluate products, and provide personalized guidance.
At the center is the UserProfileDB — a simple, robust Firestore wrapper that supports nested updates and integrates directly with Google ADK’s agent orchestrator.

Core Features
-- Persistent User Profiles
Store user skin type, concerns, allergies, lifestyle, habits, and product history.
-- Field-Level Updates
Update nested fields with dot notation:
update_field("u1", "skin.type", "oily")
-- Modular Architecture
Acts as the memory backend for intake agents, routine generator agents, and product analysis agents.
-- Firestore-Backed
Designed for scalability and real-time data retrieval.
-- ADK-Compatible
Works seamlessly with Google ADK workflows using InMemoryRunner or production orchestrators.

Architecture
User → Intake Agent → UserProfileDB → Firestore

