FROM python:3.10-slim

WORKDIR /app

# Copy requirements file first so Docker can cache this step
COPY backend/requirements.txt .

# Install Python dependencies
RUN pip install --upgrade pip && pip install -r requirements.txt

# Now copy the rest of the backend code
COPY backend/ .

# Expose the port FastAPI is served on
EXPOSE 8000

# Start the Uvicorn server
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]