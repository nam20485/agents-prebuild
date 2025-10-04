FROM ghcr.io/nam20485/dotnet-prebuild:main-latest

RUN npm config set fund false --global

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
#RUN curl -fsSL https://raw.githubusercontent.com/abhilashiig/kiro-ide-linux-installation/main/clone-and-install-kiro.sh | bash -s -- --user

RUN copilot --version && \
    gemini --version && \
    claude --version && \
    qwen --version && \
    opencode --version