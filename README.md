# Fatih Yapici - Portfolio Website

A professional portfolio website built with HTML, CSS, and JavaScript, featuring Apple-style aesthetics and automated deployment to Hostinger.

## Project Structure

- `index.html`: Main website content.
- `assets/css/style.css`: Stylesheet with design variables and animations.
- `assets/js/main.js`: Logic for scroll animations and dynamic elements.
- `.github/workflows/deploy.yml`: GitHub Actions workflow for FTP deployment.

## Deployment Setup

This project is configured to deploy automatically to Hostinger using GitHub Actions.

### Prerequisites

1.  **Hostinger Account**: You need an active hosting plan for `fatihyapici.com`.
2.  **GitHub Repository**: This code should be pushed to a public or private GitHub repository.

### Configuration

To enable the deployment workflow, you must add the following **Repository Secrets** in GitHub:

1.  Go to **Settings** > **Secrets and variables** > **Actions** > **New repository secret**.
2.  Add the following secrets (get these credentials from your Hostinger FTP Accounts section):
    *   `FTP_SERVER`: The FTP IP address or hostname.
    *   `FTP_USERNAME`: The FTP username.
    *   `FTP_PASSWORD`: The FTP password.

### How it Works

*   Every time you **push** changes to the `main` branch, the GitHub Action will run.
*   It utilizes `SamKirkland/FTP-Deploy-Action` to sync the files from this repository to the `public_html` directory on your Hostinger server.
*   Changes should be live within minutes.

## Local Development

To make changes locally:

1.  Open `index.html` in your browser to preview.
2.  Edit files as needed.
3.  Commit and push to trigger a deployment.
