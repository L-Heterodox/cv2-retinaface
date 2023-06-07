# cv2-retinaface
1.搭建pytorch对应环境并git clone官方开源代码\
2.下载数据集和标签，并正确组织数据集结构，修改代码中传入路径\
3.使用widerface训练集训练模型，原作者提供了用restnet50和mobilenet0.25作为骨干网络训练得到模型，由于本机显存所限，后续加载了官方提供的网络权重文件，本次实验选择了Resnet50\_Final.pth\
4.加载训练好的模型对widerface验证集进行检测，生成文本文件\
5.对比验证集真值，得出该模型在验证集的测试效果\
6.输入单张照片进行测试，可视化实验结果

文件夹组织结构：\
├─curve：存放一些测试图片，最终用于detect.py传入和传出\
├─data：放置数据集\
│  ├─FDDB：此实验未使用\
│  ├─widerface：widerface数据集，下面给出了百度网盘链接（已组织好）\
│  │  ├─train\
│  │  │  └─images\
│  │  └─val\
│  │      └─images\
│  └─__pycache__\
├─layers\
│  ├─functions\
│  │  └─__pycache__\
│  ├─modules\
│  │  └─__pycache__\
│  └─__pycache__\
├─models\
│  └─__pycache__\
├─utils\
│  ├─nms\
│  │  └─__pycache__\
│  └─__pycache__\
├─weights：官方开源的一些权重文件，下面会给出百度云下载链接\
└─widerface_evaluate：评估在val上效果\
    ├─build\
    │  ├─lib.win-amd64-3.9\
    │  └─temp.win-amd64-3.9\
    │      └─Release\
    ├─ground_truth：真值文件\
    └─widerface_txt：测试生成文本文件\

一些已经可以使用的百度云链接：\
widerface数据集：链接：https://pan.baidu.com/s/1CzuwzcwRccf_Qv8Geemziw?pwd=pcei 提取码：pcei \
weights文件：链接：https://pan.baidu.com/s/1-WJykZyGMPk2cBae3lIk1w?pwd=8gl7 提取码：8gl7 \
ground_truth文件：链接：https://pan.baidu.com/s/1rotUXCPJtoRMuADvyoudyw?pwd=pjhn 提取码：pjhn \
本次实验在val上结果widerface_txt：链接：https://pan.baidu.com/s/1wJWhsylQPMOREBeG63AoEQ?pwd=10ep 提取码：10ep 

参考链接：\
RetinaFace: Single-stage Dense Face Localisation in the Wild：https://arxiv.org/abs/1905.00641 \
代码参考：\
https://github.com/biubug6/Pytorch_Retinaface \
https://github.com/hukkelas/DSFD-Pytorch-Inference \
https://gitee.com/FateFaker/retinaface-pytorch#https://gitee.com/link?target=https%3A%2F%2Fpan.baidu.com%2Fs%2F1LIYlK5sVx4qsK9tvEuJ4cw

        
