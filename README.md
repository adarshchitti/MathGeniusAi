# MathGeniusAi

MathGeniusAi is an AI-powered web application that analyzes math problems from text or images, generates structured question templates, estimates the grade level and topic, and allows users to generate similar questions for practice. It leverages Google Gemini for AI understanding and Tesseract.js for OCR (optical character recognition) on images.

---

## Features

- **Input Flexibility:** Users can enter a math problem as text or upload/paste an image of the problem.
- **OCR Support:** Images are processed with OCR to extract math problems automatically.
- **AI-Powered Analysis:** Problems are sent to Google Gemini, which:
    - Generates a step-by-step solution template.
    - Estimates the topic and grade level.
    - Provides a "blueprint" for generating similar problems.
- **Generate Similar Problems:** Users can create new, similar math questions based on the AI-generated blueprint.
- **Feedback:** Rate templates and leave feedback to improve future templates.
- **Modern UI:** Built with React, Wouter (routing), TanStack Query, Tailwind CSS, and shadcn/ui components.

---

## Video Demo

[*A sample demo video should show:*
- Typing or uploading a math problem.
- Viewing the analyzed template, grade, topic.
- Generating a similar question.
- (Optional) Leaving feedback.

*(Replace the video link above after uploading your demo!)*](https://youtu.be/N8-I4XgODnQ)

---

## How It Works

### 1. Problem Input

- **Text:** Type or paste your math problem into the provided text area.
- **Image:** Upload or paste a math problem image (e.g., from a worksheet or textbook).
- The app uses OCR to extract the math problem from images automatically.

### 2. AI Processing

- The backend sends the problem (from text or OCR result) to Gemini.
- Gemini returns:
    - A step-by-step solution template.
    - The problem's estimated topic (e.g., algebra, geometry).
    - The estimated grade level (e.g., Grade 6).
    - A "blueprint" for generating similar problems.

### 3. Results Page

- View the original problem, the AI-generated solution template, topic, grade, and extracted blueprint.
- If an image was uploaded, a preview is shown.

### 4. Generate Similar Questions

- Click "Generate Similar Question" to create a new math problem based on the same template and blueprint.
- The AI generates a new problem and a step-by-step solution.

---

## Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- A Gemini API key from Google


### Installation

```bash
git clone https://github.com/adarshchitti/MathGeniusAi.git
cd MathGeniusAi
```

#### 1. Setup Backend

- Set your `GEMINI_API_KEY` in the env file.

```bash
cd server
npm install
```

#### 2. Setup Frontend

```bash
cd ../client
npm install
```

#### 3. Run Development Server

```bash
# From the root folder
npm run dev
```

- This will start both the backend (API, OCR, Gemini integration) and the frontend (React app).
- App will be served at [http://localhost:5000](http://localhost:5000)

---

## Project Structure

```
MathGeniusAi/
│
├── client/         # React frontend (Vite, Tailwind, shadcn/ui)
├── server/         # Express backend, Gemini & Tesseract integration
├── shared/         # Shared TypeScript types and schema (zod/drizzle)
├── drizzle.config.ts # Drizzle ORM config
└── README.md
```

---

## Key Technologies

- **Frontend:** React, Vite, Wouter, TanStack Query, Tailwind CSS, shadcn/ui
- **Backend:** Express, Gemini AI, Tesseract.js, Drizzle ORM, Multer (for file uploads)
- **OCR:** Tesseract.js
- **AI:** Google Gemini (via API key)

---

## Environment Variables

- `GEMINI_API_KEY`: **Required**. Get from Google AI Studio.

---

## Example Usage

1. Start the server and visit [http://localhost:5000](http://localhost:5000).
2. Enter a math problem or upload an image.
3. View the analyzed template, topic, and grade.
4. Generate a similar question for more practice.

---

## License

MIT


## Authors

- [adarshchitti](https://github.com/adarshchitti)

---
