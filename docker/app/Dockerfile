FROM ubuntu:18.04
#USER root

## Set environment variables
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8


RUN apt-get update --fix-missing
RUN apt-get install -y wget \
	bzip2 \
	ca-certificates \
	build-essential \
	curl \
	git-core \
	pkg-config \
	python3-dev \
	python3-pip \
	python3-setuptools \
	python3-virtualenv \
	unzip \
	software-properties-common \
	llvm
RUN add-apt-repository -y ppa:ubuntugis/ubuntugis-unstable && apt-get update

# Set python aliases for python3
RUN echo 'alias python=python3' >> ~/.bashrc
RUN echo 'alias pip=pip3' >> ~/.bashrc

# Update C env vars so compiler can find gdal
ENV CPLUS_INCLUDE_PATH=/usr/include/gdal
ENV C_INCLUDE_PATH=/usr/include/gdal

RUN apt install -y gdal-bin python-gdal python3-gdal

## Install packages to Python3
RUN pip3 install --upgrade pip
RUN pip3 install pandas==0.25.1 \
		numpy==1.17.1 \ 
		rasterio==1.1.0 \
		scipy==1.3.1 \
		folium==0.10.0 \
		GDAL \
		requests \
		pytest-shutil \
		glob2 \
		Shapely \
		simplejson \
		scikit-learn==0.21.3 \ 
		matplotlib==3.1.1 \
		rio-l8qa \
		rio_toa==0.3.0 \
		rio_color==1.0.0 \ 
		fiona==1.8.6 \ 
		geopandas==0.6.0rc1 \
		descartes\
		jupyterlab 


# Generate default config and disable authentication
RUN jupyter-notebook --generate-config --allow-root
RUN sed -i "s/#c.NotebookApp.token = '<generated>'/c.NotebookApp.token = ''/" /root/.jupyter/jupyter_notebook_config.py

WORKDIR /home
COPY jupyter_files /home
COPY shp /home

CMD jupyter-lab --port=8888 --no-browser --ip=0.0.0.0 --allow-root








