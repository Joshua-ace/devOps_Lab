# DevOps Lab: CI/CD Pipeline for Automated Application Deployment

A small Flask application with a GitHub Actions pipeline that automatically
tests, builds (Docker) and optionally deploys the application on every push.

## Structure
- `app.py` - Flask application
- `tests/test_app.py` - automated tests (pytest)
- `Dockerfile` - container image definition
- `.github/workflows/ci-cd.yml` - CI/CD pipeline (test -> build -> deploy)

## Run locally
```
pip install -r requirements.txt
pytest -v
python app.py
```

## Run with Docker
```
docker build -t devops-lab-app .
docker run -p 5000:5000 devops-lab-app
```
