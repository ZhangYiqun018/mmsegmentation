# mmsegmentation简明使用方法

## 如何在新的数据集上训练segformer？
首先明确文件夹整体的结构
```
|-- mmsegmentation
|   |-- configs
|   |   |-- _base_
|   |   |   |-- datasets
|   |   |   |   |-- 存放数据集配置文件
|   |   |   |-- models
|   |   |   |   |-- 存放模型配置文件    
|   |   |   |-- schedules
|   |   |   |   |-- 存放优化器配置文件
|   |   |   |-- default_runtime.py
|   |   |-- segformer
|   |   |   |-- 存放模型针对数据集的细节配置文件
|   |-- data
|   |   |-- 存放数据集
|   |-- result
|   |   |-- 存放日志等结果文件（个人规定）
|   |-- tools
|   |   |-- 存放自定义工具文件
|   |   |-- train.py
|   |   |-- test.py
```
（刨除ade20k和cityscapes）
### mmsegmentation原本就包含的数据集
以chase_db1数据集为例，在segformer上训练
1. 将数据集原始配置文件`chase_db1.py`放到`.configs.base.datasets`中

2. 观察数据集发现，chase_db1数据集的窗口大小是128*128，在`configs.segformer`中创建`segformer_mit-b0_128x128_160k_chase_db1.py`

3. 


### 全新的数据集
