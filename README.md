# Python Flask CI/CD


This project is a basic Python Flask web API demonstrating DevSecOps principles through an automated CI/CD pipeline with security and quality gates configured using GitHub Actions.

## CI/CD Pipeline
The `.github/workflows/main.yaml` file defines the GitHub Actions workflow, which includes:
- Linting with `flake8`
- Running tests with `unittest`
- Performing static code analysis with `Bandit`

## Local Installation and Execution

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Anirudh21-hub/StockMarketMaven.git
    cd StockMarketMaven
    ```

2.  **Create and activate a Python virtual environment:**
    ```bash
    python -m venv venv
    # On Windows:
    .\venv\Scripts\activate
    # On macOS/Linux:
    source venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    (Note: `Bandit` requires Python 3.7+; ensure your Python version is compatible within your virtual environment.)

4.  **Run the Flask application:**
    ```bash
    flask run
    ```
    Access the application at `http://127.0.0.1:5000/` in your browser.

5.  **Run the tests:**
    ```bash
    python -m unittest test_app.py
    ```

## Deployment to Heroku (Optional)

To deploy this application to Heroku, follow these steps:

1.  **Install the Heroku CLI:**
    Follow the instructions on the official Heroku Dev Center: [https://devcenter.heroku.com/articles/heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)

2.  **Log in to Heroku CLI:**
    ```bash
    heroku login
    ```
    This will open a browser window for you to log in.

3.  **Create a Heroku app:**
    ```bash
    heroku create <YOUR_APP_NAME>
    ```
    Replace `<YOUR_APP_NAME>` with a unique name for your Heroku application.

4.  **Push code to Heroku:**
    ```bash
    git push heroku main
    ```
    Heroku will detect the `Procfile` and `runtime.txt` and deploy your application.

5.  **Open the deployed application:**
    ```bash
    heroku open
    ```

## Build Status
[![Build Status](https://github.com/Anirudh21-hub/StockMarketMaven/workflows/Python%20Flask%20CI/CD/badge.svg)](https://github.com/Anirudh21-hub/StockMarketMaven/actions)

## Security Scan
[![Bandit Security Scan](https://github.com/Anirudh21-hub/StockMarketMaven/workflows/Python%20Flask%20CI/CD/badge.svg?event=push)](https://github.com/Anirudh21-hub/StockMarketMaven/actions)
[![Secret Scan](https://github.com/Anirudh21-hub/StockMarketMaven/workflows/Secret%20Scan/badge.svg)](https://github.com/Anirudh21-hub/StockMarketMaven/actions?query=workflow%3A%22Secret+Scan%22)

## Result Demo and link
https://drive.google.com/file/d/1laf8inCoHWQ_qA_U5wTdaEZbRRsDgXHd/view?usp=sharing
https://github.com/Anirudh21-hub/StockMarketMaven/actions

## Reflection
During this project,the importance of continuous integration and the value of incorporating security and quality gates early in the development lifecycle were demonstrated. Setting up the GitHub Actions pipeline, especially configuring tools like Bandit and Gitleaks, provided hands-on experience with DevSecOps practices. The most challenging aspect was resolving environment and compatibility issues with various Python packages across different Python versions.

## AI Usage

This project was significantly aided by usage of ChatGPT. It was instrumental in generating the initial Flask application structure, setting up the GitHub Actions workflow YAML files, and creating the Procfile and runtime.txt for Heroku deployment. 
