# ASL mediapipe

This is a mediapipe project that uses the mediapipe hands solution to detect sign languages. Click [here](https://github.com/firekind/asl-model) for the model repo.

## Development

build using

```
$ bazel build -c opt --define MEDIAPIPE_DISABLE_GPU=1 asl-mediapipe:hand_tracking_cpu
```

and run using

```
$ GLOG_logtostderr=1 ./bazel-bin/asl-mediapipe/hand_tracking_cpu \
    --calculator_graph_config_file=asl-mediapipe/graphs/hand_tracking_desktop_live.pbtxt
```

Progress:
- [x] train model
- [x] move hands solution to this repo
- [ ] implement model in hands solution