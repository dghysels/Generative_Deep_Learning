sudo apt update && sudo apt upgrade -y
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.10 -y
python3.10 --version


-- may also need
sudo apt update
sudo apt install build-essential libssl-dev libffi-dev zlib1g-dev libncurses5-dev libgdbm-dev libsqlite3-dev libreadline-dev libbz2-dev
sudo apt install python3.10-venv python3.10-distutils
--

python3.10 -m venv tf210venv
source ./tf210venv/bin/activate

python -m pip install "numpy<2" notebooks

python -m pip install "numpy<2" matplotlib

python -m pip install "numpy<2" seaborn

python -m pip install "numpy<2" scikit-image

python -m pip install "tensorflow<2.11"
-- or --
python -m pip install tensorflow==2.10.0

-- other packages may replace when loaded
pip install 'numpy<2'

watch -n 1 nvidia-smi


