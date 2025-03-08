# Hexapod RL

## CAD File
OnShape Link: [https://cad.onshape.com/documents/6791a2c4d6d4567f83869291/w/f8e5a40000bd118081a8919e/e/7156de64f21d497b44a0c287](https://cad.onshape.com/documents/6791a2c4d6d4567f83869291/w/f8e5a40000bd118081a8919e/e/7156de64f21d497b44a0c287)

## RL Demo
Create Virtual Environment
```sh
python -m venv ~/venvs/opus_rl
```

Install Required Packages
```sh
source ~/venvs/opus_rl/bin/activate
pip install -r requirements.txt
```

Install rsl_rl
```sh
source ~/venvs/opus_rl/bin/activate
cd rsl_rl && pip install -e .
cd ..
```

Export URDF from OnShape. **Configure your own OnShape API according to this [documentation](https://onshape-to-robot.readthedocs.io/en/latest/)**.
```sh
source ~/venvs/opus_rl/bin/activate
onshape-to-robot opus_urdf
```

Train an RL Policy
```sh
source ~/venvs/opus_rl/bin/activate
python opus_train.py
```

Monitor in TensorboardOpen [http://localhost:6006](http://localhost:6006)
```sh
tensorboard --logdir logs/fit
```

Evaluate an RL Policy
```sh
source ~/venvs/opus_rl/bin/activate
python opus_eval.py
```