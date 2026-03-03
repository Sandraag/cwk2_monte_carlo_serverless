MonteCarlo_Serverless_Benchmarking
=====================

## Overview:
This project evaluates the performance, scalability, and efficiency of serverless computing platforms by benchmarking a Monte Carlo simulation used to estimate the value of π (Pi). The study compares a commercial cloud platform (Microsoft Azure Functions) with an open-source alternative (OpenFaaS) to assess execution time, cold vs warm start behaviour, concurrency handling, and runtime performance under varying workloads.

## Key Features:
- Cloud-Based Serverless Benchmarking: Implementation and comparison of Microsoft Azure Functions (commercial) and OpenFaaS (open-source) deployed on a Docker-based Azure Virtual Machine.
- Monte Carlo Simulation Engine: Python (v3.11) multithreaded simulation using concurrent.futures.ThreadPoolExecutor to estimate π with configurable parameters.
- Interactive Web Interface: Lightweight HTML/CSS/JavaScript frontend allowing users to trigger simulations, modify test parameters, and visualise performance results.
- Performance Evaluation: Measurement of execution time, total test time, error margin, cold vs warm start latency, and concurrency scalability.
- Scalability Testing: Experimental increase of concurrent requests to analyse runtime behaviour under load.

## Tasks Breakdown

1. Architecture Design:
Design a high-level cloud architecture separating computational logic, API endpoints, and UI components. Implement modular serverless functions for scalability and clean deployment.

2. Commercial Deployment (Azure Functions):
Develop HTTP-triggered Azure Functions to:
- Perform Monte Carlo computation
- Serve frontend interface
- Save and export test history
Deploy using Azure Function runtime and integrate monitoring tools.

3. Open-Source Deployment (OpenFaaS):
Deploy OpenFaaS on an Azure-hosted Ubuntu VM.
Containerise the Python simulation using Docker and deploy via OpenFaaS CLI.
Separate computational logic (function_app.py) and handler (handler.py) for modular design.

4. Experimentation:
Conduct cold vs warm start testing.
Increase concurrency levels to observe scalability trends.
Measure execution time, response behaviour, and system stability under varying loads.

5. Data Collection:
Record:
- Successful and failed requests
- Average π estimation
- Average execution time
- Total test time
- Error margin
Store test history for cross-platform comparison.

6. Statistical Analysis:
Analyse execution times using descriptive statistics.
Compare performance trends between Azure Functions and OpenFaaS.
Evaluate concurrency impact on runtime efficiency.

7. Results Reporting:
Summarise findings on:
- Cold vs warm start performance differences
- Concurrency scalability behaviour
- Runtime consistency and error margins
Highlight that both platforms produced accurate π approximations (~3.14159) with competitive performance, while demonstrating expected increases in execution time under higher concurrent loads.
 ![Alt text](https://github.com/Sandraag/cwk2_monte_carlo_serverless/blob/main/14e581c5-1.png)
 ![Alt text](https://github.com/Sandraag/cwk2_monte_carlo_serverless/blob/main/Screenshot%202026-03-03%20141706.png)

## Technologies Used:
- Python 3.11
- Microsoft Azure Functions
- OpenFaaS
- Docker
- Azure Virtual Machine (Ubuntu)
- HTML, CSS, JavaScript
- concurrent.futures (ThreadPoolExecutor)




