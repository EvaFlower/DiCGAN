# Differential-Critic GAN: Generating What You Want by a Cue of Preferences
Code for [Differential-Critic GAN: Generating What You Want by a Cue of Preferences (TNNLS 2022)](https://arxiv.org/abs/2107.06700)

# Requirements
- python3
- pytorch
- NumPy, SciPy, Matplotlib

# Training  
1) Pretrain mnist classifier:  
  - Under ./cls_mnist dir: run `python cls_mnist.py --save-model`  
    - **Expected Output**  
      - mnist_cnn.pt

2) Pretrain WGAN:
  - Run `python gan_mnist.py`
    - **Expected Output**  
      - `results/pretrain`
    
3) Train DiCGAN:
  - Run `python dicgan_mnist.py`
    - **Expected Output**
      - `results/$RUN_NAME/0/positive.txt` records the percentage of desired samples at each epoch
      - `results/$RUN_NAME/0/samples` contain sampled outputs from generator
      - Default `$RUN_NAME` is `dicgan_small_digits` 
    
# Citation
@article{yao2022differential,  
  title={Differential-Critic GAN: Generating What You Want by a Cue of Preferences},  
  author={Yao, Yinghua and Pan, Yuangang and Tsang, Ivor W and Yao, Xin},  
  journal={IEEE Transactions on Neural Networks and Learning Systems},  
  year={2022},  
  publisher={IEEE}  
}
