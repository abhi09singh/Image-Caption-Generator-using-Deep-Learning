#Using the base image with Python 3.10
FROM python:3.10
 
#Set our working directory as app
WORKDIR /app 

# Copy the model's directory and server.py files
COPY . /app

#Installing Python packages through requirements.txt file
RUN python3 -m pip install --no-cache-dir -r requirements.txt
 
#Exposing port 5000 from the container
EXPOSE 5000

#Starting the Python application
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "app3_Final:app"]
