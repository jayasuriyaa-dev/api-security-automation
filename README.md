# api-security-automation
[![Automated API Security Fuzzing](https://github.com/jayasuriyaa-dev/api-security-automation/actions/workflows/api-pipeline.yml/badge.svg)](https://github.com/jayasuriyaa-dev/api-security-automation/actions/workflows/api-pipeline.yml)

## 🎯 Project Overview
This repository contains a fully automated Continuous Integration / Continuous Deployment (CI/CD) pipeline dedicated to API security testing. It executes daily fuzzing payloads against RESTful endpoints to identify vulnerabilities, bypassing standard UI limitations.

## 🛠️ Tech Stack & Architecture
* **Postman:** API request configuration and JavaScript test assertions.
* **JSON Data Loops:** Injection of adversarial AI fuzzing payloads to test security boundaries.
* **Newman:** CLI execution engine.
* **GitHub Actions (YAML):** Cloud-hosted CI/CD automation and cron scheduling.
* **HTMLExtra:** Enterprise-grade executive dashboard generation.

## ⚙️ Pipeline Mechanics
1. **Automated Trigger:** The pipeline runs on every `push` to the main branch AND automatically at midnight UTC via a scheduled `cron` job.
2. **Environment Setup:** Spins up an `ubuntu-latest` runner and configures the `Node.js 20` engine.
3. **Execution:** Fires the Newman CLI, feeding environmental variables and fuzzing data arrays into the collection.
4. **Artifact Generation:** Regardless of test pass/fail status, the pipeline extracts the results and uploads an interactive `Newman-Dashboard.zip` artifact containing the HTML summary.
