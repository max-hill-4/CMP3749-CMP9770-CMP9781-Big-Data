#FROM python:3.12-slim
#ENV PYSPARK_VERSION=3.5.1
#RUN apt-get update && apt-get install -y \
#    openjdk-11-jdk \
#    wget \
#    curl \
#    && rm -rf /var/lib/apt/lists/*
#ENV JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64"
#ENV PATH="${JAVA_HOME}/bin:${PATH}"
#RUN pip install --upgrade pip
#RUN pip install findspark
#RUN pip install pyspark==$PYSPARK_VERSION
#RUN pip install streamlit
#RUN pip install ipykernel

# Use the official Python image from the Docker Hub with Python 3.12 (Debian Bullseye)
FROM python:3.12-slim-bullseye

# Set the environment variables for Python and Java
ENV PYSPARK_PYTHON=python3
ENV PYSPARK_DRIVER_PYTHON=python3

# Install the required packages
RUN apt-get update && \
    apt-get install -y openjdk-11-jre-headless && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set JAVA_HOME environment variable
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64

# Install PySpark
RUN pip install --upgrade pip
RUN pip install findspark
RUN pip install pyspark
RUN pip install streamlit
RUN pip install ipykernel

CMD ["clear"]