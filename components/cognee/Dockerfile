# Dockerfile for Cognee AI Framework
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    && rm -rf /var/lib/apt/lists/*

# Copy requirements and install
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy Cognee code
COPY . .

# Expose port if Cognee has a web interface
EXPOSE 8001

# Default command (adjust based on Cognee's entry point)
CMD ["python", "-m", "cognee"]
