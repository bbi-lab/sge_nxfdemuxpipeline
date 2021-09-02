FROM continuumio/miniconda:4.7.12
LABEL author=""

LABEL description=""

COPY environment.yml .
RUN conda env update -n root -f environment.yml && conda clean -afy
RUN apt-get update && \
    apt-get install -y procps r-base && \
    Rscript -e "install.packages('writexl', repos='http://cran.rstudio.com/')"
