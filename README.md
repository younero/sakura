# 用python代码描绘樱花绽放
基于python3.7
### 基本思想
1. 读取源视频文件，将其逐帧切分为源图片
2. 以文字为像素点新建图片
3. 对每一张源图片的像素信息进行提取，赋给新建的图片
4. 将新建图片逐帧合成，得到新视频
### 需要准备的有
1. 相关python库，主要包括：cv2、PIL
2. 源视频
### 操作步骤
1. 清空各个文件夹（包括pic、new等）内的图片
2. 将源视频放入video文件夹，同时修改第一个代码块中的文件名，即源代码中的`vidcap = cv2.VideoCapture('video/video.avi')`
3. 根据源视频的分辨率尺寸修改第三个代码块中的目标输出视频尺寸，即源代码中的`picvideo(r'new', (960, 544))`
4. 修改第三个代码块中生成新视频的文件名，即源代码中的`file_path = 'video/new.mp4'`
5. 逐步运行代码，在video文件夹中得到新视频
### 如何部署到ModelArts？
1. 打开华为云，进入ModelArts控制台
2. 选择右侧“开发环境”下的“NoteBook”
3. 点击操作界面右上角的“new”，依次新建video、pic、new、font文件夹
4. 点击操作界面右上角/“new”旁的“upload”，上传源视频和代码文件以及字体文件，具体存放位置为：
（1）源视频————>video
（2）代码————>根目录
（3）字体文件————>font
5. 点击源代码文件，在弹出的选项中将kernel设置为tensorflow，即可按4中的步骤运行
### 注意事项
1. 当源视频过长/分辨率较高的时候处理事件可能较长
2. 源视频文件格式为AVI
