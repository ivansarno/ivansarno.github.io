FROM ubuntu:22.04

# Prevents prompts during package install
ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies for Ruby and Jekyll
RUN apt-get update && apt-get install -y \
  curl gnupg build-essential ruby-full git nodejs npm \
  && gem install jekyll bundler \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

# RUN gem install github-pages

# Set up working directory
WORKDIR /workspace

CMD [ "jekyll", "--version" ]