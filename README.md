# make-dataset-VOC2007-
制作属于自己的VOC2007数据集
##  VOC数据格式(Visual Object Classes)
        └── VOCdevkit     #根目录
        └── VOC2007   #2007年份的数据集。
        ├── Annotations       #存放xml文件，与JPEGImages中的图片一一对应，解释图片的内容，包括标签和边界框的坐标信息等等。
        ├── ImageSets          #Action文件夹:存放的是人体动作，Layout文件夹:存放的是人体部位的数据，Segmentation:存放可用于分割的数据,Main存放的是同我们目标检测项目   相关的图像物体识别数据，文件夹下为txt文件，txt文件中每一行包含一个图片的名称，末尾会加上±1表示正负样本。 
        ├── JPEGImages       #存放图片，同Annotations中的xml文件一一对应。    


 第一步：JPEGSImages文件夹

1)把你的图片放到JPEGSImages里面，在VOC2007里面，图片文件名都是000001.jpg类似这样的，我们也统一格式，把我们的图片名字重命名成这样的，详见change_img_name.py

第二步：Annatations文件夹

LabelImg标注工具手动标注可自动生成图片信息的xml文件，主要有VOC以及YOLO两种数据格式，此外http://darkpgmr.tistory.com/16为附带目标追踪的图像标注工具，方便视频下的目标标注，文件格式为txt。


第三步：ImageSets文件夹中的Main文件夹中的四个文件

make_main_txt.py(划分测试图片，训练图片)

  ——————————————————————————————张旭
