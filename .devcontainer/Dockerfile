FROM ghcr.io/astral-sh/uv:debian

RUN apt install bash git  && \
    curl -sS https://starship.rs/install.sh | sh -s - -y && \
    echo 'eval "$(starship init bash)"' >> $HOME/.bashrc && \
    git config --global --add safe.directory '*' && \
    uv tool install pre-commit

ENV PATH="/root/.local/bin:${PATH}"

ENV SHELL=bash
CMD ["/bin/bash"]