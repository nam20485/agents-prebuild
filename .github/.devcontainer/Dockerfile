FROM ghcr.io/nam20485/dotnet-prebuild:main-latest

RUN npm install -g @github/copilot
RUN npm install -g @google/gemini-cli@preview
RUN curl -fsSL https://claude.ai/install.sh | bash -s latest
RUN npm install -g @qwen-code/qwen-code@latest
RUN curl -fsSL https://opencode.ai/install | bash

# desktop commander
# install jetbrains rider backend
# install jb gateway
# install jetbrains toolbox

# run vs code server


# install kiro code editor
RUN copilot --version && \
    gemini --version && \
    claude --version && \
    qwen-code --version && \
    opencode --version