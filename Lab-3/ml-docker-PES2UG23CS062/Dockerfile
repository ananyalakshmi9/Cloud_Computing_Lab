# Step 1: Specify the base image
FROM python:3.10-slim

# Step 2: Set the working directory
WORKDIR /app

# Step 3: Copy the application file
COPY app.py .

# Step 4: Copy the ML model file
COPY spam_classifier_model.pkl .

# Step 5: Copy the vectorizer file
COPY tfidf_vectorizer.pkl .

# Step 6: Copy the HTML templates folder
COPY templates ./templates

# Step 7: Install required libraries
RUN pip install --no-cache-dir flask scikit-learn joblib

# Step 8: Expose the Flask port
EXPOSE 5000

# Step 9: Command to start the application
CMD ["python", "app.py"]
