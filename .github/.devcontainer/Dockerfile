FROM ghcr.io/nam20485/dotnet-prebuild:main-latest

# Base image already runs as vscode user with shell completions configured
# We just need to continue as that user for our additional installations
USER vscode

# Disable npm funding messages for this user (applies to all npm operations including -g installs)
RUN npm config set fund false

# Install AI CLI tools globally (using sudo since vscode user has sudoers access)
RUN sudo npm install -g @github/copilot && \
    sudo npm install -g @google/gemini-cli@preview && \
    sudo npm install -g @qwen-code/qwen-code@latest

# Install Claude CLI (runs as vscode user)
RUN curl -fsSL https://claude.ai/install.sh | bash -s latest

# Install OpenCode CLI (runs as vscode user)
RUN curl -fsSL https://opencode.ai/install | bash

# Verify installations
RUN copilot --version && \
    gemini --version && \
    claude --version && \
    qwen --version

# Set working directory to vscode user home
WORKDIR /home/vscode
