# Use a web server as the base image
FROM nginx:latest

WORKDIR /usr/share/nginx/html

# Copy the contents of the app/front directory to the working directory
COPY . .

# Make the entrypoint.sh script executable
RUN chmod +x entrypoint.sh

# Install dos2unix and convert the entrypoint.sh script
RUN apt-get update && apt-get install -y dos2unix && dos2unix entrypoint.sh

# Set the environment variable WS_BACK_URL
ENV WS_BACK_URL=http://new-container:8080

# Set the entrypoint
ENTRYPOINT ["./entrypoint.sh"]
