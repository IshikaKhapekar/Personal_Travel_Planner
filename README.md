# Personal Travel Planner Agent

## Overview

The Personal Travel Planner Agent is an AI-powered travel planning agent built using Google ADK and Gemini.

It takes a user's travel request and generates a simple, practical, and budget-conscious travel plan based on the destination, duration, budget, and interests provided by the user.

## Features

- Understands natural-language travel requests
- Identifies destination, duration, budget, and interests
- Recommends suitable places and activities
- Creates a day-wise itinerary
- Estimates the overall travel budget
- Provides a category-wise budget breakdown
- Compares the estimated cost with the user's budget
- Provides a final structured travel plan

## Technology Used

- Python
- Google ADK (Agent Development Kit)
- Google Gemini

## Project Structure

Personal_Travel_Planner/
│
├── README.md
├── requirements.txt
│
└── travel_planner/
    ├── agent.py
    ├── __init__.py
    └── .env

## How It Works

The user provides a travel request containing details such as destination, number of days, budget, and interests.

The agent then:

1. Understands the user's requirements.
2. Recommends suitable places and activities.
3. Estimates the travel budget.
4. Compares the estimated cost with the given budget.
5. Generates a day-wise itinerary.

## Example Conversations

### Conversation 1 - Jaipur

User:

I want to visit Jaipur for 3 days with a budget of ₹15,000. I like history and local food.

Agent:

The agent generates a 3-day itinerary focused on historical places and local food, recommends suitable attractions, provides an estimated budget, and compares the estimated cost with the user's budget.

### Conversation 2 - Goa

User:

I want to visit Goa for 4 days with a budget of ₹25,000. I enjoy beaches, adventure activities, and local seafood.

Agent:

The agent generates a 4-day itinerary focused on beaches, adventure activities, and local seafood, along with recommended places and an estimated budget.

### Conversation 3 - Delhi

User:

I want to visit Delhi for 2 days with a budget of ₹10,000. I am interested in history and street food.

Agent:

The agent generates a 2-day itinerary focused on historical attractions and street food, along with recommended places and an estimated budget.

## Example Input

I want to visit Jaipur for 3 days with a budget of ₹15,000. I like history and local food.

## Expected Output

The agent provides:

- Trip Summary
- Recommended Places
- Estimated Budget
- Budget Status
- Day-wise Itinerary

The day-wise itinerary is organized into morning, afternoon, and evening activities.

## Note

The budget and itinerary provided by the agent are estimates and may vary depending on actual prices, availability, and travel conditions.