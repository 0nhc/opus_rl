# Opus RL

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

Train an RL Policy
```sh
source ~/venvs/opus_rl/bin/activate
python nh_train.py
```

Monitor in TensorboardOpen [http://localhost:6006](http://localhost:6006)
```sh
tensorboard --logdir logs/fit
```

Evaluate an RL Policy
```sh
source ~/venvs/opus_rl/bin/activate
python nh_eval.py
```