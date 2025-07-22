# AI Math Solver

This project is an interactive application that allows users to draw math expressions in the air using hand gestures, and then solve them using Google's Gemini AI. It combines computer vision, real-time hand tracking, and generative AI to create a seamless, touchless math-solving experience.

## Overview

The system captures hand gestures from a webcam using OpenCV and the `cvzone` hand tracking module. When the user draws a math expression with their index finger, it is displayed in real time on a virtual canvas. Once the gesture-based input is completed, the drawn image is processed and sent to Google Gemini for interpretation and solution. The solution is displayed on the right panel using Streamlit.

## Features

- Real-time webcam-based hand gesture tracking  
- Index-finger drawing on a virtual canvas  
- Gesture-based canvas clearing and submission  
- Integration with Gemini AI for solving handwritten math problems  
- Streamlit-based user interface for a smooth user experience  

## Technologies Used

- Python  
- OpenCV  
- cvzone  
- Streamlit  
- google-generativeai (Gemini API client)  
- Pillow (PIL)

## Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/math-gestures-ai.git
cd math-gestures-ai
```

2. **Create a virtual environment (optional)**

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Set your Google Gemini API key**

Open the Python file and replace the placeholder with your API key:

```python
genai.configure(api_key="YOUR_API_KEY")
```

You can generate an API key from: https://aistudio.google.com/app/apikey

## Running the Application

To launch the app:

```bash
streamlit run app.py
```

The application will open in your browser. You will see the live webcam feed and output from the AI on the interface.

## System Requirements

- Python 3.7 to 3.11  
- Webcam  
- Internet connection (for Gemini API)

## Usage

- Raise only your index finger to draw.  
- Raise only your thumb to clear the canvas.  
- Raise all fingers except the pinky to submit the canvas for solving.

## License
This project is licensed under the MIT License.
