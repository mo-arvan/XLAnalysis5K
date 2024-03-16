# Projects Artifacts

# Loading the docker image

Download the file from URL, then load the docker image using the command below:

```
bash
docker load --input rep-xla_image.tar


docker run --rm --gpus all -v ${PWD}:/workspace -it rep-xla bash

```


## Inside the docker

```bash
. ./artifact/scripts/run.sh
```

[output.log](artifact/results/output.log) contains the log of running the `generate_features.py` script. This script should output the result of table 1 in the paper, but it fails due to a runtime error. This issue was reported on June 23rd, 2022 on [Github](https://github.com/AlexJonesNLP/XLAnalysis5K/issues/1).