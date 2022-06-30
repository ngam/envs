FROM mambaorg/micromamba:0.24.0
COPY --chown=$MAMBA_USER:$MAMBA_USER env.yml /tmp/env.yml
ENV CONDA_OVERRIDE_CUDA="11.2"
RUN micromamba install -y -n base -f /tmp/env.yml && \
    micromamba clean --all --yes
