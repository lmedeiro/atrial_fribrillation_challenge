# Atrial Fibrillation Classification with Recurrent Neural Networks

## Abstract


With the advent of portable one-lead ECG devices, there is a significant incentive to develop algorithms that are able to detect cardiac anomalies. For example, Atrial Fibrillation (AF), defined as uncoordinated atrial activation, which generally results in deterioration of atrial mechanical functions, is an arrhythmia whose early detection can significantly increase the patient's chance from retaining long-term, debilitating consequences, or even death. Since the advent of Deep Learning and the development progress of GPU computing, we have found that a possible contribution to this field could be Recurrent Neural Networks. As such this work proposes a solution based on Long-Short-Term-Memory (LSTM) Neural Networks which is able to consistently (with 92% accuracy on the test set) distinguish AF signals from normal sinus wave, alternate rhythms, or just noise. This is done in the context of one-lead ECG signals, with the dataset provided by Physionet's AF Classification Challenge from 2017.

## Repository Information

The data setup file located [here](./data_setup.ipynb) sets up the datasets as they will be used by the models. You should download the dataset from the [here](https://archive.physionet.org/challenge/2017/), and extract the folders in a desired folder. Then, you should modify the data directory paths accordingly. 

Two models were proposed in this experiment. The first model, a basic LSTM model located [here](./LSTM_training_notebook.ipynb), proposes a simple LSTM model that is able to produce a respectable performance in the test set (92% accuracy). 

The second model, located [here](./LSTM_FFT_training_notebook.ipynb), demonstrates a model which used the FFT to provide more information for the model. It produces an 87% accuracy on the test set at the moment. This is mainly due to an error in the augmentation step. In order to fix this and produce a better performance, one should reproduce the fft set on the augmented signal. You can email me for more questions, or general discussions about the subject. 

A final, more in-depth discussion regarding the project may be found [here](./project_report_LFM.pdf). 

If you use any of the material on this repo, please reference accordingly. 
