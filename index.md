# Generative-based Target Speech Extraction with Speech Discretization and Vocoder
## Abstract
Target speech extraction (TSE) is a task aimed at isolating the speech of a specific target speaker from an audio mixture, using an auxiliary recording of that target speaker. 
Most existing TSE methods employ discriminative-based models to estimate the target speaker's proportion in the mixture, but they are plagued by the inability to effectively eliminate residual interfering speech. 
In this paper, we present a novel generation-based TSE approach by combining speech discretization and vocoder techniques. 
By predicting a sequence of discrete tokens with the auxiliary audio and employing a vocoder that takes discrete tokens as input, the target speech can be effectively re-synthesized.
Our experiments conducted on the WSJ0-2mix and Libri2mix datasets demonstrate that our proposed method yields high-quality target speech without interference.


## Test samples of Target Speech Extraction 
The sound files blow are some raw noisy wavs and the extracted speech from different methods.
All the samples are driven from the test set of Libri2Mix (16k min).

**(1) Sample1:**

Noisy wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-noisy.wav?raw=true"></audio>

Reference wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-ref.wav?raw=true"></audio>

DPCCN:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-dpccn.wav?raw=true"></audio>

Our discrete extraction:

(UniCATs-HuBERT-512)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-hubert512.wav?raw=true"></audio>
(UniCATs-HuBERT-4096)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-hubert4096.wav?raw=true"></audio>
(UniCATs-vq-wav2vec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-vq.wav?raw=true"></audio>
(encodec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample1-enc.wav?raw=true"></audio>
\\

**(2) Sample2:**

Noisy wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-noisy.wav?raw=true"></audio>

Reference wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-ref.wav?raw=true"></audio>

DPCCN:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-dpccn.wav?raw=true"></audio>

Our discrete extraction:

(UniCATs-HuBERT-512)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-hubert512.wav?raw=true"></audio>
(UniCATs-HuBERT-4096)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-hubert4096.wav?raw=true"></audio>
(UniCATs-vq-wav2vec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-vq.wav?raw=true"></audio>
(encodec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample3-enc.wav?raw=true"></audio>
\\

**(3) Sample3:**

Noisy wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-noisy.wav?raw=true"></audio>

Reference wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-ref.wav?raw=true"></audio>

DPCCN:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-dpccn.wav?raw=true"></audio>

Our discrete extraction:

(UniCATs-HuBERT-512)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-hubert512.wav?raw=true"></audio>
(UniCATs-HuBERT-4096)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-hubert4096.wav?raw=true"></audio>
(UniCATs-vq-wav2vec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-vq.wav?raw=true"></audio>
(encodec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample4-enc.wav?raw=true"></audio>
\\

**(4) Sample4:**

Noisy wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-noisy.wav?raw=true"></audio>

Reference wav:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-ref.wav?raw=true"></audio>

DPCCN:
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-dpccn.wav?raw=true"></audio>

Our discrete extraction:

(UniCATs-HuBERT-512)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-hubert512.wav?raw=true"></audio>
(UniCATs-HuBERT-4096)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-hubert4096.wav?raw=true"></audio>
(UniCATs-vq-wav2vec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-vq.wav?raw=true"></audio>
(encodec)
<audio id="audio" controls="" preload="none">
<source id="wav" src="https://github.com/earthmanylf/DiscreteTSE/blob/main/discretetse/wavs/sample5-enc.wav?raw=true"></audio>