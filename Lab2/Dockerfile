# Use base image python:3.9-slim
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Install system packages curl and vim
RUN apt-get update && apt-get install -y curl vim && rm -rf /var/lib/apt/lists/*

# Copy requirements.txt and install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy app.py file into the container
COPY app.py .

# Create user appuser with UID 1000
RUN useradd -u 1000 -m appuser

# Switch to user appuser
USER appuser

# Expose port 5000
EXPOSE 5000

# Set environment variable FLASK_ENV to production
ENV FLASK_ENV=production

# Run the application
CMD ["python", "app.py"]
