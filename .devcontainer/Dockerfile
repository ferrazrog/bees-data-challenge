FROM python:3.12.1-bullseye
#FROM nvcr.io/nvidia/merlin/merlin-tensorflow:23.09

# Atualiza os pacotes
#RUN apt-get update && apt-get install -y python3 python3-pip python3-dev

COPY requirements.txt /tmp/

RUN pip install --no-cache-dir -r /tmp/requirements.txt

# Make port 8888 available to the world outside this container
EXPOSE 8888

# Run Jupyter notebook when the container launches
CMD ["jupyter", "notebook", "--ip='*'", "--port=8888", "--no-browser", "--allow-root"]