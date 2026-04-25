sebot_catering是整个流程
包含6个launch       --------- 5个cpp
sebot_arm              --------- arm          机械臂初始化 -> 伸展 -> while1 -> 失能
sebot_yolo             --------- yolo          初始化识别器 -> 初始化摄像头 -> 推理 -> cv2可视化
sebot_


机械臂 include/arm.hpp             ---------- USB通信设置 -- 类实现 === 串口及工具|构造函数|姿态学控制(x, y, z, pitch, yaw, roll)-单关节
识别器 include/detection.hpp
摄像头 cv::VideoCapture