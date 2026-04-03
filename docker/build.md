

Install the container toolkit on ubuntu
https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html

docker run --gpus all -it --rm -v $(pwd):/tf/notebooks -p 8888:8888 tensorflow/tensorflow:2.15.0-gpu-jupyter

docker build -f ./docker/Dockerfile.gpu -t tensorflow2_10_1_gpu:Gen_deep_learn .

docker run --gpus all -it --rm  tensorflow2_10_1_gpu:Gen_deep_learn

* remove the container when stopped - start the container in the folder ./Generative_Deep_Learning
docker run -it --rm --gpus all -p 8888:8888 -v "$(pwd)/notebooks:/tf" tensorflow/tensorflow:2.10.1-gpu-jupyter

* give the container the name tf210gpu - start the container in the folder ./Generative_Deep_Learning
docker run -it --name tf210gpu --gpus all -p 8888:8888 -v "$(pwd)/notebooks:/tf" tensorflow/tensorflow:2.10.1-gpu-jupyter

* start the persistent container
docker start -ai tf210gpu

C:\Python\Python310

c:\python\python310\python -m venv tensor210venv

(activate)

python -m pip install "tensorflow<2.11"

python -m pip install tensorflow==2.10.0