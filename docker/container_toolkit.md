https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html

sudo nano /etc/docker/daemon.json

{
  "runtimes": {
    "nvidia": {
      "path": "nvidia-container-runtime",
      "runtimeArgs": []
    }
  },
  "default-runtime": "nvidia"
}

sudo systemctl restart docker
