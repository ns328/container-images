# container-images
# simple web applcation
# Installing and configure web server 
apt-get update

apt-get install -y python

apt-get install python3-pip

pip install flask

# Start web server

FLASK_APP= /opt/app.py flask run --host=0.0.0.0

# Create docker image

docker build . -t namrata328/my-flask-app:v1

# Run docker image

docker run namrata328/my-flask-app:v1

# Push docker image into github package

docker tag namrata328/my-flask-app:v1 ghcr.io/ns328/container-images/namrata328/my-flask-app:v1

docker push ghcr.io/ns328/container-images/namrata328/my-flask-app:v1
