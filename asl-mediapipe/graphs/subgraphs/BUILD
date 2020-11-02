load(
    "@mediapipe/framework/tool:mediapipe_graph.bzl",
    "mediapipe_simple_subgraph",
)

mediapipe_simple_subgraph(
    name = "hand_detection_cpu",
    graph = "hand_detection_cpu.pbtxt",
    register_as = "HandDetectionSubgraph",
    deps = [
        "@mediapipe//mediapipe/calculators/image:image_properties_calculator",
        "@mediapipe//mediapipe/calculators/image:image_transformation_calculator",
        "@mediapipe//mediapipe/calculators/tflite:ssd_anchors_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_converter_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_custom_op_resolver_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_inference_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_tensors_to_detections_calculator",
        "@mediapipe//mediapipe/calculators/util:detection_label_id_to_text_calculator",
        "@mediapipe//mediapipe/calculators/util:detection_letterbox_removal_calculator",
        "@mediapipe//mediapipe/calculators/util:detections_to_rects_calculator",
        "@mediapipe//mediapipe/calculators/util:detections_to_render_data_calculator",
        "@mediapipe//mediapipe/calculators/util:non_max_suppression_calculator",
        "@mediapipe//mediapipe/calculators/util:rect_transformation_calculator",
    ],
)

mediapipe_simple_subgraph(
    name = "hand_landmark_cpu",
    graph = "hand_landmark_cpu.pbtxt",
    register_as = "HandLandmarkSubgraph",
    deps = [
        "@mediapipe//mediapipe/calculators/core:split_normalized_landmark_list_calculator",
        "@mediapipe//mediapipe/calculators/core:split_vector_calculator",
        "@mediapipe//mediapipe/calculators/image:image_cropping_calculator",
        "@mediapipe//mediapipe/calculators/image:image_properties_calculator",
        "@mediapipe//mediapipe/calculators/image:image_transformation_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_converter_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_custom_op_resolver_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_inference_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_tensors_to_classification_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_tensors_to_floats_calculator",
        "@mediapipe//mediapipe/calculators/tflite:tflite_tensors_to_landmarks_calculator",
        "@mediapipe//mediapipe/calculators/util:detections_to_rects_calculator",
        "@mediapipe//mediapipe/calculators/util:landmark_letterbox_removal_calculator",
        "@mediapipe//mediapipe/calculators/util:landmark_projection_calculator",
        "@mediapipe//mediapipe/calculators/util:landmarks_to_detection_calculator",
        "@mediapipe//mediapipe/calculators/util:landmarks_to_render_data_calculator",
        "@mediapipe//mediapipe/calculators/util:rect_transformation_calculator",
        "@mediapipe//mediapipe/calculators/util:thresholding_calculator",
        "//asl-mediapipe/graphs/calculators:hand_landmarks_to_rect_calculator",
    ],
)

mediapipe_simple_subgraph(
    name = "renderer_cpu",
    graph = "renderer_cpu.pbtxt",
    register_as = "RendererSubgraph",
    deps = [
        "@mediapipe//mediapipe/calculators/util:annotation_overlay_calculator",
        "@mediapipe//mediapipe/calculators/util:detections_to_render_data_calculator",
        "@mediapipe//mediapipe/calculators/util:labels_to_render_data_calculator",
        "@mediapipe//mediapipe/calculators/util:landmarks_to_render_data_calculator",
        "@mediapipe//mediapipe/calculators/util:rect_to_render_data_calculator",
    ],
)