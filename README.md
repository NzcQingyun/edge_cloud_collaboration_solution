upload_video_xml.py  包含了除去复赛要求的截取片段，高置信度行为判别，创建用户专属的obs，上传文件到obs（jpg和对应的xml），相当于为不同用户创建个性化模型省去手工标注的工作。
其中注释部分包含检验过程可视化，置信度可视化，网速测试并行。

upload_localcamera_xml.py是本地摄像头采取并生成xml

S3_api.py  该文件封装了对obs的相关函数，包含列出内容，创建桶，上传/下载文件，删除桶等函数

test.py  用于检验S3_api文件，里面的ak  sk 需要自己查看华为云账号的凭证

该程序作用是利用端侧设备收集用户专属的的疲劳/分神行为，并利用端侧初始模型自动标注，省去了手动标注数据集的成本，将数据集上传到云端用户专属obs，进行个性化的端侧模型优化，提升准确度。
考虑到家庭共用一台车，泛化的模型不能更好的满足用户的需求。为用户打造多套专属的检测模型。

上车时进行人脸识别，并匹配专属的模型。

该方案充分的利用到端侧算力资源，充分的利用了云端的算力优势。利用庞大的端云体系，对端侧设备做到协调优化升级
