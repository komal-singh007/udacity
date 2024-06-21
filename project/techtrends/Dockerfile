# Use Python 3.8 as a base image
FROM python:3.8

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Install the packages from the requirements file
RUN pip install -r requirements.txt

# Copy the rest of the application code into the container
COPY . .

# Expose port 3111 for the application
EXPOSE 3111

# Run the database initialization script
RUN python init_db.py

# Command to run the application
CMD ["python", "app.py"]
