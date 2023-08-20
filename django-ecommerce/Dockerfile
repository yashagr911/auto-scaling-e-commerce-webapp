# Use an official Python runtime as the base image
FROM python:3.8-slim

# Set environment variables
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container at /app
COPY requirements.txt /app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Django project code into the container at /app
COPY . /app/

# Specify the command to run on container startup
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
