# Personal Travel Planner Agent

## Overview

The **Personal Travel Planner Agent** is an AI-powered travel planning agent built using **Google ADK and Gemini**.

It takes a user's travel request and generates a practical, budget-conscious, day-wise travel plan based on the **destination, duration, budget, and interests** provided.


## Key Features

- Understands natural-language travel requests
- Identifies destination, duration, budget, and interests
- Recommends suitable places and activities
- Creates a day-wise itinerary
- Estimates the overall travel budget
- Provides a category-wise budget breakdown
- Compares estimated cost with the user's budget
- Provides a structured final travel plan
  

## Security & Guardrails

The agent includes multiple security layers to make it safer for real-world use:

| Guardrail | Purpose |
|---|---|
| **Input Safety** | Blocks harmful, illegal, or malicious requests |
| **Prompt Injection Protection** | Blocks attempts to override safety rules or reveal internal instructions |
| **Travel Domain Control** | Keeps the agent focused on travel-related requests |
| **PII Protection** | Blocks sensitive information such as passwords, API keys, financial details, government IDs, and exact home addresses |
| **Output Safety** | Checks generated responses for clearly unsafe or harmful content |
| **Safety Instructions** | Prevents exposure of credentials, internal instructions, and unnecessary personal information |

The guardrails are implemented at both the **input and output stages** using Google ADK callbacks.


## Technology Used

- Python
- Google ADK (Agent Development Kit)
- Google Gemini

## Project Structure

```text
Personal_Travel_Planner/
│
├── agent.py
├── requirements.txt
├── README.md
│
├── examples/
│   ├── conversation_1_jaipur.txt
│   ├── conversation_2_goa.txt
│   └── conversation_3_delhi.txt
│
└── screenshots/
    ├── jaipur_1.png
    ├── jaipur_2.png
    ├── goa_1.png
    ├── goa_2.png
    ├── delhi_1.png
    └── delhi_2.png
```

## How It Works

1. User provides a travel request.
2. Input guardrails check the request for unsafe, malicious, prompt-injection, privacy, and scope-related issues.
3. Valid travel requests are processed by the Gemini-powered agent.
4. The agent recommends places and activities.
5. The estimated budget is calculated and compared with the user's budget.
6. A day-wise itinerary is generated.
7. The output is checked by the output safety guardrail before being returned to the user.
   

## Security Tests Performed

The implemented guardrails were tested with:

- ✅ Normal travel request
- ✅ Harmful request
- ✅ Prompt injection attempt
- ✅ Off-topic / malicious request
- ✅ Sensitive personal information / exact address

The unsafe requests were blocked or redirected to safe travel assistance.


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

## Example Conversation Screenshots

### 1: I want to visit Jaipur for 3 days with a budget of ₹15,000. I like history and local food.

<img width="1912" height="955" alt="Screenshot 2026-10-05 174739" src="https://github.com/user-attachments/assets/57480316-a515-475b-af93-1ff22b72303b" />


<img width="1898" height="842" alt="Screenshot 2026-10-05 174825" src="https://github.com/user-attachments/assets/593dc863-5b9f-4d1e-8e05-586d59652cbb" />



### 2: I want to visit Goa for 4 days with a budget of ₹25,000. I enjoy beaches, adventure activities, and local seafood.

<img width="1917" height="847" alt="Screenshot 2026-10-05 181949" src="https://github.com/user-attachments/assets/305a0152-1251-481f-b634-b8fca1858320" />


<img width="1917" height="842" alt="Screenshot 2026-10-05 182000" src="https://github.com/user-attachments/assets/db772d69-da3e-4a6c-84a2-071c4bdb6a3f" />


<img width="1917" height="847" alt="Screenshot 2026-10-05 182009" src="https://github.com/user-attachments/assets/a48066d0-5c04-477b-9b52-9df2a877c5c5" />



### 3: I want to visit Delhi for 2 days with a budget of ₹10,000. I am interested in history and street food.

<img width="1917" height="845" alt="Screenshot 2026-10-05 182107" src="https://github.com/user-attachments/assets/6fc5a914-3129-41ae-a08a-50435106b2d3" />


<img width="1917" height="848" alt="Screenshot 2026-10-05 182129" src="https://github.com/user-attachments/assets/728aca5e-9046-40d8-967a-9c7774b4942a" />


## Note

The budget and itinerary provided by the agent are estimates and may vary depending on actual prices, availability, and travel conditions.
