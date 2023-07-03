# StandupSync

StandupSync is a Python-based application that automates and enhances daily standup meetings. With real-time transcription and accurate speech-to-text conversion, teams can effortlessly generate meeting transcripts. The application supports multiple languages, including US English, Spanish, and regional Indic languages. StandupSync intelligently extracts insights, assigns action items, and provides weekly data analysis, improving efficiency and collaboration. Integrated with Google Calendar, it directly inputs meeting details and allows users to ask questions based on collected data. With its powerful features and user-friendly interface, StandupSync transforms standup meetings, saving time and enabling effective communication for teams.

## Track - LLM API Endpoint

## Problem Statement
- Lack of comprehensive software for tracking and analyzing Daily Stand-Up Meetings (DSMs).
- Challenges in improving collaboration and individual contributions without systematic DSM insights. 
- Difficulty in identifying areas of improvement and tracking bug origins. 
- Manual analysis of DSMs leading to inefficiency in resource utilization. 
- Limited ability to generate actionable insights and performance metrics from DSM discussions.
- Difficulty in tracking meeting insights and providing timely feedback.

## Solution 
- Implemented routes and endpoints within the Flask-based API to handle audio processing, insights extraction, and summary generation. 
- Integrate the DSM transcription module to convert audio recordings into text using Azure speech-to-text API.
- Utilize the GPT API for natural language processing tasks and analysis..
- The API is fluent in US-English, Spanish and majority of our Indic-Regional languages as well.
- Seamlessly integrate with team members' Google Calendars to automatically add notes and reminders based on extracted DSM insights.

## Getting Started 
To run the project locally, follow these steps:

## Prerequisites
- Python 3.x installed on your machine
- Virtual environment tool such as venv or conda (optional but recommended)

## Installation

1. Clone the repository: </br>
    ```
    git clone https://github.com/Mercor-HackLab/StandupSync.git 
    cd StandupSync
    ```

2. Install the required dependencies: </br>
    ```
    pip install -r requirements.txt
    ```

3. Set up the secret key: 
    - Create a secret_key.py file in the project root directory.
    - Add the following content to the secret_key.py file: </br>
        ```
        API_KEY = "<your-api-key>"
        AZURE_KEY = "<your-azure-key>"
        ```
    - Replace `<your-api-key>` and `<your-azure-key>` with your actual API keys.

4. Set up the Google Calendar credentials:
    - Place the credentials.json file (which contains your Google Calendar API credentials) in the project root directory.

5. Run the project

## API Endpoints
https://meetingsync123.azurewebsites.net/process_audio
https://meetingsync123.azurewebsites.net/analyse_weekly_data
https://meetingsync123.azurewebsites.net/questions

## Workflow
- User selects the preferred language.
- User chooses the audio input source (Microphone or Audio Stream).
- Audio is recorded and saved as a WAV file.
- Speech-to-text conversion is performed using the selected language and Azure Speech Recognition API.
- The transcribed text is processed using the GPT API to extract insights, summaries, and action items.
- The resulting text is sent to Google Calendar for event creation and notification.
- Enabling weekly analysis based on Google Calendar data.

## Tech Stack/ Methodology
- Python: For server-side development.
- Flask: For building the API server.
- OpenAI GPT API: For Natural Language Processing and Text Generation.
- Google Calendar API: For notes creation and notifications.
- SpeechRecognition Library: For speech-to-text conversion.
- JSON and RESTful API for data exchange. 
- Git for version control and collaborative development.

## Use Cases:
- Automated transcription and analysis of DSMs.
- Improved productivity and efficiency in meeting discussions. 
- Seamless integration with Google Calendar for event management. 
- Multilingual support for enhanced user experience.

## USPs
- Real-time Transcription 
- Multilingual Support 
- Accurate Speech-to-Text Conversion
- Intelligent Meeting Highlights 
- Google Calendar Integration
- Weekly Data Analysis
- Enhanced Efficiency

## Future Scope:
- Developing a  Interactive Dashboard
- Voice Assistant Integration
- Enhanced Scalability
- Custom Analysis Periods

## Video Link
[Click here to redirect](https://drive.google.com/drive/folders/18GDRqg_0BOjwRme-AA4GUBGqKSfp_mHt?usp=sharing) 

## Presentation Link
[Click here to redirect](https://docs.google.com/presentation/d/11PkhfxdJocP7GWlwcuSNR-8Kr3nF9AEv/edit?usp=sharing&ouid=110734208587736988558&rtpof=true&sd=true)

## Acknowledgments
This project is inspired by the need to automate and streamline the process of daily standup meetings. We would like to express our gratitude to the developers and contributors of the libraries and APIs used in this project, which include the GPT API, speech_recognition library and Google Cloud services.