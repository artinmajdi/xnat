# Use the MONAI base image
FROM xnat/monai-notebook:0.3.0

USER root

# Install Java
RUN apt-get update && \
    apt-get install -y openjdk-8-jdk && \
    apt-get clean;

# Switch back to the non-root user
USER jovyan

# Set the working directory
WORKDIR /work

# Add RoiUploaDAssistant.jar to the container
ADD RoiUploadAssistant-Fat.jar /work;

# Set the entry point to run the jar
# ENTRYPOINT ["java", "-jar", "/work/RoiUploadAssistant-Fat.jar"]
