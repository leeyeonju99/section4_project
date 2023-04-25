# section4_project
<pre><code>
import glob
 
val_img_list = glob.glob('/content/valid/*')
     

#테스트 데이터

from IPython.display import Image
import os
 
val_img_path = val_img_list[2]
 
!python detect.py --weights /content/yolov5/runs/train/test_yolov5s_1003/weights/best.pt --img 416 --conf 0.5 --exist-ok --source "{val_img_path}"
 
 #이미지로 저장
 
Image(os.path.join('/content/yolov5/runs/detect/exp', os.path.basename(val_img_path)))
 </code></pre>
