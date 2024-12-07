# Use Python 3.7 slim image as the base image
FROM python:3.7-slim

# Set working directory inside the container
WORKDIR /app

# Install dependencies from requirements.txt
COPY requirements.txt /app/requirements.txt
RUN pip3 install --no-cache-dir -r requirements.txt

# Copy the rest of the web application code into the container
COPY . /app

# Set environment variable for Flask secret key
ENV TRIPMEAL_KEY="your-secret-key-here"

# Expose port 5000 for the Flask application
EXPOSE 5000

# Explicitly run the app using python3
CMD ["python3", "/app/app.py"]
