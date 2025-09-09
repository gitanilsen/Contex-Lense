📸 Context Lens - AI Visual Explainer
Context Lens is a responsive web application that uses your device's camera and the power of the Google Gemini API to identify and explain anything you point it at. Turn your world into an interactive encyclopedia!

🌟 About The Project
Have you ever looked at a landmark, a plant, or a piece of art and wished you could instantly know its story? Context Lens bridges that gap. This application captures a live image from your camera, sends it to Google's advanced multimodal AI, and displays a rich, detailed explanation in real-time. It's a simple yet powerful demonstration of the capabilities of modern generative AI.

This project was built to be:

Simple: Contained in a single HTML file with no complex dependencies or build steps.

Modern: Utilizes a clean, responsive UI built with Tailwind CSS.

Powerful: Directly integrates with the Google Gemini API for state-of-the-art visual analysis.

✨ Features
Real-Time Camera Access: Uses the rear-facing camera (environment) on mobile devices for easy pointing.

AI-Powered Analysis: Leverages the gemini-2.5-flash-preview-05-20 model for fast and accurate image understanding.

Responsive Design: A beautiful and intuitive interface that works seamlessly on desktop and mobile browsers.

Loading & Error States: Clear UI feedback while the AI is processing or if an error occurs.

Zero Dependencies: Runs directly in the browser with no installation required, using only a CDN for Tailwind CSS.

🛠️ Technology Stack
Frontend: HTML5, CSS3, JavaScript (ES6+)

Styling: Tailwind CSS

Core AI: Google Gemini API

⚙️ How It Works
The application's logic is straightforward:

The browser's navigator.mediaDevices.getUserMedia API is used to access the device's video camera.

The live video is streamed to an HTML <video> element.

When the "Analyze" button is clicked, a single frame from the video stream is drawn onto a hidden <canvas> element.

The canvas image is converted to a Base64-encoded JPEG string.

A fetch request is made to the Gemini API, sending the image data along with a carefully crafted prompt.

The AI's text response is parsed and displayed in the explanation panel.

🚀 Getting Started
To get a local copy up and running, follow these simple steps.

Prerequisites
You only need a modern web browser and a free Google Gemini API key.

Installation & Setup
Clone the repository (or download the context-lens.html file):

git clone [https://github.com/your-username/context-lens.git](https://github.com/your-username/context-lens.git)

Get your Free Gemini API Key:

Navigate to Google AI Studio.

Sign in and click "Get API key" > "Create API key in new project".

Copy the generated key to your clipboard.

Add the API Key to the App:

Open context-lens.html in your favorite code editor.

Find the API_KEY constant within the <script> tag.

Replace 'YOUR_API_KEY_HERE' with the key you just copied.

// --- IMPORTANT: PASTE YOUR GEMINI API KEY HERE ---
const API_KEY = 'AIzaSyB...your_actual_key...Q3oA2s'; 
// --------------------------------------------------

Run the Application:

Open the modified context-lens.html file directly in your web browser.

Grant the requested camera permissions, and you're ready to start exploring!

Enjoy using Context Lens!
