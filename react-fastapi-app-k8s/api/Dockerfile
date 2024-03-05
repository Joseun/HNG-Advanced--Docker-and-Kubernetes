FROM python:3.10-alpine

# Set the working directory to /app
WORKDIR /api
# Copy the requirements file into the container at /app
COPY requirements.txt ./

# Install the required packages
RUN pip install -r requirements.txt --no-cache-dir

# Copy the "api" folder into the container at /app
COPY . ./

ENV HNG_LESSON_DAY day1
ENV HNG_API_ORIGINS http//localhost:3000
ENV HNG_API_HOST localhost
ENV HNG_API_PORT 8000

# Expose the port that the FastAPI server will be running on
EXPOSE 8000

CMD ["python", "main.py"] 
