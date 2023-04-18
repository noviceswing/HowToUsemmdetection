## pytorch环境
conda create -n mmdetection python=3.8 -y

conda install pytorch==1.12.0 torchvision==0.13.0 torchaudio==0.12.0 cudatoolkit=11.3 cudnn=8.2.1 -c pytorch


## 源码安装 mmdetection
pip install -U openmim
mim install mmengine
mim install "mmcv>=2.0.0"

git clone https://github.com/open-mmlab/mmdetection.git

cd mmdetection(可有可无)

**将 pycocotools_windows-2.0.0.2-cp38-cp38-win_amd64.whl 用 pip 安装至环境**

进入pycocotools_windows-2.0.0.2-cp38-cp38-win_amd64.whl 文件夹

pip install pycocotools_windows-2.0.0.2-cp38-cp38-win_amd64.whl

回到 mmdetection 文件夹
pip install -v -e .


## 下载权重
mim download mmdet --config rtmdet_tiny_8xb32-300e_coco --dest .

## 验证demo
python demo/image_demo.py demo/demo.jpg rtmdet_tiny_8xb32-300e_coco.py --weights rtmdet_tiny_8xb32-300e_coco_20220902_112414-78e30dcc.pth --device cpu





