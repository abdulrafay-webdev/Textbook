# Physical AI & Humanoid Robotics Textbook

This repository contains an AI-native technical textbook for "Physical AI & Humanoid Robotics," built using Docusaurus. It also includes a Retrieval-Augmented Generation (RAG) chatbot capable of answering questions based on the book's content.

## Project Structure

-   `textbook/`: The Docusaurus project for the textbook.
-   `backend/`: A FastAPI application for the RAG chatbot's backend.

## Getting Started

### Prerequisites

-   Node.js (version 18.x or later)
-   npm (comes with Node.js)
-   Python (version 3.11 or later)
-   pip (comes with Python)

### 1. Clone the repository

```bash
git clone https://github.com/abdulrafay-webdev/Textbook.git
cd Textbook
```

### 2. Set up the Docusaurus Frontend (Textbook)

Navigate to the `textbook` directory and install dependencies:

```bash
cd textbook
npm install
```

To run the Docusaurus development server locally:

```bash
npm start
```

This will open the textbook in your browser at `http://localhost:3000`.

### 3. Set up the FastAPI Backend (RAG Chatbot)

Open a new terminal and navigate to the `backend` directory.

```bash
cd backend
```

Create a Python virtual environment and install dependencies:

```bash
python -m venv venv
./venv/Scripts/activate # On Windows
# source venv/bin/activate # On macOS/Linux
pip install -r requirements.txt
```

Run the FastAPI application:

```bash
uvicorn app.main:app --reload
```

The FastAPI application will be available at `http://localhost:8000`.

## Deployment to Vercel

This project is configured for easy deployment to Vercel.

1.  **Sign up for a Vercel account:**
    *   Go to [https://vercel.com/signup](https://vercel.com/signup) and create an account. It's recommended to sign up with your GitHub account.

2.  **Import your Project:**
    *   From your Vercel dashboard, click on "Add New..." -> "Project".
    *   Under "Import Git Repository," select your `Textbook` repository from GitHub.

3.  **Configure the Project:**
    *   Vercel will automatically detect that you are deploying a Docusaurus project.
    *   The "Framework Preset" should be set to "Docusaurus".
    *   The "Root Directory" should be set to `textbook`.
    *   Click "Deploy".

4.  **Backend Deployment (Optional):**
    *   The FastAPI backend is not automatically deployed with the Docusaurus frontend. To deploy the backend, you would need to set up a separate Vercel project pointing to the `backend` directory, or use another hosting service.

Vercel will build and deploy your Docusaurus site, and provide you with a live URL.
