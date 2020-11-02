# Description:
#   OpenCV libraries for video/image processing on Linux
load("@rules_cc//cc:defs.bzl", "cc_library")

licenses(["notice"])  # BSD license

exports_files(["LICENSE"])

cc_library(
    name = "opencv",
    srcs = [
        "lib/libopencv_core.so",
        "lib/libopencv_calib3d.so",
        "lib/libopencv_features2d.so",
        "lib/libopencv_highgui.so",
        "lib/libopencv_imgcodecs.so",
        "lib/libopencv_imgproc.so",
        "lib/libopencv_video.so",
        "lib/libopencv_videoio.so",
    ],
    hdrs = glob([
        # For OpenCV 3.x
        # "include/opencv2/**/*.h*",
        # For OpenCV 4.x
        "include/opencv4/opencv2/**/*.h*",
    ]),
    includes = [
        # For OpenCV 3.x
        # "include/",
        # For OpenCV 4.x
        "include/opencv4/",
    ],
    linkstatic = 1,
    visibility = ["//visibility:public"],
)
