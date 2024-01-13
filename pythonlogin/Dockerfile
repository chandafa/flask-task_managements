# Use the official Python image as the base image
FROM python:3.12.1

# Set the working directory in the container
WORKDIR /app

# Install the application dependencies
COPY requirements.txt .

# Copy the application files into the working directory
RUN pip install --no-cache-dir -r requirements.txt

#copy app
COPY . .

# set env
ENV FLASK_APP=main.py

# expose
EXPOSE 5000

# Define the entry point for the container
CMD ["flask", "run", "--host=0.0.0.0"]