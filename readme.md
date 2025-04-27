# Nursery Chatbot Project

Welcome to the **Nursery Chatbot** project! This project is a chatbot designed for a nursery, providing information about the nursery and telling age-appropriate stories when explicitly requested. The chatbot leverages Flask for its web interface and Google's Generative AI for conversational capabilities.

---

## Features
1. **Nursery Information**: Provides core details about the nursery such as location, hours, fees, curriculum, and more.
2. **Stories for Kids**: Offers age-appropriate, engaging stories with morals when explicitly requested.
3. **Web-based Interface**: Users can interact with the chatbot through a web app.
4. **CLI Mode**: An optional command-line interface for local testing.

---

## Prerequisites

Before running this project, ensure you have the following installed:

1. **Python**: Version 3.9 or higher.
2. **Docker** (optional): For containerized deployment.
3. **Git**: To clone the repository.

---

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/nursery-chatbot.git
cd nursery-chatbot
```

### 2. Set Up Environment Variables
Create a `.env` file in the root directory and add the following content:

```
GEMINI_API_KEY=your-google-generative-ai-api-key
```

> Replace `your-google-generative-ai-api-key` with your actual API key for Google's Generative AI.

---

## Running the Project

### Option 1: Run Locally

#### 1. Install Dependencies
Install the required Python packages using pip:

```bash
pip install -r requirements.txt
```

#### 2. Start the Flask App
Run the web interface locally:

```bash
python app.py
```

The app will be available at `http://localhost:5001`.

#### 3. Using the CLI Mode (Optional)
To run the chatbot in CLI mode:

```bash
python My_chatbot.py
```

---

### Option 2: Using Docker

#### 1. Build the Docker Image
Build the Docker image for the project:

```bash
docker build -t nursery-chatbot .
```

#### 2. Run the Docker Container
Run the chatbot in a Docker container:

```bash
docker-compose up
```

The app will be available at `http://localhost:5001`.

---

## Deployment to Production

### Using Gunicorn
The project is pre-configured for production using Gunicorn. To run it:

```bash
gunicorn app:app --bind=0.0.0.0:5001 --workers=2
```

---

## File Structure

- `app.py`: Main Flask application file.
- `My_chatbot.py`: Command-line interface for the chatbot.
- `Dockerfile`: Docker configuration file for containerization.
- `docker-compose.yml`: Compose file for multi-container Docker setup.
- `.env`: Environment variable file.
- `requirements.txt`: List of Python dependencies.
- `Procfile`: Configuration for process management.

---

## Troubleshooting

1. **Missing GEMINI_API_KEY**:
   - Ensure the `.env` file is properly set up with your API key.

2. **Port Conflicts**:
   - If port `5001` is already in use, modify the `docker-compose.yml` or Flask app to use an alternative port.

3. **Dependency Issues**:
   - Use `pip install --force-reinstall -r requirements.txt` to resolve dependency conflicts.

---

## Contribution

Contributions are welcome! Feel free to fork the repository and submit pull requests for new features or bug fixes.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
**Happy Coding! 🌻**