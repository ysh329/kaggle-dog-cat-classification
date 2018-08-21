# kaggle-dog-cat-classification

## Download Docker Image

```shell
docker pull mxnet/python:gpu
docker run -v /home/yuanshuai:/home/yuanshuai -tdi mxnet/python:gpu
docker attach <container_id>
```

## Install Software

```shell
apt update
apt install -y vim git tmux ipython
```

Python library:

```shell
pip install --upgrade pip
pip install opencv-python
```

## Download MXNet

```shell
mkdir /home/yuanshuai/code
cd /home/yuanshuai/code
git clone --recursive https://github.com/apache/incubator-mxnet.git
cd incubator-mxnet
```

## Prepare MXNet Data  

```shell
python tools/im2rec.py --list --recursive --train-ratio 0.95 dogcat /home/yuanshuai/code/kaggle-dog-cat-classification/data/train/
python tools/im2rec.py --resize 224 --quality 95 --num-thread 16 dogcat /home/yuanshuai/code/kaggle-dog-cat-classification/data/train
mv dogcat_* /home/yuanshuai/code/kaggle-dog-cat-classification/data/
```

useless More: [Libgthread-2.0.so.0 Download (RPM, TXZ)](https://pkgs.org/download/libgthread-2.0.so.0)


