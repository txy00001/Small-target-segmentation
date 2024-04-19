# 项目名称

气泡分割检测项目：致力于工厂的pc板上的瑕疵气泡的检测定位


## 准备环境
### 安装mmseg
首先，你需要安装必要的库和依赖。打开你的终端或命令提示符，执行以下命令：
requirements.txt里也有对应mmseg,mmcv,mmengine的安装版本链接

```
pip install -U openmim
mim install mmengine
mim install "mmcv"
pip install -U openmim
mim install mmengine
pip install "mmsegmentation"

```

### 安装 requirements.txt
在确保你的Python环境设置完毕后，通过以下命令安装项目所需的其他依赖：

```
pip install -r requirements.txt

```
## 运行
### 运行脚本

要运行主脚本，请确保你已经处于项目的根目录下，然后执行：

```
cd utils
python demo.py

```
### model

请确保config.py和weights.pth文件都位于同一个文件夹内。这对于脚本的正确执行至关重要。

### 说明
添加了ONNX的推理，在对应文件夹内，用onnx做推理的话batch指定为1，用pth和config推理的话，batch小于等于35，大了会报错；
onnx的接口与torch接口方式一致，接口实现做了调整，onnx的文件夹里knet-dy-sim.onnx是动态的，另一个onnx是静态的，建议使用静态的onnx

```
 模型权重链接：链接：https://pan.baidu.com/s/1QwBlnN4B4ADq0g5qv10NBg?pwd=sqvn 
提取码：sqvn
