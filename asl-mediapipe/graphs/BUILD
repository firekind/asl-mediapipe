load("@rules_cc//cc:defs.bzl", "cc_library")

package(default_visibility = ["//visibility:public"])

cc_library(
    name = "desktop_offline_calculators",
    deps = [
        "@mediapipe//mediapipe/calculators/core:flow_limiter_calculator",
        "@mediapipe//mediapipe/calculators/core:gate_calculator",
        "@mediapipe//mediapipe/calculators/core:immediate_mux_calculator",
        "@mediapipe//mediapipe/calculators/core:packet_inner_join_calculator",
        "@mediapipe//mediapipe/calculators/core:previous_loopback_calculator",
        "@mediapipe//mediapipe/calculators/video:opencv_video_decoder_calculator",
        "@mediapipe//mediapipe/calculators/video:opencv_video_encoder_calculator",
    ],
)

cc_library(
    name = "desktop_tflite_calculators",
    deps = [
        ":desktop_offline_calculators",
        "@mediapipe//mediapipe/calculators/core:merge_calculator",
        "@mediapipe//mediapipe/graphs/hand_tracking/subgraphs:hand_detection_cpu",
        "@mediapipe//mediapipe/graphs/hand_tracking/subgraphs:hand_landmark_cpu",
        "@mediapipe//mediapipe/graphs/hand_tracking/subgraphs:renderer_cpu",
    ],
)