# verl-trainingWithoutRollout

#### step 0 

prepare verl enviroment.

git clone this repo

#### step1

prepare `gsm8k`dateset

```sh
cd verl
python examples/data_preprocess/gsm8k.py
```

#### step2

use vllm to collect rollout data

```sh
python verl/trainer/vllm_rollout.py
```

#### step3

training without rollout

```sh
bash grpo_gsm8k_withoutrollout.sh
```



## 🧩 Experimental Results

#### Figure 1. Training with rollout
![Training Convergence Curve](./pic/fig1.png)

#### Figure 2. Training without rollout
![Validation Accuracy over Epochs](./pic/fig2.png)

#### Figure 3.Training without rollout

rollout data collect from fig4,rm_fn not same with fig1&fig2 

![Comparison with Other Models](./pic/fig3.png)

#### Figure 4.Training with rollout


![Comparison with Other Models](./pic/fig4.png)