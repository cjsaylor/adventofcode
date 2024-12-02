FROM quay.io/jupyter/minimal-notebook

USER root

ENV DENO_INSTALL="/usr/local/deno"
RUN curl -fsSL https://deno.land/install.sh | sh

USER ${NB_UID}

RUN /usr/local/deno/bin/deno jupyter --unstable --install