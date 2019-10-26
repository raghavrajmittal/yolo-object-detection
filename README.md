# Object Detection in images and videos using the YOLO Object Detector

### Overview
Applies the YOLO Object Detector to detect and classift ~80 object types in a given image or video. The algorithm was first described by Redmon et al.,in their paper [*You Only Look Once: Unified, Real-time Object Detection*](https://arxiv.org/pdf/1506.02640.pdf). In this, we used YOLO3, which has some improvements over their original model ([*YOLOv3: An Incremental Improvement*](https://arxiv.org/pdf/1804.02767.pdf)). All their code can be found at https://pjreddie.com/yolo/.

The file size of the model weights is greater than github's size limit, so it's downloadable at https://pjreddie.com/yolo/ or instead just run download_model_weights.sh.

**Running the YOLO Object Detector on one image** <br/>
  * $ python --image images/baggage_claim.jpg
      * Required arguments:
        * --image (path to input image)
      * Option arguments:
        * --threshold (threshold when applying non-maxima suppression, type=float)
        * --confidence (minimum probability to filter weak detections, type=float)

**Running the YOLO Object Detector on a video** <br/>
  * $ python yolo_video.py --input videos/airport.mp4 --output output/airport_output.avi
      * Required arguments:
        * --input (path to input video)
        * --output(path to output video)
      * Optional arguments:
        * --threshold (threshold when applying non-maxima suppression, type=float)
        * --confidence (minimum probability to filter weak detections, type=float)

**Running the YOLO Object Detector on a live webcam video** <br/>
  * $ python yolo_real_time.py
      * Option argument:
        * --output (path to output video if you want to save)
        * --threshold (threshold when applying non-maxima suppression, type=float)
        * --confidence (minimum probability to filter weak detections, type=float)

**Credit:** <br/>
  * Adrian Rosebrock: https://www.pyimagesearch.com/2018/11/12/yolo-object-detection-with-opencv
