# tf-demo-python-hello-world

Simple Python Flask hello world application for Azure App Service deployment.

## Local Development

### Prerequisites

- Python 3.10 or higher
- pip

### Setup and Run

1. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

2. **Start the server:**
   ```bash
   python app.py
   ```

3. **Test the application:**
   ```bash
   # Hello endpoint
   curl http://localhost:8000/
   
   # Health check
   curl http://localhost:8000/health
   ```

The server runs on port `8000` by default (or the port specified in `PORT` environment variable).

### Expected Response

```json
{
  "message": "Hello World from Python!",
  "timestamp": "2025-12-15T10:30:00.000000",
  "version": "1.0.0"
}
```

## Deployment

This application is automatically packaged by GitHub Actions CI pipeline and deployed to Azure App Service via the CD pipeline.
