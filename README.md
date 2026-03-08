# FitBuddy AI - Project Workflow

### 1. Project Overview
**FitBuddy** is an AI-powered fitness plan generator designed to provide users with personalized workout routines based on their unique physical attributes and goals.

### 2. User Journey & Data Flow
The application follows a structured data pipeline to ensure security and efficiency:

* **Step 1: Client Input** – The user provides data (age, weight, goal, and equipment) via the frontend.
* **Step 2: FastAPI Backend** – The server receives the request and validates the input.
* **Step 3: Authentication** – The system securely retrieves the Gemini API key from a `.env` file.
* **Step 4: AI Processing** – A structured prompt is sent to the `gemini-1.5-flash` model for stable generation.
* **Step 5: Error Handling** – The workflow includes **Exponential Backoff** to manage rate limits (429 errors) and ensure high availability.
* **Step 6: Response Delivery** – The generated plan is parsed and sent back to the user as a JSON response.



### 3. Core Milestones
* **Milestone 1**: Architecture and Model Selection (Gemini Flash).
* **Milestone 2**: Core Functionalities Development.
* **Milestone 3**: `routes.py` implementation for API handling.
* **Milestone 4**: Frontend connection and user interface.
* **Milestone 5**: Testing and Deployment.

### 4. Technical Stack
* **Language**: Python
* **Framework**: FastAPI
* **AI Model**: Gemini 2.0/1.5 Flash
* **Environment Management**: python-dotenv (`.env`)