# Sound-classifiction-using-pytorch-and-Cnn-and-Ubersounddataset
Training a sound classifier using Urbendataset8k and CNN architecture and  visualizing the  the layers of the CNN.
A problem occuerd :
"/home/ali/PycharmProjects/Pytorch/Autoencoder /venv/bin/python" /home/ali/PycharmProjects/Pytorch/Autoencoder /urbansounddataset.py 
Using device cuda
There are 8732 samples in the dataset. ## it gives the number of samples but gives an error abou the necessity of working on cude despite working on it# 
Traceback (most recent call last):
  File "/home/ali/PycharmProjects/Pytorch/Autoencoder /urbansounddataset.py", line 99, in <module>
    signal, label = usd[0]
  File "/home/ali/PycharmProjects/Pytorch/Autoencoder /urbansounddataset.py", line 33, in __getitem__
    signal = self._resample_if_necessary(signal, sr)
  File "/home/ali/PycharmProjects/Pytorch/Autoencoder /urbansounddataset.py", line 56, in _resample_if_necessary
    signal = resampler(signal)
  File "/home/ali/PycharmProjects/Pytorch/Autoencoder /venv/lib/python3.8/site-packages/torch/nn/modules/module.py", line 1130, in _call_impl
    return forward_call(*input, **kwargs)
  File "/home/ali/PycharmProjects/Pytorch/Autoencoder /venv/lib/python3.8/site-packages/torchaudio/transforms/_transforms.py", line 959, in forward
    return _apply_sinc_resample_kernel(waveform, self.orig_freq, self.new_freq, self.gcd, self.kernel, self.width)
  File "/home/ali/PycharmProjects/Pytorch/Autoencoder /venv/lib/python3.8/site-packages/torchaudio/functional/functional.py", line 1496, in _apply_sinc_resample_kernel
    resampled = torch.nn.functional.conv1d(waveform[:, None], kernel, stride=orig_freq)
RuntimeError: Input type (torch.cuda.FloatTensor) and weight type (torch.FloatTensor) should be the same

Process finished with exit code 1
