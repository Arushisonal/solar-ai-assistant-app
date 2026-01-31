
Design and implement an AI-powered rooftop analysis tool that uses satellite imagery to assess solar installation potential. This project evaluates your ability to integrate multiple AI services while solving a critical solar industry challenge.

Project Goal
Create an intelligent system that analyses any rooftop from satellite imagery and provides accurate solar potential assessments, installation recommendations, and ROI estimates for both homeowners and solar professionals.

Required Knowledge Areas
•	Solar Panel Technology: Types, efficiency, specifications
•	Installation Processes: Mounting, electrical, permits
•	Maintenance Requirements: Monitoring, cleaning, warranties
•	Cost & ROI Analysis: Pricing, incentives, payback periods
•	Industry Regulations: Codes, net metering, safety standards
•	Market Trends: Technology advances, adoption rates

Technical Assessment Areas (80%)
AI Implementation (40%)
•	LLM Integration: Vision AI for image analysis
•	Prompt Engineering: Structured output extraction
•	Context Management: Multi-source data handling
•	Response Accuracy: Validation and confidence scoring






![image](https://github.com/user-attachments/assets/3942f137-a479-472c-b1aa-a9764e643706)
Project Directory Structure (newproject/)
/Users/arushisonal/Downloads/newproject
│
├── backend/                           #  FastAPI backend
│   ├── main.py                        # Main backend logic, API routes
│   ├── requirements.txt               # Python dependencies
│   ├── .env                           # Contains OPENWEATHERMAP_API_KEY
│   ├── utils/
│   │   ├── image_processing.py        # (optional) Helper for OpenCV, etc.
│   │   └── solar_calc.py              # (optional) Functions like ROI, area
│   └── venv/                          # Python virtual environment
│
├── frontend/                          # React frontend
│   ├── src/
│   │   ├── App.tsx                    # Main React component
│   │   ├── index.tsx                  # React entry point
│   │   ├── api/                       # Axios API calls
│   │   │   └── backend.ts             # API interaction code
│   │   └── components/                # Reusable UI components (Dropzone, ResultCard)
│   ├── public/
│   │   └── index.html                 # Static template
│   ├── package.json                   # NPM dependencies
│   ├── package-lock.json              # Locked package versions
│   └── tsconfig.json                  # TypeScript configuration
│
├── docker-compose.yml                 #  Run backend & frontend together
├── Dockerfile                         # Build single-container image
├── nginx.conf                         # Config for Nginx server
│
├── docs/                              #  Documentation
│   ├── system_architecture.md         # (optional) Architecture diagram
│   ├── api_endpoints.md               # (optional) API structure
│   └── future_features.md             # (optional) Ideas & improvements
│
├── README.md                          #  Project overview & setup instructions
├── LICENSE                            # Project license (MIT, Apache, etc.)
└── .gitignore                         # (optional) Files/folders to ignore in Git





WHY Use Each Folder and File

📁 /backend/ — Why?
This folder contains your FastAPI backend, which:

Receives the image from the frontend
Processes it (e.g., using OpenCV or AI models)
Uses APIs like OpenWeatherMap to calculate solar potential
Sends the result (ROI, panel count, etc.) back to the frontend

🔹 Why main.py?
Main entry point where you define your API (/analyze-rooftop)
Calls image analysis and ROI functions
Acts as the controller of your backend logic

🔹 Why .env?

Stores sensitive keys like OPENWEATHERMAP_API_KEY securely
Keeps credentials separate from your code
🔹 Why requirements.txt?

Lists all Python libraries (fastapi, uvicorn, opencv-python, etc.)
Makes setup easy: just run pip install -r requirements.txt
🔹 Why venv/?

A virtual environment keeps your project’s dependencies isolated
Avoids breaking global Python packages on your system

📁 /frontend/ — Why?
This folder contains your React frontend, which:

Lets users upload images
Sends them to the backend via API
Displays results like solar area, savings, and ROI

🔹 Why App.tsx?

It’s the main UI logic of your React app
Handles image upload, fetches backend results, and shows them

🔹 Why api/backend.ts?

Centralizes all API calls using Axios
Makes code cleaner and easier to maintain
🔹 Why components/?

Holds reusable UI elements like:
Image uploader
Result card
Loading spinner

🔹 Why package.json?

Lists frontend dependencies (React, Axios, Material UI, etc.)
Defines scripts like npm start to run the app
🐳 docker-compose.yml — Why?
Makes it easy to run both frontend and backend together
You can start your entire app using just:
docker-compose up

🐳 Dockerfile & nginx.conf — Why?
Build a single Docker container to deploy your full app
Useful for Hugging Face Spaces, Heroku, Render, etc.
Nginx serves frontend & routes API requests to backend

📁 docs/ — Why?
Store developer notes, architecture diagrams, and future ideas
Helps new team members understand your project

📄 README.md — Why?
Gives users and collaborators:
Setup instructions
Project summary
How to run and use the app

📄 LICENSE — Why?
Makes your code legally reusable
Common licenses: MIT, Apache 2.0
📄 .gitignore — Why?
Tells Git to ignore sensitive or unnecessary files like:
venv/
.env
node_modules/





Terminal 1: For the Backend
Navigate to your backend directory
cd /Users/arushisonal/Downloads/newproject/backend
Activate your Python virtual environment:
 source venv/bin/activate
 Make sure you see (venv) at the beginning of your terminal prompt).
Start the FastAPI backend server on port 8003:
   uvicorn main:app --reload --port 8003
   his terminal will show backend logs and should indicate that Uvicorn is running on http://127.0.0.1:8003 or http://localhost:8003. Keep this terminal open and running.
Terminal 2: For the Frontend
Navigate to your frontend directory:
  cd /Users/arushisonal/Downloads/newproject/frontend
  Start the React frontend development server:
  npm start



