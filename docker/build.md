

docker build -f ./docker/Dockerfile.gpu -t tensorflow2_10_1_gpu:Gen_deep_learn .

docker run --gpus all -it --rm  tensorflow2_10_1_gpu:Gen_deep_learn

docker run -it --rm --gpus all -p 8888:8888 -v "$(pwd)/notebooks:/tf/notebooks" tensorflow/tensorflow:2.10.1-gpu-jupyter

C:\Python\Python310

c:\python\python310\python -m venv tensor210venv

(activate)

python -m pip install "tensorflow<2.11"

python -m pip install tensorflow==2.10.0