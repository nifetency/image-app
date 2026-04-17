# Image App Example

A **Python-based image processing** application published as a **sample deployment project for [Nife.io](https://nife.io)**.

This repository demonstrates how to run a lightweight image processing application locally and deploy it on [Nife.io](https://nife.io). It is intended as a practical sample for testing image processing deployment workflows and showcasing a straightforward Flask deployment path.

## Overview

This project is a basic image processing application with a standard project structure and comprehensive image manipulation logic. It provides various image operations and morphological transformations. It is designed to be small enough for learning and deployment experiments while still reflecting the conventions of a real image processing application.[3]

If you want a simple image processing sample to test deployment on [Nife.io](https://nife.io), this repository is a good starting point.

## Features

| Feature | Description |
| --- | --- |
| Image operations | Equalization, flipping, mirroring, binarization, inversion, solarization |
| Morphological transformations | Erosion, dilation, opening, closing, gradient, boundary extraction |
| File upload | Direct image upload from local folder |
| Grayscale conversion | Toggle switch for grayscale conversion |
| Flask web interface | User-friendly web-based interface |
| Deployment-ready setup | Can be deployed using Git-based workflows |
| Nife.io sample use case | Suitable as a reference project for [Nife.io](https://nife.io) deployments |

## Tech Stack

| Technology | Purpose |
| --- | --- |
| Python | Runtime environment |
| Flask | Web framework |
| OpenCV | Computer vision library |
| NumPy | Numerical computing |
| Nife.io | Deployment platform |

## Prerequisites

Before running the project locally, make sure the following are installed.

| Requirement | Notes |
| --- | --- |
| Python | Version 3.7+ recommended |
| pip | Python package manager |
| Git | Required to clone the repository |

## Getting Started

### Clone the repository

```bash
git clone https://github.com/nifetency/image-app.git
cd image-app
```

### Create a virtual environment (recommended)

```bash
python -m venv venv
```

**Activate the virtual environment:**

- **On Windows:**
  ```bash
  venv\Scripts\activate
  ```

- **On macOS/Linux:**
  ```bash
  source venv/bin/activate
  ```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Start the application

```bash
python app.py
```

Then open the application at `http://localhost:80`.

## Deploy on Nife.io

You can deploy this application on [Nife.io](https://nife.io) using either the Git repository or the CLI.[1] [2]

### Option 1: Deploy from the Git repository

Deploy the project directly from GitHub.

| Setting | Value |
| --- | --- |
| Source | Git Repository |
| Provider | GitHub |
| Branch | `main` |
| Internal Port | `8080` |
| External Port | `80` |
| Build Mode | Auto-Dockerize with runtime |

### Option 2: Deploy with `nifectl`

If you prefer the command line, use the following workflow.

```bash
nifectl auth login
nifectl init
nifectl deploy
```

For step-by-step instructions, see the [Nife.io Quick Deploy documentation](https://docs.nife.io/overview/quick-deploy) and the [nifectl quick start guide](https://docs.nife.io/deploy/python).

## Environment Variables

The following variables are commonly relevant for deployment.

| Variable | Description | Example |
| --- | --- | --- |
| `FLASK_ENV` | Flask execution environment | `production` |
| `PORT` | Application port | `80` |

## Repository Structure

| Path | Purpose |
| --- | --- |
| `app.py` | Main Flask application |
| `image_ops_scratch.py` | Image operations implementation |
| `image_morphs_scratch.py` | Morphological transformations |
| `assets/` | Static assets (CSS, JavaScript) |
| `images/` | Sample images and output storage |
| `requirements.txt` | Python dependencies |

## Troubleshooting

| Issue | Suggested fix |
| --- | --- |
| Python not installed | Install Python and verify with `python --version` |
| Dependencies missing | Run `pip install -r requirements.txt` |
| Flask import error | Reinstall Flask with `pip install flask` |
| OpenCV import error | Reinstall OpenCV with `pip install opencv-python` |
| Virtual environment issues | Delete venv folder and recreate with `python -m venv venv` |
| Port `80` already in use | Stop the conflicting process or change the port |
| Image upload fails | Check file permissions in `images/` directory |
| Deployment fails on Nife.io | Verify ports, environment variables, and build settings |
| Application is unreachable | Check routing, service exposure, and deployment logs |

## Acknowledgements

This repository is maintained by **Nifetency** as a sample deployment project for [Nife.io](https://nife.io).

Original project by [msameeruddin](https://github.com/msameeruddin/image-app). It is good practice to retain visible credit to the original author.

## License

This project is licensed under the **MIT License**.

## References

[1]: https://nife.io "Nife.io"
[2]: https://docs.nife.io/overview/quick-deploy "Nife.io Quick Deploy"
[3]: https://github.com/nifetency/image-app "nifetency/image-app"
[4]: https://docs.nife.io/deploy/python "Nifectl Quick Start"