FROM condaforge/linux-anvil-cuda:11.7

COPY cgc/env.yml /tmp/env.yml

ENV CONDA_OVERRIDE_CUDA="11.2"
ENV PATH=$PATH:/opt/conda/bin

RUN rm -rf ~/.condarc

RUN /opt/conda/bin/mamba clean --all --yes -q
RUN /opt/conda/bin/mamba update --all --yes

RUN /opt/conda/bin/mamba env update -f /tmp/env.yml && \
    /opt/conda/bin/mamba clean --all --yes -q
