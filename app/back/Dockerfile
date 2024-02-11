# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set the working directory to /app/back
WORKDIR /app/back

# Copy the current directory contents into the container at /app/back
COPY . /app/back

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose port 8080 to allow external access
EXPOSE 8080

# Command to run on container start
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]