# face-generator [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/danwild/face-generator/master)
Face generation with Deep Convolutional Generative Adversarial Networks (DCGAN).

Uses the [CelebFaces Attributes Dataset (CelebA)](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) to train the networks, which then produces new faces (which are mostly white people due to bias in training dataset).

## Example output:
![Screenshot](/screenshots/example.png?raw=true)

## Setup notes
I'm using AWS' [Deep Learning AMI (Ubuntu) v23](https://aws.amazon.com/marketplace/pp/B077GCH38C) (however to run remotely on CPU follow the binder link).

```
# enter provided env
source activate pytorch_p36
python -m pip install -r requirements.txt

# quick setup jupyter
jupyter notebook --generate-config
sed -ie "s/#c.NotebookApp.ip = 'localhost'/#c.NotebookApp.ip = '*'/g" ~/.jupyter/jupyter_notebook_config.py
jupyter notebook --ip=0.0.0.0 --no-browser

# navigate to url provided (will need to replace IP)
# may also need to select kernal corresponding to env above
```

## Images

Need to download:
- [CelebFaces Attributes Dataset (CelebA)](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
  - Goes in: `<project_root>/assets`




