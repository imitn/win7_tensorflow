# Win7 环境下安装Tensorflow

1. 下载Anaconda：https://www.anaconda.com/download/。

2. 安装Anaconda。一路默认即可。

3. 打开“开始目录”，找到Anaconda/Anaconda prompt，以管理员权限运行。

4. 添加清华镜像
```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --set show_channel_urls yes
```

5. 创建一个python版本为3.5的名为mytensorflow 的环境。

conda create -n mytensorflow python=3.5 anaconda

6. 安装TensorFlow到mytensorflow环境。

conda install -n mytensorflow -c conda-forge tensorflow=1.3.0

7. 激活虚拟环境

activate mytensorflow 

8. 安装下列依赖包
```
conda install jupyter=1.0.0
conda install matplotlib=2.0.2
conda install numpy=1.13.1
conda install pandas=0.20.3
conda install psutil=5.3.1
conda install scikit-learn=0.19.0
conda install scipy=0.19.1
conda install sympy=1.1.1
```

9. 启动jupyter
```
jupyter notebook
```

10. 新建文件夹tensorflow

11. 新建python3文件

12. 重命名为test

13. 输入测试内容，shift+enter执行
```
import tensorflow as tf
hello= tf.constant('Hello,Tensorflow!')
sess=tf.Session()
print(sess.run(hello))
```

14. 完成，安装成功。
