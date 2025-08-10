# Description: Dockerfile for Docker container with Base Jupyter Notebook environment for network traffic analysis

FROM quay.io/jupyter/base-notebook

#### INSTALL DEPENDENCIES ####
RUN conda update --all --yes \
    && conda install --yes notebook pyshark nest-asyncio pandas numpy scapy matplotlib scikit-learn

#### INSTALL ENVIRONMENT ####
USER root

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends tshark \
    && apt clean

# Generally, Dev Container Features assume that the non-root user (in this case jovyan)
# is in a group with the same name (in this case jovyan). So we must first make that so.
# (see https://github.com/devcontainers-community/templates-jupyter-datascience-notebooks/)
RUN groupadd jovyan \
    && usermod -g jovyan -a -G users jovyan

#### RESTORE UNPRIVILEGED USER ####
USER ${NB_UID}