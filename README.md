# SuperPoint Library
用于ORB_SLAM2_SP，利用 CAFFE-SSD 运行特征点提取，也可以单独运行。
## 安装
- 先安装caffe-ssd，https://github.com/efc-robot/caffe-ssd.git
- 安装superpoint

    `git clone https://github.com/efc-robot/superpoint.git`
        
    `cd superpoint && mkdir build`

    `cd build && cmake .. && make`

- 关于 ./CMakeLists.txt 的说明
    其中 13-14 行，需要修改
    ```CMAKE
    SET(CPU_ARCH x86_64)
    SET(CAFFE_DIR /home/yujc/robotws/caffe-ssd/) #选择caffe路径
    ```
    分别指定 体系 结构 x86_64（电脑） 还是 aarch64 （tx2)
    还有安装的 caffe-ssd 路径
  

## 使用
  提供了一个example演示使用方法。

  `cd example && ./example`
