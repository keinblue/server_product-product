FROM mcr.microsoft.com/devcontainers/java:1-17-bookworm

# Install additional tools
RUN apt-get update && apt-get install -y \
    mariadb-client \
    && rm -rf /var/lib/apt/lists/*

# Create directories with proper ownership
RUN mkdir -p /workspace/uploads && chown vscode:vscode /workspace/uploads \
    && mkdir -p /home/vscode/.gradle && chown vscode:vscode /home/vscode/.gradle \
    && mkdir -p /workspace/build && chown vscode:vscode /workspace/build

# Set working directory
WORKDIR /workspace

USER vscode
