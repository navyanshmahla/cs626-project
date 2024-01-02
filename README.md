# Course Project: CS626

This is my project for the course CS626 IITB.

My aim was to improve the logical consistency and reasoning abilities of LLMs by implementing the approach **LogiGAN** from the paper: https://arxiv.org/abs/2205.08794

This is a pre-training approach which is highly compute intensive. Details of my implementation:

- Pre-training Corpus: BookCorpus (https://arxiv.org/abs/1506.06724)
- Compute: 1 nVidia A100 80GB GPU
- LLM for generator: google/t5-v1_1-small (60M parameters)
- LLM for verifier: albert-large-v2 (18M parameters)
- Number of GAN iterations: 3

This paper mentions warming up both generator anad verifier on the same dataset before pre-training for better convergence of both gen and verif LLM weights. Since I had limited compute, I chose to go with smaller LLMs and no warmup iterations at all.

This pre-trained model is deployed on huggingface at: https://huggingface.co/navyanshmahla/cs626-iitb-llm
PPT explaining the project in more details can be found at: https://docs.google.com/presentation/d/1yfKeoqo3SgqlQq5WSc-sGTxe53hzwVdtAJ0NQOsEVcU/edit?usp=sharing


```
@article{pi2022logigan,
  title={LogiGAN: Learning Logical Reasoning via Adversarial Pre-training},
  author={Pi, Xinyu and Zhong, Wanjun and Gao, Yan and Duan, Nan and Lou, Jian-Guang},
  journal={arXiv preprint arXiv:2205.08794},
  year={2022}
}
```
