FROM condaforge/linux-anvil-cuda:11.7
COPY cgc/env.yaml /tmp/env.yaml
ENV CONDA_OVERRIDE_CUDA="11.2"
RUN /opt/conda/bin/mamba env create -f /tmp/env.yaml && \
    mamba clean --all --yes
