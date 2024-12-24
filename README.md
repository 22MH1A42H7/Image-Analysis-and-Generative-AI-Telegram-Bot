# ImageAnalysis and GenerativeAI Telegram-Bot

**ImageAnalysis and GenerativeAI Telegram-Bot** is a Flask-based application that integrates Telegram's bot API, AWS Rekognition, and Google Generative AI to provide interactive and intelligent features. This bot is designed to process text and image inputs, analyze their content, and provide detailed responses, including generating answers from text or images and recognizing labels, celebrities, and text in images.

---

## Features

1. **Telegram Integration**: Interactive chatbot hosted on Telegram, responding to text and image messages.
2. **Generative AI**: Provides context-aware responses using the Gemini Generative AI API.
3. **Image Analysis**: Uses AWS Rekognition for label detection, celebrity recognition, and text extraction from uploaded images.
4. **Text-Based Assistance**: Processes natural language queries to deliver meaningful insights.
5. **Scalable Deployment**: Hosted on AWS EC2 for reliable and scalable performance.

---

## Technologies Used

- **Backend**: Flask (Python) for server-side logic.
- **Generative AI**: Gemini API for dynamic text generation.
- **Image Processing**: AWS Rekognition for analyzing uploaded images.
- **Telegram Bot API**: For handling user interactions.
- **Deployment**: AWS EC2 running Ubuntu Linux.

---

## Prerequisites

Before setting up the project, ensure the following:

1. **Python 3.8 or above**
2. **Flask Framework**
3. **Telegram Bot API Token** (create a bot using [BotFather](https://core.telegram.org/bots))
4. **Gemini API Key** (for Generative AI features)
5. **AWS Access Credentials** (for Rekognition service)

---

## Installation and Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/22MH1A42H7/Image-Analysis-and-Generative-AI-Telegram-Bot.git
cd image-analysis-generativeai-telegram-bot
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Configure Environment Variables

Replace sensitive details in the `app.py` file with environment variables:

- **Telegram Bot Token**: Set as `TELEGRAM_BOT_TOKEN`
- **Gemini API Key**: Set as `GENAI_API_KEY`
- **AWS Access Keys**: Set as `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`

Use the `.env` file to securely store the variables:

```plaintext
TELEGRAM_BOT_TOKEN=your-telegram-bot-token
GENAI_API_KEY=your-generative-ai-key
AWS_ACCESS_KEY_ID=your-aws-access-key
AWS_SECRET_ACCESS_KEY=your-aws-secret-key
AWS_REGION=us-east-1
```

Install the `python-dotenv` package to load the environment variables:

```bash
pip install python-dotenv
```

### Step 4: Run the Application

Start the Flask app:

```bash
python app.py
```

### Step 5: Telegram Bot Configuration

1. Open [BotFather](https://core.telegram.org/bots) in Telegram.
2. Create a new bot using the `/newbot` command and get your token.
3. Configure the webhook URL for your bot:
   
   Replace `<your-server-ip-or-domain>` with your EC2 public IP or domain:

   ```bash
   curl -F "url=https://<your-server-ip-or-domain>/" https://api.telegram.org/bot<YOUR_TELEGRAM_BOT_TOKEN>/setWebhook
   ```

4. Test the bot by sending messages or images.

---

## Deployment Steps on Ubuntu Linux

### 1. Update the System

```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Install Required Packages

```bash
sudo apt install python3 python3-pip python3-venv -y
```

### 3. Set Up Virtual Environment

- Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

- Install the required Python packages:

```bash
pip install -r requirements.txt
```

### 4. Run the Flask Application

```bash
python app.py
```

### 5. Configure Web Server (Optional)

Use Nginx or Apache for serving the bot in production.

---

## Future Enhancements

1. **Multi-Language Support**: Add support for handling queries in multiple languages.
2. **Database Integration**: Store user interactions in a database for analysis and feedback.
3. **Enhanced Security**: Implement OAuth and IP-based restrictions for secure access.
4. **Webhooks for Notifications**: Integrate webhook notifications for real-time updates.

---

## Author

**Satya Praveen M**  
Cloud and Devops Enthusiast  

- **LinkedIn**: [https://www.linkedin.com/in/Satya Praveen M](https://www.linkedin.com/in/satya-praveen-m-36442725b/)  
- **GitHub**: [https://github.com/Satya Praveen M](https://github.com/22MH1A42H7)  

---

Thank you for exploring **ImageAnalysis and GenerativeAI Telegram-Bot**! If you have suggestions or would like to contribute, feel free to create an issue or submit a pull request.

