object_detection_tutorial

参考：
1、https://github.com/tensorflow/models/tree/master/research/object_detection

#Installation

```
# For CPU
pip3 install tensorflow
# For GPU
pip3 install tensorflow-gpu

sudo apt-get install protobuf-compiler

sudo pip3 install pillow
sudo pip3 install lxml
sudo pip3 install jupyter
# 启动jupyter 输入 jupyter notebook
sudo pip3 install matplotlib

# 下载models  如：存放在 /home/wu/tf_models/
git clone https://github.com/tensorflow/models.git

cd /home/wu/tf_models/models/research/
protoc object_detection/protos/*.proto --python_out=.

cd /home/wu/tf_models/models/research/
vim ~/.bashrc 
写入 export PYTHONPATH=$PYTHONPATH:'/home/wu/tf_models/models/research':'/home/wu/tf_models/models/research/slim'

bash
```

# 测试

```python
python3 object_detection/builders/model_builder_test.py

"""
Ran 7 tests in 0.016s

OK
"""
```

