FROM continuumio/miniconda3
MAINTAINER Patrick Hüther <patrick.huether@gmi.oeaw.ac.at>
LABEL authors="patrick.huether@gmi.oeaw.ac.at" \
    description="Container image containing shiny dependencies for araDeepopsis"

COPY environment.yml /
RUN apt-get update && apt-get install -y procps graphviz && apt-get clean -y
RUN conda env create -f /environment.yml && conda clean -afy
ENV PATH /opt/conda/envs/aradeepopsis-shiny-v1.2.1/bin:$PATH

EXPOSE 44333