FROM sgillespie/gitlab-runner:0.4.0

# Install docker client
RUN apt-get update && apt-get install -y docker.io

# Add gitlab-runner to docker group
RUN usermod -aG docker gitlab-runner

# Override default params
CMD ["run"]
