# Use an official Python runtime as a parent image
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app


# Copy the requirements.txt file into the container
COPY requirements.txt /app/requirements.txt

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt


# Copy the rest of the application code into the container
COPY .. .


# Make port 5000 available to the world outside this container
EXPOSE 5000

# Run insert_data.py and then api_server.py when the container launches
CMD ["sh", "-c", "python insert_data.py && python api_server.py"]

