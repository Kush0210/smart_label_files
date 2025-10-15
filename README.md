# Smart Label: Model-Assisted Human-in-the-Loop Labeling

An intelligent web application built with Flask and PyTorch that uses a dual-model ensemble (ResNet-18 & MobileNetV2) to assist hematopathologists in classifying and curating blood cell images. The system enables efficient expert review and streamlines digital curation.

## Features

- **Secure User Authentication:** Multi-user support with registration and login (Flask-Login).
- **Patient-Centric Workflow:** Process entire folders of images for a specific patient.
- **Dual-Model Ensemble:** Uses both ResNet-18 and MobileNetV2 for robust predictions.
- **Intelligent HITL Trigger:** Automatically flags images for expert review based on model disagreement or low-confidence agreement.
- **Batch Curation Tools:** Efficiently apply labels to multiple images at once.
- **PDF Report Generation:** Creates a professional, downloadable PDF summary for each patient session.
- **Persistent History:** Each user can view a history of all patient reports they have curated.

## Tech Stack

- **Backend:** Flask, Flask-SQLAlchemy, Flask-Login
- **Database:** SQLite (can be easily switched to PostgreSQL)
- **Deep Learning:** PyTorch
- **AI Models:** ResNet-18, MobileNetV2
- **Frontend:** JavaScript (AJAX), HTML5, CSS3
- **PDF Generation:** FPDF2
- **Image Processing:** OpenCV, Pillow

## Setup & Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Kushal-LTI/smart_label.git
    cd smart_label
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    # For Windows
    python -m venv env
    .\env\Scripts\activate

    # For macOS/Linux
    python3 -m venv env
    source env/bin/activate
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the application:**
    ```bash
    python app.py
    ```
    The application will create the `database.db` file automatically on first run and will be available at `http://127.0.0.1:5000`.

## Usage

1.  Register a new user account.
2.  Log in with your credentials.
3.  On the Curation page, enter a patient's name.
4.  Use the "Select Images" or "Select Folder" button to upload cell images.
5.  Click "Analyze & Curate" to begin the process.
6.  Review the AI's suggestions, correcting any labels as needed using the dropdowns.
7.  Once finished, click "Finish & Save Report".
8.  Download the generated PDF report or view the session in your "Patient History".
