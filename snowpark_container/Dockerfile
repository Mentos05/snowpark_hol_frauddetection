FROM continuumio/miniconda3:latest
MAINTAINER Michael Gorkow <michael.gorkow@snowflake.com>

# Copy Conda-Environment File and Snowpark into Container
COPY conda_env.yml .

# Create Anaconda Environment from Conda-Environment File and cleanup
RUN conda env create -f conda_env.yml && rm conda_env.yml && conda clean -a

# Create the Jupyter Lab Startup Folder
RUN mkdir -p /snowpark_dev

# Run Jupyter Lab at container startup
ENTRYPOINT ["/bin/sh", "-c", "echo 'Visit http://localhost:9998' && \
    /opt/conda/envs/pysnowpark/bin/jupyter notebook \
         --ip 0.0.0.0 --port 9998 --allow-root \
         --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/snowpark_dev'"]