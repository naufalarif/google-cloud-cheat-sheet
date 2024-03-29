### How to use Google Cloud Run to deploy your serverless app #asia-southeast2
# Create your Artifacts Registry
- gcloud artifacts repositories create REPO_NAME --repository-format=docker --location=YOUR_LOCATION --description="[YOUR_DESCRIPTION]"
# Make sure your artifacts is exists
- gcloud artifacts repositories describe REPO_NAME --location=asia-southeast2
# Setup your local env to be able push docker image to Artifact Registry
- gcloud auth configure-docker asia-southeast2-docker.pkg.dev
# On your local, build docker image first
- docker build -t asia-southeast2-docker.pkg.dev/PROJECT_ID/REPO_NAME/IMAGE_NAME:IMAGE_TAG .
# Then push it to artifacts registry
- docker push asia-southeast2-docker.pkg.dev/PROJECT_ID/REPO_NAME/IMAGE_NAME:IMAGE_TAG
# Afterwards go to google cloud console -> google cloud run https://console.cloud.google.com/run
## Setup your google cloud run, pointing your repository to artifacts registry you want
Done!
