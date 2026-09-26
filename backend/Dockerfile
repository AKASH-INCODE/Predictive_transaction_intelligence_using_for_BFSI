# ---- Base Image ----
FROM python:3.11-slim

# Set working directory inside the container
WORKDIR /app

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire backend source code
COPY . .

# Expose the port FastAPI runs on
EXPOSE 8000

# Start the FastAPI app using uvicorn
# main.py is at: src/utils/fraud_dashboard/main.py
CMD ["uvicorn", "src.utils.fraud_dashboard.main:app", "--host", "0.0.0.0", "--port", "8000"]
