# Pre-built Dev Container Image for R. More info: https://github.com/rocker-org/devcontainer-images/pkgs/container/devcontainer%2Ftidyverse
# Available R version: 4, 4.1, 4.0
ARG VARIANT="4.2"
FROM ghcr.io/rocker-org/devcontainer/tidyverse:${VARIANT}

# change user password
RUN echo "rstudio:rstudious" | chpasswd

# Example of adding R package automatically
RUN install2.r --error --skipinstalled -n -1 \
        httpgd \
        cowsay \
    && rm -rf /tmp/downloaded_packages
